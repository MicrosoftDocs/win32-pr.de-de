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
# <a name="xps-om-part-interfaces"></a><span data-ttu-id="86f07-103">XPS-OM-Teil Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="86f07-103">XPS OM Part Interfaces</span></span>

<span data-ttu-id="86f07-104">In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die den Zugriff auf XPS-Dokument Teile in einem XPS-OM ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="86f07-104">This topic describes how to use the interfaces that provide access to XPS document parts in an XPS OM.</span></span>



| <span data-ttu-id="86f07-105">Schnittstellen Name</span><span class="sxs-lookup"><span data-stu-id="86f07-105">Interface name</span></span>                                                                                                    | <span data-ttu-id="86f07-106">Logische untergeordnete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="86f07-106">Logical child interfaces</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="86f07-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86f07-107">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86f07-108">**Ixpsompart**</span><span class="sxs-lookup"><span data-stu-id="86f07-108">**IXpsOMPart**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [<span data-ttu-id="86f07-109">**Ixpsomdocumentsequence**</span><span class="sxs-lookup"><span data-stu-id="86f07-109">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="86f07-110">**Ixpsomdocument**</span><span class="sxs-lookup"><span data-stu-id="86f07-110">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [<span data-ttu-id="86f07-111">**Ixpsompagereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="86f07-111">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [<span data-ttu-id="86f07-112">**Ixpsomcoreproperties**</span><span class="sxs-lookup"><span data-stu-id="86f07-112">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [<span data-ttu-id="86f07-113">**Ixpsomresource**</span><span class="sxs-lookup"><span data-stu-id="86f07-113">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | <span data-ttu-id="86f07-114">Dokument Komponenten, aus denen die Dokumentstruktur besteht.</span><span class="sxs-lookup"><span data-stu-id="86f07-114">Document components that make up the document structure.</span></span><br/>                                          |
| [<span data-ttu-id="86f07-115">**Ixpsomresource**</span><span class="sxs-lookup"><span data-stu-id="86f07-115">**IXpsOMResource**</span></span>](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [<span data-ttu-id="86f07-116">**Ixpsomparametresources**</span><span class="sxs-lookup"><span data-stu-id="86f07-116">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | <span data-ttu-id="86f07-117">Ixpsomfontresource</span><span class="sxs-lookup"><span data-stu-id="86f07-117">IXpsOMFontResource</span></span><br/> <span data-ttu-id="86f07-118">Ixpsomimageresource</span><span class="sxs-lookup"><span data-stu-id="86f07-118">IXpsOMImageResource</span></span><br/> <span data-ttu-id="86f07-119">Ixpsomcolorprofileresource</span><span class="sxs-lookup"><span data-stu-id="86f07-119">IXpsOMColorProfileResource</span></span><br/> <span data-ttu-id="86f07-120">Ixpsomprintticketresource</span><span class="sxs-lookup"><span data-stu-id="86f07-120">IXpsOMPrintTicketResource</span></span><br/> <span data-ttu-id="86f07-121">Ixpsomremotediktattionaryresource</span><span class="sxs-lookup"><span data-stu-id="86f07-121">IXpsOMRemoteDictionaryResource</span></span><br/> <span data-ttu-id="86f07-122">Ixpsomdocumentstructureresource</span><span class="sxs-lookup"><span data-stu-id="86f07-122">IXpsOMDocumentStructureResource</span></span><br/> <span data-ttu-id="86f07-123">Ixpsomstoryfragmentsresource</span><span class="sxs-lookup"><span data-stu-id="86f07-123">IXpsOMStoryFragmentsResource</span></span><br/> <span data-ttu-id="86f07-124">Ixpsomsignatureblockresource</span><span class="sxs-lookup"><span data-stu-id="86f07-124">IXpsOMSignatureBlockResource</span></span><br/> | <span data-ttu-id="86f07-125">Dokument Komponenten, die Elemente enthalten, die in einer Seite oder einem Dokument verwendet werden oder auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="86f07-125">Document components that contain elements that are used in or referenced by a page or a document.</span></span><br/> |
| [<span data-ttu-id="86f07-126">**Ixpsomparamecollection**</span><span class="sxs-lookup"><span data-stu-id="86f07-126">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | <span data-ttu-id="86f07-127">Keine</span><span class="sxs-lookup"><span data-stu-id="86f07-127">None</span></span><br/>                                                                                                                                                                                                                                                                                              | <span data-ttu-id="86f07-128">Eine Auflistung von Teil-URIs.</span><span class="sxs-lookup"><span data-stu-id="86f07-128">A collection of part URIs.</span></span><br/>                                                                        |



 

## <a name="code-examples"></a><span data-ttu-id="86f07-129">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="86f07-129">Code Examples</span></span>

<span data-ttu-id="86f07-130">Die folgenden Codebeispiele zeigen zwei Beispiele für die Verwendung der Part-Schnittstellen für den Zugriff auf XPS OM-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="86f07-130">The code examples that follow show two examples of how to use the part interfaces to access XPS OM content.</span></span>

### <a name="get-the-name-of-a-document-part"></a><span data-ttu-id="86f07-131">Den Namen eines Dokument Teils erhalten</span><span class="sxs-lookup"><span data-stu-id="86f07-131">Get the name of a document part</span></span>

<span data-ttu-id="86f07-132">Im folgenden Codebeispiel wird zu einem Dokument Teil navigiert und der Name des Teils abgerufen.</span><span class="sxs-lookup"><span data-stu-id="86f07-132">The following code example navigates to a document part and gets the part's name.</span></span>


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="86f07-133">Hiermit werden die Teil Ressourcen angezeigt, die dieser Seite zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="86f07-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="86f07-134">Im folgenden Codebeispiel werden die Listen der verschiedenen Ressourcen abgerufen, die von dieser Seite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86f07-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


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



 

