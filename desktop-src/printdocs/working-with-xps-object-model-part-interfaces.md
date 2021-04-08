---
description: In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die den Zugriff auf XPS-Dokument Teile in einem XPS-OM ermöglichen.
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: XPS-OM-Teil Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81cbf17c26e4ba6c80199ee787b1ee11b28d260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959622"
---
# <a name="xps-om-part-interfaces"></a>XPS-OM-Teil Schnittstellen

In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die den Zugriff auf XPS-Dokument Teile in einem XPS-OM ermöglichen.



| Schnittstellen Name                                                                                                    | Logische untergeordnete Schnittstellen                                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Ixpsompart**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [**Ixpsomcoreproperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [**Ixpsomresource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | Dokument Komponenten, aus denen die Dokumentstruktur besteht.<br/>                                          |
| [**Ixpsomresource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [**Ixpsomparametresources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | Ixpsomfontresource<br/> Ixpsomimageresource<br/> Ixpsomcolorprofileresource<br/> Ixpsomprintticketresource<br/> Ixpsomremotediktattionaryresource<br/> Ixpsomdocumentstructureresource<br/> Ixpsomstoryfragmentsresource<br/> Ixpsomsignatureblockresource<br/> | Dokument Komponenten, die Elemente enthalten, die in einer Seite oder einem Dokument verwendet werden oder auf die verwiesen wird.<br/> |
| [**Ixpsomparamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | Keine<br/>                                                                                                                                                                                                                                                                                              | Eine Auflistung von Teil-URIs.<br/>                                                                        |



 

## <a name="code-examples"></a>Codebeispiele

Die folgenden Codebeispiele zeigen zwei Beispiele für die Verwendung der Part-Schnittstellen für den Zugriff auf XPS OM-Inhalt.

### <a name="get-the-name-of-a-document-part"></a>Den Namen eines Dokument Teils erhalten

Im folgenden Codebeispiel wird zu einem Dokument Teil navigiert und der Name des Teils abgerufen.


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Hiermit werden die Teil Ressourcen angezeigt, die dieser Seite zugeordnet sind.

Im folgenden Codebeispiel werden die Listen der verschiedenen Ressourcen abgerufen, die von dieser Seite verwendet werden.


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



 

