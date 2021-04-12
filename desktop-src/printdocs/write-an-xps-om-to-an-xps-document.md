---
description: Beschreibt, wie der Inhalt eines XPS-om in einem Programm in eine XPS-Dokument Datei geschrieben wird.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Schreiben eines XPS-om in ein XPS-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216868"
---
# <a name="write-an-xps-om-to-an-xps-document"></a><span data-ttu-id="dfac8-103">Schreiben eines XPS-om in ein XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="dfac8-103">Write an XPS OM to an XPS Document</span></span>

<span data-ttu-id="dfac8-104">Beschreibt, wie der Inhalt eines XPS-om in einem Programm in eine XPS-Dokument Datei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dfac8-104">Describes how to write the contents of an XPS OM in a program to an XPS document file.</span></span>

<span data-ttu-id="dfac8-105">Wenn ein Programm über ein XPS-OM verfügt, das ein umfassendes Dokument enthält, kann das Programm das XPS-om in eine Datei als XPS-Dokument schreiben, indem die Methode " [**Write-ToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) " der [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="dfac8-105">If a program has an XPS OM that contains a complete document, the program can write the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>

<span data-ttu-id="dfac8-106">Bevor Sie diese Codebeispiele in einem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="dfac8-106">Before using these code examples in a program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a><span data-ttu-id="dfac8-107">Schreiben eines kompletten XPS-om in ein XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="dfac8-107">Writing a complete XPS OM to an XPS document</span></span>

<span data-ttu-id="dfac8-108">Nachdem Sie den Inhalt eines XPS-Maps festgelegt haben, können Sie das XPS-OM als XPS-Dokument in einer Datei speichern, indem Sie die Methode " [**Write-ToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) " der [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dfac8-108">After you set the contents of an XPS OM, you can save the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> <span data-ttu-id="dfac8-109">Wenn Sie ein XPS-om in eine Datei oder einen Stream schreiben, wird nicht automatisch eine Miniaturansicht für das XPS-Dokument erstellt.</span><span class="sxs-lookup"><span data-stu-id="dfac8-109">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="dfac8-110">Verwenden Sie zum Erstellen einer Miniaturansicht des XPS-Dokuments die [**ixpsomthumbnailgenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dfac8-110">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="incrementally-writing-an-xps-document"></a><span data-ttu-id="dfac8-111">Inkrementelles Schreiben eines XPS-Dokuments</span><span class="sxs-lookup"><span data-stu-id="dfac8-111">Incrementally writing an XPS document</span></span>

<span data-ttu-id="dfac8-112">Die [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle kann verwendet werden, um die Teile eines XPS-Dokuments inkrementell zu schreiben; beispielsweise, wenn die Dokument Teile nacheinander erstellt oder verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="dfac8-112">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface can be used to write the parts of an XPS document incrementally; for example, when the document parts are created or processed in sequence.</span></span>

> [!Note]  
> <span data-ttu-id="dfac8-113">Wenn Sie ein XPS-om in eine Datei oder einen Stream schreiben, wird nicht automatisch eine Miniaturansicht für das XPS-Dokument erstellt.</span><span class="sxs-lookup"><span data-stu-id="dfac8-113">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="dfac8-114">Verwenden Sie zum Erstellen einer Miniaturansicht des XPS-Dokuments die [**ixpsomthumbnailgenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dfac8-114">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dfac8-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dfac8-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dfac8-116">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="dfac8-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="dfac8-117">Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="dfac8-117">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="dfac8-118">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="dfac8-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="dfac8-119">**Iopcparamei**</span><span class="sxs-lookup"><span data-stu-id="dfac8-119">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="dfac8-120">**Ixpsompackage**</span><span class="sxs-lookup"><span data-stu-id="dfac8-120">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="dfac8-121">**Ixpsomthumbnailgenerator**</span><span class="sxs-lookup"><span data-stu-id="dfac8-121">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

<span data-ttu-id="dfac8-122">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="dfac8-122">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="dfac8-123">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="dfac8-123">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="dfac8-124">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="dfac8-124">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="dfac8-125">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="dfac8-125">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
