---
description: In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die Zugriff auf FixedDocumentSequence bereitstellen, das die oberste Ebene der Dokument Hierarchie in einem XPS-OM ist.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Arbeiten mit ixpsomdocumentsequence-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f108cbadf735b334f758102915abbda239a4e974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349472"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>Arbeiten mit ixpsomdocumentsequence-Schnittstellen

In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die Zugriff auf FixedDocumentSequence bereitstellen, das die oberste Ebene der Dokument Hierarchie in einem XPS-OM ist.



| Schnittstellen Name                                                          | Logische untergeordnete Schnittstellen                            | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | Gruppiert einen Satz von fixeddocuments in eine geordnete Liste.<br/>          |
| [**Ixpsomdocumentcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | Keine<br/>                                     | Die Auflistung von fixeddocuments in einer XPS-Dokument Sequenz.<br/> |



 

## <a name="code-example"></a>Codebeispiel

Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) -Schnittstelle abgerufen, die die Dokument Sequenz des durch *xpspackage* dargestellten XPS-OMS enthält. Im Beispiel werden dann die Dokumente in der-Auflistung aufgelistet.


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



 

 




