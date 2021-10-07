
 - ### If you are using Manjaro Linux and trying to enable mongo community server in your system , then type the following commands sequentially
       pamac install mongodb-bin
       sudo systemctl enable --now mongodb
       sudo systemctl status mongodb
    
    <br>

    ## Mongo Commands ( Same For All Operating System) <br><br>
- ### For Opening Mongo Shell from terminal
      mongo
- ### For creating a database or switching to a existing database
      use database_name
- ### For creating a collection and then inserting one document
      db.collection_name.insertOne({ attribute1 : , attribute2 :   , ... , attributeN: })
- ### For creating a collection and then inserting many document
      db.collection_name.insertMany([{ attribute1 : , attribute2 :   , ... , attributeN:},{ attribute1 : , attribute2 :   , ... , attributeM:}])
- ### For Finding All the documents in a collection
      db.collection_name.find()
- ### For Finding All the documents in a collection
      db.collection_name.find()
- ### For showing all the databases
      show dbs
- ### For showing all the Collections of current database
      show collections
- ### For clearing mongo shell : ctrl + l
- ### For quiting mongo shell 
      quit()