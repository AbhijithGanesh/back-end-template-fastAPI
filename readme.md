# FastAPI template

To run on the server, run the following commands:

## Commands

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run server

```bash
hypercorn run
```

### Test the endpoint

```bash
curl localhost:8000
```

This code defines a simple FastAPI application with a single endpoint that returns a JSON object with the message "Hello, World" when a GET request is sent to the root URL ("/"). The if **name** == "**main**": block at the end of the file ensures that the server is only run when the script is executed directly (not when it is imported as a module).

## Methods

```python
# Create a new item
@app.post("/items/")
async def create_item(item: Item):
    # Add logic to create a new item
    return {"status": "Item created"}

# Update an existing item
@app.patch("/items/{item_id}")
async def update_item(item_id: int, item: Item):
    # Add logic to update the item with the specified ID
    return {"status": f"Item {item_id} updated"}

# Delete an item
@app.delete("/items/{item_id}")
async def delete_item(item_id: int):
    # Add logic to delete the item with the specified ID
    return {"status": f"Item {item_id} deleted"}
```
## OpenAPI docs
You can view the OpenAPI docs at http://localhost:8000/docs
