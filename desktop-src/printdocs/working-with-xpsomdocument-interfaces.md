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
# <a name="working-with-ixpsomdocument-interfaces"></a><span data-ttu-id="812f3-103">Arbeiten mit ixpsomdocument-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="812f3-103">Working with IXpsOMDocument Interfaces</span></span>

<span data-ttu-id="812f3-104">In diesem Thema werden die Schnittstellen beschrieben, die den Zugriff auf die Komponenten auf Dokument Ebene eines XPS-OMS ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="812f3-104">This topic describes the interfaces that provide access to the document-level components of an XPS OM.</span></span>



| <span data-ttu-id="812f3-105">Schnittstellen Name</span><span class="sxs-lookup"><span data-stu-id="812f3-105">Interface name</span></span>                                                                        | <span data-ttu-id="812f3-106">Logische untergeordnete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="812f3-106">Logical child interfaces</span></span>                                      | <span data-ttu-id="812f3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="812f3-107">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="812f3-108">**Ixpsomdocument**</span><span class="sxs-lookup"><span data-stu-id="812f3-108">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [<span data-ttu-id="812f3-109">**Ixpsompagereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="812f3-109">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | <span data-ttu-id="812f3-110">Stellt einen einzelnen FixedDocument-Teil dar und bindet eine Auflistung von Seiten verweisen.</span><span class="sxs-lookup"><span data-stu-id="812f3-110">Represents a single FixedDocument part and binds a collection of page references.</span></span><br/> <span data-ttu-id="812f3-111">[**Ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) ist die Sammlungs Schnittstelle, die zum Durchlaufen der [**ixpsompagereferenzierungsschnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) in einem Dokument verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="812f3-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) is the collection interface that is used to iterate through the [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces in a document.</span></span><br/> |
| [<span data-ttu-id="812f3-112">**Ixpsomdocumentstructureresource**</span><span class="sxs-lookup"><span data-stu-id="812f3-112">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | <span data-ttu-id="812f3-113">Keine</span><span class="sxs-lookup"><span data-stu-id="812f3-113">None</span></span><br/>                                               | <span data-ttu-id="812f3-114">Stellt den DocumentStructure-Teil dar.</span><span class="sxs-lookup"><span data-stu-id="812f3-114">Represents the DocumentStructure part.</span></span><br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a><span data-ttu-id="812f3-115">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="812f3-115">Code Examples</span></span>

<span data-ttu-id="812f3-116">Die Codebeispiele in diesem Abschnitt veranschaulichen, wie einige der Dokument Schnittstellen in einem Programm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="812f3-116">The code examples in this section illustrate how some of the document interfaces are used in a program.</span></span>

### <a name="get-the-page-references-of-a-document"></a><span data-ttu-id="812f3-117">Seiten Verweise eines Dokuments erhalten</span><span class="sxs-lookup"><span data-stu-id="812f3-117">Get the page references of a document</span></span>

<span data-ttu-id="812f3-118">Im folgenden Codebeispiel wird ein Zeiger auf [**ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) abgerufen, das die Liste der [**ixpsompagereferenzierungsschnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) für das Dokument enthält, auf das vom *doc* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="812f3-118">The following code example gets a pointer to the [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) that contains the list of [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces for the document that is referenced by *doc* parameter.</span></span>


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



### <a name="get-the-document-structure-of-a-document"></a><span data-ttu-id="812f3-119">Die Dokumentstruktur eines Dokuments erhalten.</span><span class="sxs-lookup"><span data-stu-id="812f3-119">Get the document structure of a document</span></span>

<span data-ttu-id="812f3-120">Im folgenden Codebeispiel wird die Ressource abgerufen, die die Dokumentstruktur enthält.</span><span class="sxs-lookup"><span data-stu-id="812f3-120">The following code example gets the resource that contains the document structure.</span></span>


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



 

 




