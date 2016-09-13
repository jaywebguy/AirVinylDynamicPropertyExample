# AirVinylDynamicPropertyExample
Pulled from tutorial on PluralSight. Final version of tutorial. Example of the Linq to Entity error.

After running the solution (your port number may be different)

Make this request:
http://localhost:5810/odata/People(1)?$expand=VinylRecords($expand=DynamicVinylRecordProperties)

You will get back an error similar to this:

message: "The specified type member 'Properties' is not supported in LINQ to Entities. Only initializers, entity members, and entity navigation properties are supported."


Here's working urls
http://localhost:5810/odata/People(1)/VinylRecords    this URL shows properties
http://localhost:5810/odata/People(1)?$expand=VinylRecords  url does not return dynamic properties. ( I think the other was aware of the bug/issue with OData, and worked around the issue in this example.
