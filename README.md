
 - ### If you are using Manjaro Linux and trying to enable mongo community server in your system , then type the following commands sequentially
       pamac install mongodb-bin
       sudo systemctl enable --now mongodb
       sudo systemctl status mongodb
    
    <br>

    ## Mongo Commands ( Same For All Operating System) <br><br>

## BASIC OPERATIONS
- ### For Opening Mongo Shell from terminal
      mongo
- ### For creating a database or switching to a existing database
      use database_name
- ### For showing all the databases
      show dbs
- ### For showing all the Collections of current database
      show collections
- ### For clearing mongo shell : ctrl + l
- ### For quiting mongo shell 
      quit()

## CREATE OPERATION
<br>

- ### For creating a collection and then inserting one document
      db.collection_name.insertOne({ attribute1 : , attribute2 :   , ... , attributeN: })
- ### For creating a collection and then inserting many document
      db.collection_name.insertMany([{ attribute1 : , attribute2 :   , ... , attributeN:},{ attribute1 : , attribute2 :   , ... , attributeM:}])

## READ OPEATION 
<br>

- ### For Finding All the documents in a collection
      db.collection_name.find()
- ### For Finding a single documents in a collection
      db.collection_name.find({attribute_name : value})
- ### And operation 
      db.collection_name.find({ attribute1 : ,  attribute2 : })
- ### And operation with query operator
      db.collection_name.find({ attribute1 : {$query_operator1 : value1}, attribute2 : {$query_operator2 : value2} })
- ### Or operation with Query Operator 
      db.collection_name.find({ $or : [{ attribute1 : {$query_operator1 : value1}},{attribute2 : {$query_operator2 : value2}} ] })
- ### Or operation finding instances of for defined key . Suppose we just want to find the names of users who have blood group B+ and lives in Sylhet Then command will be like this 
      db.collection_name.find({ $or : [{ attribute1 : {$query_operator1 : value1}},{attribute2 : {$query_operator2 : value2}} ] } , { attribute3 : value3})

### visit [Mongo DB Query Operators](https://docs.mongodb.com/manual/reference/operator/query/) for learning about query and Projection operators
 <br><br>
## UPDATE OPERATION
   <br>

- ### For updating one single document
      db.collection_name.updateOne( { filtering_part },{ information_to_be_updated } )

      means,

      db.collection_name.updateOne( { query } , { $set : {query}})

      means,

      db.collection_name.updateOne( { attribute1 : value1} , { $set : {attribute2 : value2 } } )
- ### For updating Many document
      db.collection_name.updateMany( { filtering_part },{ information_to_be_updated } )
      
      means,

      db.collection_name.updateMany( { query } , { $set : {query}})

      means,

      db.collection_name.updateMany( { attribute1 : value1} , { $set : {attribute2 : value2 } } )      
## DELETE OPERATION
   <br>

- ### For Deleting one single document
      db.collection_name.deleteOne( { filtering_part })

      means,

      db.collection_name.deleteOne( { query })

      means,

      db.collection_name.deleteOne( { attribute1 : value1})
- ### For Deleting Many document
      db.collection_name.deleteMany( { filtering_part })
      
      means,

      db.collection_name.deleteMany( { query })

      means,

      db.collection_name.deleteMany( { attribute1 : value1})   

- ### For deleting all documents
      db.collection_name.deleteMany({})   