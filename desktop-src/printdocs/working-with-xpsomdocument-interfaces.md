---
description: In diesem Thema werden die Schnittstellen beschrieben, die Zugriff auf die Komponenten einer XPS OM auf Dokumentebene ermöglichen.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Arbeiten mit IXpsOMDocument-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7e8c0908382a731532f2697f03c8d67cb732ddf902f0c1ea181fe221d075fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033758"
---
# <a name="working-with-ixpsomdocument-interfaces"></a>Arbeiten mit IXpsOMDocument-Schnittstellen

In diesem Thema werden die Schnittstellen beschrieben, die Zugriff auf die Komponenten einer XPS OM auf Dokumentebene ermöglichen.



| Schnittstellenname                                                                        | Logische untergeordnete Schnittstellen                                      | Beschreibung                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Stellt einen einzelnen FixedDocument-Teil dar und bindet eine Auflistung von Seitenverweisen.<br/> [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) ist die Sammlungsschnittstelle, die zum Durchlaufen der [**IXpsOMPageReference-Schnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) in einem Dokument verwendet wird.<br/> |
| [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | Keine<br/>                                               | Stellt den DocumentStructure-Teil dar.<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a>Codebeispiele

Die Codebeispiele in diesem Abschnitt veranschaulichen, wie einige der Dokumentschnittstellen in einem Programm verwendet werden.

### <a name="get-the-page-references-of-a-document"></a>Abrufen der Seitenverweise eines Dokuments

Das folgende Codebeispiel ruft einen Zeiger auf die [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) ab, die die Liste der [**IXpsOMPageReference-Schnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) für das Dokument enthält, auf das vom *doc-Parameter* verwiesen wird.


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a>Abrufen der Dokumentstruktur eines Dokuments

Das folgende Codebeispiel ruft die Ressource ab, die die Dokumentstruktur enthält.


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 




