# Query-Engine-for-English-language.
Data Source: BigBasket’s Products List data: 
Link Deliverables:
-> Implement vector embeddings on the given dataset and store them in a Vector DB like Qdrant. 
-> Implement an LLM on the DB that can give contextual answers to the queries strictly from the database. 
-> Wrap this LLM as an API using any framework.



# Sample Queries for Product Dataset

## Query 1: Retrieve Product Information by ID

**Request:**
```json
{
  "query": "Retrieve product information for ID 2"
}

**RESPONSE**

{
  "product_id": 2,
  "product_name": "Water Bottle - Orange",
  "category": "Kitchen, Garden & Pets",
  "sub_category": "Storage & Accessories",
  "brand": "Mastercook",
  "sale_price": 180,
  "market_price": 180,
  "type": "Water & Fridge Bottles",
  "rating": 2.3,
  "description": "Each product is microwave safe (without lid), refrigerator safe, dishwasher safe..."
}


{
  "query": "Find products in the 'Beauty & Hygiene' category"
}

**RESPONSE**

{
  "matching_products": [
    {
      "product_id": 1,
      "product_name": "Garlic Oil - Vegetarian Capsule 500 mg",
      "category": "Beauty & Hygiene",
      "sub_category": "Hair Care",
      "brand": "Sri Sri Ayurveda",
      "sale_price": 220,
      "market_price": 220,
      "type": "Hair Oil & Serum",
      "rating": 4.1,
      "description": "This Product contains Garlic Oil that is known to help proper digestion..."
    },
    {
      "product_id": 5,
      "product_name": "Creme Soft Soap - For Hands & Body",
      "category": "Beauty & Hygiene",
      "sub_category": "Bath & Hand Wash",
      "brand": "Nivea",
      "sale_price": 162,
      "market_price": 162,
      "type": "Bathing Bars & Soaps",
      "rating": 4.4,
      "description": "Nivea Creme Soft Soap gives your skin the best care that it must get..."
    }
  ]
}
