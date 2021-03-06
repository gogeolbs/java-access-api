# java-access-api

This is an example of how to use **goGeo** API in Java.

The source code is based on **retrofit** rest client. The choice was made for the provided easy conversion between Java Objects and JSON. However, any rest client may be used with goGeo API.

In this example just some services was added. You are well come to fork this repository and improve it.

## Endpoints implemented
 
 * POST /database
 * GET  /database
 * GET  /databases/{database}
 * POST /databases/{database}/collections
 * GET  /databases/{database}/collections
 * GET  /databases/{database}/collections/{collection}
 * POST /databases/{database}/collections/{collection}/documents.json
 * GET  /databases/{database}/collections/{collection}/documents


## Usage

1. Clone this repository
2. Import it as *Maven project* in Eclipse IDE
3. Configure the following variables in *io.gogeo.app.App.java* file
  1. APIKEY
  2. DATABASENAME
  3. COLLECTIONNAME
4. Run as Java project

## Explanations

All the logic behind this example is in io.gogeo.app.App.java file. You can set your APIKEY, DATABASENAME and COLLECTIONNAME in the begin file. In order insert a document, change the document properties in *generateDocumentToInsert()* method.

Notice that, if the collection already has documents, the insertion will fail if the new one does not follow the same attribute structures. If it is the first document in the collection, the structure of layer will be a reflection of this document.
