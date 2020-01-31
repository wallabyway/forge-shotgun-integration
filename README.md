# forge-shotgun-integration

This is a node.js server connects shotgun with ForgeViewer.  It lets you view 3D assets or 2D PDFs/sheets, and mark them up with the ForgeViewer markup tools.  Any new markups created, are added back into shotgun.

![POC](https://user-images.githubusercontent.com/440241/73572333-85b34180-443e-11ea-8d89-a0e1ddd779bb.jpg)

#### Features:

1. Upload your assets into shotgun as normal
any AEC/MFG asset into Shotgun, such as ... [Revit .PDF IFC DWG Inventor Fusion Sketchup]
2. Click on the URL link to view in a browser with Forge-Viewer.  This will trigger a conversion to SVF format, using Forge MD API (https://forge.autodesk.com/en/docs/model-derivative/v2/developers_guide/overview/), if the SVF hasn't been converted yet.  The SVF viewable is saved back into shotgun's S3 storage, similar to LMV offline mode (https://extract.autodesk.io)
3. Markup Comments, 3D-pushpins previously made, will appear in the drawing
markup example: https://wallabyway.github.io/offline-pdf-markup

4. Add a new comment, push-pin or markup... and it will be saved back into Shotgun
via DIV: https://forge.autodesk.com/blog/placing-custom-markup-dbid
via pushpin-ext: https://stackoverflow.com/questions/58319702/loading-pushpin-in-the-forge-viewer-does-not-respect-the-viewerstate


This sample server is written in Nodejs

#### Resources:

Using the Shotgun Notes API, for retrieving a list of comments based on an asset, and saving comments back to Shotgun:
https://developer.shotgunsoftware.com/rest-api/?javascript--nodejs#read-the-thread-contents-for-a-note


#### Diagram:

![Screen Shot 2020-01-31 at 4 13 34 PM](https://user-images.githubusercontent.com/440241/73574834-b8603880-4444-11ea-98a2-5e1821fba360.jpg)
