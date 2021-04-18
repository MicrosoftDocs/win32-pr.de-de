---
title: Buffer-Objekt
description: Buffer-Objekt
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media-Format-SDK, Puffer Objekte
- Advanced Systems Format (ASF), Buffer Objects
- ASF (Advanced Systems Format), Buffer Objects
- Objekte, Puffer Objekte
- Puffer Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106339051"
---
# <a name="buffer-object"></a><span data-ttu-id="0690d-108">Buffer-Objekt</span><span class="sxs-lookup"><span data-stu-id="0690d-108">Buffer Object</span></span>

<span data-ttu-id="0690d-109">Ein Puffer Objekt wird verwendet, um Beispiele zu speichern und diese zwischen den Objekten des Windows Media Format SDK und ihrer Anwendung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="0690d-109">A buffer object is used to hold samples and deliver them between the objects of the Windows Media Format SDK and your application.</span></span> <span data-ttu-id="0690d-110">Wenn Sie eine Datei schreiben, übergeben Sie die Eingabe Beispiele mithilfe von Puffer Objekten an den Writer.</span><span class="sxs-lookup"><span data-stu-id="0690d-110">When you write a file, you pass your input samples to the writer using buffer objects.</span></span> <span data-ttu-id="0690d-111">Beim Lesen einer Datei stellt das Reader-Objekt oder das synchrone Reader-Objekt der Anwendung in Puffer Objekten Beispiele zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0690d-111">When you read a file, the reader object or synchronous reader object provides samples to your application in buffer objects.</span></span>

<span data-ttu-id="0690d-112">Zum Schreiben von Beispielen in eine Datei können Sie ein Puffer Objekt mithilfe der Methode [**iwmwriter:: Zuweisung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) erstellen.</span><span class="sxs-lookup"><span data-stu-id="0690d-112">For writing samples to a file, you can create a buffer object using the [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) method.</span></span> <span data-ttu-id="0690d-113">Zum Lesen von Beispielen erstellen sowohl das Reader-Objekt als auch das synchrone Reader-Objekt Puffer Objekte intern.</span><span class="sxs-lookup"><span data-stu-id="0690d-113">For reading samples, the reader object and synchronous reader object both create buffer objects internally.</span></span> <span data-ttu-id="0690d-114">Wenn Sie sich für entscheiden, können Sie mithilfe von [**iwmreaderallocatorex:: allocateforoutputex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) oder [**iwmreaderallocatorex:: allocateforstreamex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)eigene Puffer Objekte für das Lesen von Dateien zuordnen.</span><span class="sxs-lookup"><span data-stu-id="0690d-114">If you choose to, you can allocate your own buffer objects for file reading by using [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) or [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span>

<span data-ttu-id="0690d-115">Die folgenden Schnittstellen werden von jedem Puffer Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0690d-115">The following interfaces are supported by every buffer object.</span></span>



| <span data-ttu-id="0690d-116">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0690d-116">Interface</span></span>                          | <span data-ttu-id="0690d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0690d-117">Description</span></span>                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="0690d-118">**Inssbuffer**</span><span class="sxs-lookup"><span data-stu-id="0690d-118">**INSSBuffer**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | <span data-ttu-id="0690d-119">Steuert und ermöglicht den Zugriff auf den Puffer.</span><span class="sxs-lookup"><span data-stu-id="0690d-119">Controls and provides access to the buffer.</span></span>                          |
| [<span data-ttu-id="0690d-120">**INSSBuffer2**</span><span class="sxs-lookup"><span data-stu-id="0690d-120">**INSSBuffer2**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | <span data-ttu-id="0690d-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0690d-121">Not implemented.</span></span>                                                     |
| [<span data-ttu-id="0690d-122">**INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="0690d-122">**INSSBuffer3**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | <span data-ttu-id="0690d-123">Unterstützt Puffer Eigenschaften, die für dateneinheits Erweiterungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0690d-123">Supports buffer properties, which are used for data unit extensions.</span></span> |
| [<span data-ttu-id="0690d-124">**INSSBuffer4**</span><span class="sxs-lookup"><span data-stu-id="0690d-124">**INSSBuffer4**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | <span data-ttu-id="0690d-125">Listet Puffer Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="0690d-125">Enumerates buffer properties.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="0690d-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0690d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0690d-127">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="0690d-127">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




