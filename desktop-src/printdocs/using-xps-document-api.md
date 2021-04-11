---
description: In diesem Abschnitt wird beschrieben, wie Sie die XPS-Dokument-API verwenden, um Programmieraufgaben auszuführen.
ms.assetid: 05b3d7b6-7628-4a5f-87b7-9d51ead51c79
title: Verwenden der XPS-Dokument-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8870c64bfa8fe478fb71174703c82a96e3723c53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960588"
---
# <a name="using-xps-document-api"></a><span data-ttu-id="32232-103">Verwenden der XPS-Dokument-API</span><span class="sxs-lookup"><span data-stu-id="32232-103">Using XPS Document API</span></span>

<span data-ttu-id="32232-104">In diesem Abschnitt wird beschrieben, wie Sie die [XPS-Dokument-API](documents-xps.md) verwenden, um Programmieraufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="32232-104">This section describes how to use the [XPS Document API](documents-xps.md) to perform programming tasks.</span></span>

<span data-ttu-id="32232-105">Beispiele für die Verwendung der [XPS-Dokument-API](documents-xps.md) in einem Programm finden Sie im Abschnitt [XPS-Dokument-API-Programmieraufgaben](#xps-document-api-programming-tasks) .</span><span class="sxs-lookup"><span data-stu-id="32232-105">For examples of how to use the [XPS Document API](documents-xps.md) in a program, see the [XPS Document API Programming Tasks](#xps-document-api-programming-tasks) section.</span></span>

<span data-ttu-id="32232-106">Informationen zur Verwendung des XPS-Objektmodells und seiner Implementierung durch die [XPS-Dokument-API](documents-xps.md)finden Sie unter [about XPS Document API](about-xps-document-api.md)(Informationen zur XPS-Dokument-API).</span><span class="sxs-lookup"><span data-stu-id="32232-106">For information about how to use the XPS Object Model and how it is implemented by the [XPS Document API](documents-xps.md), see [About XPS Document API](about-xps-document-api.md).</span></span>

## <a name="getting-started-with-the-xps-document-api"></a><span data-ttu-id="32232-107">Einstieg in die XPS-Dokument-API</span><span class="sxs-lookup"><span data-stu-id="32232-107">Getting Started with the XPS Document API</span></span>

<span data-ttu-id="32232-108">Bevor Sie mit der Verwendung der XPS-Dokument-API beginnen, stellen Sie sicher, dass Sie mit den folgenden Programmierthemen vertraut sind:</span><span class="sxs-lookup"><span data-stu-id="32232-108">Before you start using the XPS Document API, make sure that you are familiar with the following programming topics:</span></span><dl>

[<span data-ttu-id="32232-109">COM-Programmierung</span><span class="sxs-lookup"><span data-stu-id="32232-109">COM Programming</span></span>](/windows/desktop/com/component-object-model--com--portal)  
[<span data-ttu-id="32232-110">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="32232-110">Error Handling in COM</span></span>](/windows/desktop/com/error-handling-in-com)  
</dl>

<span data-ttu-id="32232-111">Wenn Sie die XPS-Dokument-API verwenden, möchten Sie möglicherweise auch die folgenden Technologien verwenden:</span><span class="sxs-lookup"><span data-stu-id="32232-111">When using the XPS Document API, you might also want to use the following technologies:</span></span><dl>

[<span data-ttu-id="32232-112">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="32232-112">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)  
[<span data-ttu-id="32232-113">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="32232-113">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)  
[<span data-ttu-id="32232-114">XPS-API für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="32232-114">XPS Digital Signature API</span></span>](xps-digital-signatures.md)  
</dl>

## <a name="xps-document-api-programming-tasks"></a><span data-ttu-id="32232-115">Programmieraufgaben der XPS-Dokument-API</span><span class="sxs-lookup"><span data-stu-id="32232-115">XPS Document API Programming Tasks</span></span>

<span data-ttu-id="32232-116">In den Themen in diesem Abschnitt wird beschrieben, wie die [XPS-Dokument-API](documents-xps.md) in einem Programm verwendet wird, und es wird veranschaulicht, wie einige gängige Programmieraufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="32232-116">The topics in this section describe how to use the [XPS Document API](documents-xps.md) in a program and demonstrate how to perform some common programming tasks.</span></span>

<span data-ttu-id="32232-117">Die XPS-Dokument-API verwendet Sammlungen, um mit Gruppen von Schnittstellen zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="32232-117">The XPS Document API uses collections to work with groups of interfaces.</span></span> <span data-ttu-id="32232-118">[Beim Arbeiten mit XPS OM-Erfassungs Schnittstellen](working-with-xps-object-model-collection-interfaces.md) wird beschrieben, wie Sie mit diesen Sammlungen programmieren.</span><span class="sxs-lookup"><span data-stu-id="32232-118">[Working with XPS OM Collection Interfaces](working-with-xps-object-model-collection-interfaces.md) describes how to program with these collections.</span></span>

<span data-ttu-id="32232-119">Die [allgemeinen XPS-Dokument Programmierungsaufgaben](common-xps-document-tasks.md) umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="32232-119">The [Common XPS Document Programming Tasks](common-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="32232-120">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="32232-120">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="32232-121">Erstellen eines leeren XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="32232-121">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="32232-122">Lesen eines XPS-Dokuments in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="32232-122">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="32232-123">Navigieren im XPS-OM</span><span class="sxs-lookup"><span data-stu-id="32232-123">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="32232-124">Schreiben von Text in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="32232-124">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="32232-125">Zeichnen von Grafiken in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="32232-125">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="32232-126">Platzieren von Bildern in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="32232-126">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="32232-127">Schreiben eines XPS-om in ein XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="32232-127">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="32232-128">Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="32232-128">Print an XPS OM</span></span>](print-an-xps-om.md)  
  
</dl>

<span data-ttu-id="32232-129">Die [erweiterten XPS-Dokument Programmierungsaufgaben](advanced-xps-document-tasks.md) umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="32232-129">The [Advanced XPS Document Programming Tasks](advanced-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="32232-130">XPS-Dokumente zusammenführen</span><span class="sxs-lookup"><span data-stu-id="32232-130">Merge XPS Documents</span></span>](merging-xps-documents.md)  
[<span data-ttu-id="32232-131">Verarbeiten von XPS-Dokumenten in einem XPSDrv-Filter</span><span class="sxs-lookup"><span data-stu-id="32232-131">Processing XPS Documents in an XPSDrv Filter</span></span>](processing-xps-documents-in-an-xpsdrv-filter.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="32232-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32232-132">Related topics</span></span>

<dl> <span data-ttu-id="32232-133"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="32232-133"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="32232-134">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="32232-134">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="32232-135">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="32232-135">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
