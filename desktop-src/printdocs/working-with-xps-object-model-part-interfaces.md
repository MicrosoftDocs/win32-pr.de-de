---
description: In diesem Thema wird beschrieben, wie die Schnittstellen verwendet werden, die Zugriff auf XPS-Dokumentteile in einer XPS OM ermöglichen.
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: XPS OM-Teilschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc93023f251d96f557dfc351949b58f7b9a0b67d308903d83b182de8f710e110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823900"
---
# <a name="xps-om-part-interfaces"></a>XPS OM-Teilschnittstellen

In diesem Thema wird beschrieben, wie die Schnittstellen verwendet werden, die Zugriff auf XPS-Dokumentteile in einer XPS OM ermöglichen.



| Schnittstellenname                                                                                                    | Logische untergeordnete Schnittstellen                                                                                                                                                                                                                                                                                     | Beschreibung                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPart**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | Dokumentkomponenten, aus denen sich die Dokumentstruktur zusammensetzt.<br/>                                          |
| [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | IXpsOMFontResource<br/> IXpsOMImageResource<br/> IXpsOMColorProfileResource<br/> IXpsOMPrintTicketResource<br/> IXpsOMRemoteDictionaryResource<br/> IXpsOMDocumentStructureResource<br/> IXpsOMStoryFragmentsResource<br/> IXpsOMSignatureBlockResource<br/> | Dokumentkomponenten, die Elemente enthalten, die in einer Seite oder einem Dokument verwendet werden oder auf die von einer Seite oder einem Dokument verwiesen wird.<br/> |
| [**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | Keine<br/>                                                                                                                                                                                                                                                                                              | Eine Auflistung von Teil-URIs.<br/>                                                                        |



 

## <a name="code-examples"></a>Codebeispiele

Die folgenden Codebeispiele zeigen zwei Beispiele für die Verwendung der Teilschnittstellen für den Zugriff auf XPS OM-Inhalte.

### <a name="get-the-name-of-a-document-part"></a>Abrufen des Namens eines Dokumentteils

Das folgende Codebeispiel navigiert zu einem Dokumentteil und ruft den Namen des Teils ab.


```C++
    HRESULT                         hr = S_OK;
    
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;
    IXpsOMPageReferenceCollection   *pages;
    IXpsOMPageReference             *pageRef;
    IXpsOMPage                      *page;

    IOpcPartUri                     *thisDocPartUri;
    IOpcPartUri                     *thisPagePartUri;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // package points to the IXpsOMPackage interface to walk.

    // get the fixed document sequence of the package
    hr = package->GetDocumentSequence(&docSeq);

    // get the fixed documents in the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // get the part name (URI) of this document
        hr = doc->GetPartName ( &thisDocPartUri );

        // get the doc contents
        hr = doc->GetPageReferences(&pages);
        
        // walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // get this page reference
            hr = pages->GetAt(thisPageRef, &pageRef );

            // get the part name (URI) of this page
            hr = pageRef->GetPage (&page);
            hr = page->GetPartName ( &thisPagePartUri );

            // do something with the part name
 
            thisPagePartUri->Release();
            page->Release();
            pageRef->Release();

            thisPageRef++;
        }
        pages->Release();
        thisDocPartUri->Release();
        doc->Release();
        thisDoc++;
    }

    docs->Release();
    docSeq->Release();

```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Abrufen der Teilressourcen, die dieser Seite zugeordnet sind

Das folgende Codebeispiel ruft die Listen der verschiedenen Ressourcen ab, die von dieser Seite verwendet werden.


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );

    // use resources

    dictionaryResources->Release();
    imageResources->Release();
    fontResources->Release();
    colorProfileResources->Release();
    resources->Release();
```



 

