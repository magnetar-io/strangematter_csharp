# strangematter_csharp

Description of the General Functionality Needed

## Base Library

1.	Present an API interface for Strange Matter.
2.	Methods – Create   (Payload Independent using JSON-LD for Definition from File)
  a.	Create Collection 
    i.	Add Components to a Collection 
    ii.	Add Relationship to Components in Collection 
  b.	Write Components to Disk 
    i.	This would be file system storage as a start, but this would eventually want to be abstracted so it could be written to a database, Blog Storage, whatever. 
  c.	Write Collection to Disk… 
3.	Methods - Read
  a.	Get Collection 
    i.	Get All Components in Collection 
    ii.	Get All Components of Type(s)  in Collection
      1.	My Foo Components
      2.	All relationships 
      3.	All Relationships of type “foo”
      4.	Other
4.	Methods – Update
  a.	Update Components
    i.	Add New Version
    ii.	Update Current Component 
    iii.	Write Components to Disk
  b.	Update Collection
    i.	Add Components to Collection
    ii.	Remove Outdated Versions from the Collection
    iii.	Save as New Version of Collection
## Payloads

5.	Take in JSON-LD Component Payload Definitions (Which is a sub part of the compomponent definition) 
6.	Via Code Generation make “Libraries” or “Extensions”, “DLLs” that can be Statically typed (This is so the API can do validation at write time)
a.	These want to be “installable” somehow… so the whole library doesn’t have to contain every component… I’d imagine the Component Definitions would want to live with this in a NPM-like library.  
b.	Extent Component API methods with New Definitions
c.	Write Payloads to Disk if they are outside the component.
