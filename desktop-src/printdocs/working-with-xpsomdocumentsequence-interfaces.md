---
description: In diesem Thema wird beschrieben, wie die Schnittstellen verwendet werden, die Zugriff auf FixedDocumentSequence ermöglichen, die oberste Ebene der Dokumenthierarchie in einer XPS OM.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Arbeiten mit IXpsOMDocumentSequence-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edac74809de63c1ae4e688bb99214d11b091ee4e877c921e9280abc9c6868121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098662"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>Arbeiten mit IXpsOMDocumentSequence-Schnittstellen

In diesem Thema wird beschrieben, wie die Schnittstellen verwendet werden, die Zugriff auf FixedDocumentSequence ermöglichen, die oberste Ebene der Dokumenthierarchie in einer XPS OM.



| Schnittstellenname                                                          | Logische untergeordnete Schnittstellen                            | Beschreibung                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | Gruppiert einen Satz von FixedDocuments in eine sortierte Liste.<br/>          |
| [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | Keine<br/>                                     | Die Auflistung von FixedDocuments in einer XPS-Dokumentsequenz.<br/> |



 

## <a name="code-example"></a>Codebeispiel

Das folgende Codebeispiel ruft einen Zeiger auf die [**IXpsOMDocumentSequence-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) ab, die die Dokumentsequenz der XPS OM enthält, die durch *xpsPackage* dargestellt wird. Im Beispiel werden dann die Dokumente in der Auflistung aufzählt.


```C++
    HRESULT                         hr = S_OK;

    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
 
        // use this doc for something

        // release this doc and then go to the next one
        doc->Release();
        thisDoc++;
    }
    // release the document collection and
    // the document sequence
    docs->Release();
    docSeq->Release();
```



 

 




