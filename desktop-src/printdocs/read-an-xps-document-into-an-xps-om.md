---
description: Beschreibt, wie ein vorhandenes XPS-Dokument aus einer Datei in ein XPS-OM gelesen wird.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Lesen eines XPS-Dokuments in ein XPS-OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348219"
---
# <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="5321b-103">Lesen eines XPS-Dokuments in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="5321b-103">Read an XPS Document into an XPS OM</span></span>

<span data-ttu-id="5321b-104">Beschreibt, wie ein vorhandenes XPS-Dokument aus einer Datei in ein XPS-OM gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="5321b-104">Describes how to read an existing XPS document from a file into an XPS OM.</span></span>

<span data-ttu-id="5321b-105">Um ein XPS-OM aus einem XPS-Dokument zu erstellen, rufen Sie die [**ixpsomobjectfactory:: | atepackagefromfile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="5321b-105">To create an XPS OM from an XPS document, call the [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) method.</span></span>

<span data-ttu-id="5321b-106">Bevor Sie diese Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5321b-106">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="5321b-107">Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5321b-107">Code Example</span></span>

<span data-ttu-id="5321b-108">Im folgenden Codebeispiel wird davon ausgegangen, dass die in [Initialisieren eines XPS-OMS](xps-object-model-initialization.md) beschriebene Initialisierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5321b-108">The following code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has succeeded.</span></span>


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



<span data-ttu-id="5321b-109">Um ein XPS-OM aus einem XPS-Dokument zu erstellen, das als Stream gespeichert ist, rufen Sie [**ixpsomobjectfactory:: | atepackagefromstream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream)auf.</span><span class="sxs-lookup"><span data-stu-id="5321b-109">To create an XPS OM from an XPS document that is stored as a stream, call [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span></span>

## <a name="remarks"></a><span data-ttu-id="5321b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5321b-110">Remarks</span></span>

<span data-ttu-id="5321b-111">Wenn Sie direkt nach dem Lesen eines XPS-Pakets ein XPS-OM schreiben, können einige der ursprünglichen Inhalte verloren gehen oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5321b-111">If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.</span></span>

<span data-ttu-id="5321b-112">Einige der Änderungen, die in diesem Fall auftreten können, sind in der folgenden Tabelle aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5321b-112">Some of the changes that can occur in such case are listed in the table that follows:</span></span>

| <span data-ttu-id="5321b-113">Dokument Funktion</span><span class="sxs-lookup"><span data-stu-id="5321b-113">Document feature</span></span>                      | <span data-ttu-id="5321b-114">Aktion</span><span class="sxs-lookup"><span data-stu-id="5321b-114">Action</span></span>                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5321b-115">Digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="5321b-115">Digital signatures</span></span><br/>         | <span data-ttu-id="5321b-116">Aus dem Dokument entfernt</span><span class="sxs-lookup"><span data-stu-id="5321b-116">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="5321b-117">Verwerdsteuerungs-Teil</span><span class="sxs-lookup"><span data-stu-id="5321b-117">DiscardControl part</span></span><br/>        | <span data-ttu-id="5321b-118">Aus dem Dokument entfernt</span><span class="sxs-lookup"><span data-stu-id="5321b-118">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="5321b-119">Fremde Dokument Teile</span><span class="sxs-lookup"><span data-stu-id="5321b-119">Foreign document parts</span></span><br/>     | <span data-ttu-id="5321b-120">Aus dem Dokument entfernt</span><span class="sxs-lookup"><span data-stu-id="5321b-120">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="5321b-121">FixedPage-Markup</span><span class="sxs-lookup"><span data-stu-id="5321b-121">FixedPage markup</span></span><br/>           | <span data-ttu-id="5321b-122">Geändert von der ursprünglichen</span><span class="sxs-lookup"><span data-stu-id="5321b-122">Modified from the original</span></span><br/>                              |
| <span data-ttu-id="5321b-123">Ressourcenverzeichnis Markup</span><span class="sxs-lookup"><span data-stu-id="5321b-123">Resource dictionary markup</span></span><br/> | <span data-ttu-id="5321b-124">Geändert aus dem ursprünglichen, wenn das Optimization-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5321b-124">Modified from the original, if Optimization flag is set</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5321b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5321b-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5321b-126">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="5321b-126">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="5321b-127">Navigieren im XPS-OM</span><span class="sxs-lookup"><span data-stu-id="5321b-127">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="5321b-128">Schreiben von Text in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="5321b-128">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="5321b-129">Zeichnen von Grafiken in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="5321b-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="5321b-130">Platzieren von Bildern in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="5321b-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="5321b-131">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="5321b-131">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="5321b-132">**Ixpsomobjectfactory**</span><span class="sxs-lookup"><span data-stu-id="5321b-132">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="5321b-133">**Ixpsompackage**</span><span class="sxs-lookup"><span data-stu-id="5321b-133">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

<span data-ttu-id="5321b-134">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="5321b-134">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="5321b-135">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="5321b-135">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="5321b-136">Verpacken von APIs</span><span class="sxs-lookup"><span data-stu-id="5321b-136">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="5321b-137">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="5321b-137">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="5321b-138">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5321b-138">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

