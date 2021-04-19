---
description: In diesem Thema werden die Schnittstellen beschrieben, die den Zugriff auf die Komponenten auf Dokument Ebene eines XPS-OMS ermöglichen.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Arbeiten mit ixpsomdocument-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360516"
---
# <a name="working-with-ixpsomdocument-interfaces"></a>Arbeiten mit ixpsomdocument-Schnittstellen

In diesem Thema werden die Schnittstellen beschrieben, die den Zugriff auf die Komponenten auf Dokument Ebene eines XPS-OMS ermöglichen.



| Schnittstellen Name                                                                        | Logische untergeordnete Schnittstellen                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Stellt einen einzelnen FixedDocument-Teil dar und bindet eine Auflistung von Seiten verweisen.<br/> [**Ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) ist die Sammlungs Schnittstelle, die zum Durchlaufen der [**ixpsompagereferenzierungsschnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) in einem Dokument verwendet wird.<br/> |
| [**Ixpsomdocumentstructureresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | Keine<br/>                                               | Stellt den DocumentStructure-Teil dar.<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a>Codebeispiele

Die Codebeispiele in diesem Abschnitt veranschaulichen, wie einige der Dokument Schnittstellen in einem Programm verwendet werden.

### <a name="get-the-page-references-of-a-document"></a>Seiten Verweise eines Dokuments erhalten

Im folgenden Codebeispiel wird ein Zeiger auf [**ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) abgerufen, das die Liste der [**ixpsompagereferenzierungsschnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) für das Dokument enthält, auf das vom *doc* -Parameter verwiesen wird.


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



### <a name="get-the-document-structure-of-a-document"></a>Die Dokumentstruktur eines Dokuments erhalten.

Im folgenden Codebeispiel wird die Ressource abgerufen, die die Dokumentstruktur enthält.


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



 

 




