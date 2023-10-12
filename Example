import pandas as pd

df = pd.read_excel('loc.xlsx')
pd.set_option("Display.max_columns", None)
df.head()

import pymongo
from pymongo import MongoClient

username = ""
password = ""
database_name = ""
host = "27017"  # You can use "localhost" for a local MongoDB instance

connection_string = f"mongodb://{username}:{password}@{host}/{database_name}"

client = pymongo.MongoClient(connection_string)

db = cluster["database"]
collection = db["files"]

data = # add information to test collection
collection.insert_one(data)

# we add a list to the collection
list_of_dicts = df.to_dict(orient='records')
collection.insert_many(list_of_dicts)

# we can also add a image to the collection
import gridfs
fs = gridfs.GridFS(db)

image_file = open("my-image.png", "rb")

file_id = fs.put(image_file, filename="my-image.png")

image_file.close()
