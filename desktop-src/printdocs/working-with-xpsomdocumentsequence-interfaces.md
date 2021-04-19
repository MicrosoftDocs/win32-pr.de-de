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
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a><span data-ttu-id="5343b-103">Arbeiten mit ixpsomdocumentsequence-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5343b-103">Working with IXpsOMDocumentSequence Interfaces</span></span>

<span data-ttu-id="5343b-104">In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die Zugriff auf FixedDocumentSequence bereitstellen, das die oberste Ebene der Dokument Hierarchie in einem XPS-OM ist.</span><span class="sxs-lookup"><span data-stu-id="5343b-104">This topic describes how to use the interfaces that provide access to the FixedDocumentSequence, which is the top level of the document hierarchy in an XPS OM.</span></span>



| <span data-ttu-id="5343b-105">Schnittstellen Name</span><span class="sxs-lookup"><span data-stu-id="5343b-105">Interface name</span></span>                                                          | <span data-ttu-id="5343b-106">Logische untergeordnete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5343b-106">Logical child interfaces</span></span>                            | <span data-ttu-id="5343b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5343b-107">Description</span></span>                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="5343b-108">**Ixpsomdocumentsequence**</span><span class="sxs-lookup"><span data-stu-id="5343b-108">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [<span data-ttu-id="5343b-109">**Ixpsomdocument**</span><span class="sxs-lookup"><span data-stu-id="5343b-109">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | <span data-ttu-id="5343b-110">Gruppiert einen Satz von fixeddocuments in eine geordnete Liste.</span><span class="sxs-lookup"><span data-stu-id="5343b-110">Groups a set of FixedDocuments into an ordered list.</span></span><br/>          |
| [<span data-ttu-id="5343b-111">**Ixpsomdocumentcollection**</span><span class="sxs-lookup"><span data-stu-id="5343b-111">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | <span data-ttu-id="5343b-112">Keine</span><span class="sxs-lookup"><span data-stu-id="5343b-112">None</span></span><br/>                                     | <span data-ttu-id="5343b-113">Die Auflistung von fixeddocuments in einer XPS-Dokument Sequenz.</span><span class="sxs-lookup"><span data-stu-id="5343b-113">The collection of FixedDocuments in an XPS document sequence.</span></span><br/> |



 

## <a name="code-example"></a><span data-ttu-id="5343b-114">Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5343b-114">Code Example</span></span>

<span data-ttu-id="5343b-115">Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) -Schnittstelle abgerufen, die die Dokument Sequenz des durch *xpspackage* dargestellten XPS-OMS enthält.</span><span class="sxs-lookup"><span data-stu-id="5343b-115">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface that contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span> <span data-ttu-id="5343b-116">Im Beispiel werden dann die Dokumente in der-Auflistung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5343b-116">The example then enumerates the documents in the collection.</span></span>


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



 

 




