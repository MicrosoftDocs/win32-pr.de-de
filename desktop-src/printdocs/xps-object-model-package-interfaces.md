---
description: Die Paket Schnittstellen stellen die oberste Ebene des XPS-OMS dar, die einer XPS-Dokument Datei entspricht.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: XPS-OM-Paket Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863916"
---
# <a name="xps-om-package-interfaces"></a><span data-ttu-id="ae787-103">XPS-OM-Paket Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ae787-103">XPS OM Package Interfaces</span></span>

<span data-ttu-id="ae787-104">Die Paket Schnittstellen stellen die oberste Ebene des XPS-OMS dar, die einer XPS-Dokument Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="ae787-104">The package interfaces represent the top level of the XPS OM, which corresponds to an XPS document file.</span></span> <span data-ttu-id="ae787-105">Diese Schnittstellen enthalten Methoden, die ein XPS-om in ein XPS-Dokument oder einen XPS-Stream Serialisieren und ein XPS-Paket deserialisieren, um ein XPS-OM zu erstellen, das einem Programm den Zugriff auf den Inhalt eines Dokuments ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ae787-105">These interfaces contain methods that serialize an XPS OM to an XPS document or stream, and deserialize an XPS package to create an XPS OM that enables a program to access the contents of a document.</span></span>



| <span data-ttu-id="ae787-106">Schnittstellen Name</span><span class="sxs-lookup"><span data-stu-id="ae787-106">Interface name</span></span>                                                  | <span data-ttu-id="ae787-107">Logische untergeordnete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ae787-107">Logical child interfaces</span></span>                                                                                                            | <span data-ttu-id="ae787-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae787-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae787-109">**Ixpsompackage**</span><span class="sxs-lookup"><span data-stu-id="ae787-109">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [<span data-ttu-id="ae787-110">**Ixpsomdocumentsequence**</span><span class="sxs-lookup"><span data-stu-id="ae787-110">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="ae787-111">**Ixpsomcoreproperties**</span><span class="sxs-lookup"><span data-stu-id="ae787-111">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="ae787-112">Das gesamte XPS-OM, das dem Paket entspricht, das das XPS-Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="ae787-112">The complete XPS OM that corresponds to the package that contains the XPS document.</span></span><br/> |
| [<span data-ttu-id="ae787-113">**Ixpsompackagewriter**</span><span class="sxs-lookup"><span data-stu-id="ae787-113">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | <span data-ttu-id="ae787-114">Keine</span><span class="sxs-lookup"><span data-stu-id="ae787-114">None</span></span><br/>                                                                                                                     | <span data-ttu-id="ae787-115">Aktiviert die inkrementelle Serialisierung von Dokument Seiten zu einem Paket.</span><span class="sxs-lookup"><span data-stu-id="ae787-115">Enables incremental serialization of document pages to a package.</span></span><br/>                   |
| [<span data-ttu-id="ae787-116">**Ixpsomcoreproperties**</span><span class="sxs-lookup"><span data-stu-id="ae787-116">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="ae787-117">Keine</span><span class="sxs-lookup"><span data-stu-id="ae787-117">None</span></span><br/>                                                                                                                     | <span data-ttu-id="ae787-118">Greift auf die Dokument Metadaten zu.</span><span class="sxs-lookup"><span data-stu-id="ae787-118">Accesses the document metadata.</span></span> <br/>                                                    |



 

## <a name="code-examples"></a><span data-ttu-id="ae787-119">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="ae787-119">Code Examples</span></span>

<span data-ttu-id="ae787-120">Die folgenden Codebeispiele veranschaulichen, wie einige der Paket Schnittstellen von einem Programm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae787-120">The code examples that follow illustrate how some of the package interfaces are used by a program.</span></span> <span data-ttu-id="ae787-121">Sofern nicht anders angegeben, sind alle kursiv formatierten Elemente Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="ae787-121">Unless noted otherwise, all italicized items are parameter names.</span></span>

-   [<span data-ttu-id="ae787-122">Lesen eines XPS-Dokuments in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ae787-122">Read an XPS document into an XPS OM</span></span>](#read-an-xps-document-into-an-xps-om)
-   [<span data-ttu-id="ae787-123">Schreiben eines XPS-Maps in eine XPS-Dokument Datei</span><span class="sxs-lookup"><span data-stu-id="ae787-123">Write an XPS OM to an XPS document file</span></span>](#write-an-xps-om-to-an-xps-document-file)
-   [<span data-ttu-id="ae787-124">Zugreifen auf die Dokument Sequenz des XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="ae787-124">Access the document sequence of the XPS OM</span></span>](#access-the-document-sequence-of-the-xps-om)
-   [<span data-ttu-id="ae787-125">Zugreifen auf die coreproperties des Dokuments</span><span class="sxs-lookup"><span data-stu-id="ae787-125">Access the document's CoreProperties</span></span>](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="ae787-126">Lesen eines XPS-Dokuments in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ae787-126">Read an XPS document into an XPS OM</span></span>

<span data-ttu-id="ae787-127">In einem vorhandenen XPS-Dokument, dessen Dateiname in *xpsdocumentfilename* gespeichert ist, wird in diesem Codebeispiel ein XPS-OM erstellt, auf das von *xpspackage* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ae787-127">From an existing XPS document whose file name is stored in *xpsDocumentFilename*, this code example creates an XPS OM that is referenced by *xpsPackage*.</span></span>


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a><span data-ttu-id="ae787-128">Schreiben eines XPS-Maps in eine XPS-Dokument Datei</span><span class="sxs-lookup"><span data-stu-id="ae787-128">Write an XPS OM to an XPS document file</span></span>

<span data-ttu-id="ae787-129">Im folgenden Codebeispiel wird das XPS-OM geschrieben, auf das von *xpspackage* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ae787-129">The following code example writes the XPS OM that is referenced by *xpsPackage*.</span></span> <span data-ttu-id="ae787-130">Im Beispiel wird ein XPS-Dokument in der Datei erstellt, deren Name in *filename* gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ae787-130">The example creates an XPS document in the file whose name is stored in *fileName*.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a><span data-ttu-id="ae787-131">Zugreifen auf die Dokument Sequenz des XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="ae787-131">Access the document sequence of the XPS OM</span></span>

<span data-ttu-id="ae787-132">Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) -Schnittstelle abgerufen, die die Dokument Sequenz des durch *xpspackage* dargestellten XPS-OMS enthält.</span><span class="sxs-lookup"><span data-stu-id="ae787-132">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface, which contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a><span data-ttu-id="ae787-133">Zugreifen auf die coreproperties des Dokuments</span><span class="sxs-lookup"><span data-stu-id="ae787-133">Access the document's CoreProperties</span></span>

<span data-ttu-id="ae787-134">Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomcoreproperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) -Schnittstelle abgerufen, sodass das Programm auf den Inhalt des coreproperties-Teils zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="ae787-134">The following is code example obtains a pointer to the [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) interface, allowing the program to access the contents of the CoreProperties part.</span></span> <span data-ttu-id="ae787-135">Im Beispiel wird davon ausgegangen, dass das Dokument in ein XPS-OM gelesen wurde, das durch *xpspackage* dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ae787-135">In the example, the document is assumed to have been read into an XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a><span data-ttu-id="ae787-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae787-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae787-137">Verwenden der ixpsompackagewriter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ae787-137">Using the IXpsOMPackageWriter Interface</span></span>](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[<span data-ttu-id="ae787-138">Navigieren im XPS-OM</span><span class="sxs-lookup"><span data-stu-id="ae787-138">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="ae787-139">**Ixpsomdocumentsequence-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae787-139">**IXpsOMDocumentSequence Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="ae787-140">**Ixpsompackage-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae787-140">**IXpsOMPackage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="ae787-141">**Ixpsompackagewriter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae787-141">**IXpsOMPackageWriter Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="ae787-142">**Ixpsomcoreproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae787-142">**IXpsOMCoreProperties Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




