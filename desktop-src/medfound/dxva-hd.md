---
description: Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Video Verarbeitung.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749256"
---
# <a name="dxva-hd"></a><span data-ttu-id="69490-103">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="69490-103">DXVA-HD</span></span>

<span data-ttu-id="69490-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Video Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="69490-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <span data-ttu-id="69490-105">DXVA-HD verwendet die GPU zum Ausführen von Funktionen wie Deinterlacing, Compositing und Farb Raum Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="69490-105">DXVA-HD uses the GPU to perform functions such as deinterlacing, compositing, and color-space conversion.</span></span>

<span data-ttu-id="69490-106">DXVA-HD ähnelt der [DXVA-Video Verarbeitung](dxva-video-processing.md) (DXVA-VP), bietet jedoch erweiterte Features und ein einfacheres Verarbeitungsmodell.</span><span class="sxs-lookup"><span data-stu-id="69490-106">DXVA-HD is similar to [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), but offers enhanced features and a simpler processing model.</span></span> <span data-ttu-id="69490-107">DXVA-HD bietet ein flexibleres Kompositions Modell und unterstützt die nächste Generation von HD-optischen Formaten und Broadcast Standards.</span><span class="sxs-lookup"><span data-stu-id="69490-107">By providing a more flexible composition model, DXVA-HD is designed to support the next generation of HD optical formats and broadcast standards.</span></span>

<span data-ttu-id="69490-108">Die DXVA-HD-API erfordert entweder einen WDDM-Anzeigetreiber, der die DXVA-HD-Gerätetreiber Schnittstelle (DDI) unterstützt, oder einen Plug-in-Software Prozessor.</span><span class="sxs-lookup"><span data-stu-id="69490-108">The DXVA-HD API requires either a WDDM display driver that supports the DXVA-HD device driver interface (DDI), or a plug-in software processor.</span></span>

-   [<span data-ttu-id="69490-109">Verbesserungen bei DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="69490-109">Improvements over DXVA-VP</span></span>](#improvements-over-dxva-vp)
-   [<span data-ttu-id="69490-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69490-110">Related topics</span></span>](#related-topics)

## <a name="improvements-over-dxva-vp"></a><span data-ttu-id="69490-111">Verbesserungen bei DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="69490-111">Improvements over DXVA-VP</span></span>

<span data-ttu-id="69490-112">DXVA-HD erweitert den Satz von Features, die von DXVA-VP bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="69490-112">DXVA-HD expands the set of features provided by DXVA-VP.</span></span> <span data-ttu-id="69490-113">Zu den Erweiterungen gehören:</span><span class="sxs-lookup"><span data-stu-id="69490-113">Enhancements include:</span></span>

-   <span data-ttu-id="69490-114">RGB-und YUV-Mischung.</span><span class="sxs-lookup"><span data-stu-id="69490-114">RGB and YUV mixing.</span></span> <span data-ttu-id="69490-115">Jeder Stream kann entweder RGB oder YUV sein.</span><span class="sxs-lookup"><span data-stu-id="69490-115">Any stream can be either RGB or YUV.</span></span> <span data-ttu-id="69490-116">Der primäre Stream und die untergeordneten Datenströme unterscheiden sich nicht länger.</span><span class="sxs-lookup"><span data-stu-id="69490-116">There is no longer a distinction between the primary stream and the substreams.</span></span>
-   <span data-ttu-id="69490-117">Deinterlacing mehrerer Datenströme.</span><span class="sxs-lookup"><span data-stu-id="69490-117">Deinterlacing of multiple streams.</span></span> <span data-ttu-id="69490-118">Jeder Datenstrom kann entweder progressiv oder Zeilen Sprung sein.</span><span class="sxs-lookup"><span data-stu-id="69490-118">Any stream can be either progressive or interlaced.</span></span> <span data-ttu-id="69490-119">Darüber hinaus können der Rhythmus und die Framerate von einem Eingabestream zum nächsten abweichen.</span><span class="sxs-lookup"><span data-stu-id="69490-119">Moreover, the cadence and frame rate can can vary from one input stream to the next.</span></span>
-   <span data-ttu-id="69490-120">RGB-Hintergrundfarben.</span><span class="sxs-lookup"><span data-stu-id="69490-120">RGB background colors.</span></span> <span data-ttu-id="69490-121">Bisher wurden nur YUV-Hintergrundfarben unterstützt.</span><span class="sxs-lookup"><span data-stu-id="69490-121">Previously, only YUV background colors were supported.</span></span>
-   <span data-ttu-id="69490-122">Luma-Schlüssel Erstellung.</span><span class="sxs-lookup"><span data-stu-id="69490-122">Luma keying.</span></span> <span data-ttu-id="69490-123">Wenn die Option zum Festlegen von Luma aktiviert ist, werden Luma-Werte, die innerhalb eines bestimmten Bereichs liegen, transparent.</span><span class="sxs-lookup"><span data-stu-id="69490-123">When luma keying is enabled, luma values that fall within a designated range become transparent.</span></span>
-   <span data-ttu-id="69490-124">Dynamischer Wechsel zwischen Deinterlacing-Modi.</span><span class="sxs-lookup"><span data-stu-id="69490-124">Dynamic switching between deinterlace modes.</span></span>

<span data-ttu-id="69490-125">DXVA-HD definiert außerdem einige erweiterte Funktionen, die von Treibern unterstützt werden können.</span><span class="sxs-lookup"><span data-stu-id="69490-125">DXVA-HD also defines some advanced features that drivers can support.</span></span> <span data-ttu-id="69490-126">Anwendungen sollten jedoch nicht davon ausgehen, dass diese Features von allen Treibern unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="69490-126">However, applications should not assume that all drivers will support these features.</span></span> <span data-ttu-id="69490-127">Zu den erweiterten Features gehören:</span><span class="sxs-lookup"><span data-stu-id="69490-127">The advanced features include:</span></span>

-   <span data-ttu-id="69490-128">Inverse Telecine (z. b. 60i bis 24p).</span><span class="sxs-lookup"><span data-stu-id="69490-128">Inverse telecine (for example, 60i to 24p).</span></span>
-   <span data-ttu-id="69490-129">Umwandlung von Frame Raten (z. b. 24 bis 120P).</span><span class="sxs-lookup"><span data-stu-id="69490-129">Frame-rate conversion (for example, 24p to 120p).</span></span>
-   <span data-ttu-id="69490-130">Alpha Füll Modi.</span><span class="sxs-lookup"><span data-stu-id="69490-130">Alpha-fill modes.</span></span>
-   <span data-ttu-id="69490-131">Filter für Rauschunterdrückung und Kanten Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="69490-131">Noise reduction and edge enhancement filtering.</span></span>
-   <span data-ttu-id="69490-132">Anamorphe nichtlineare Skalierung.</span><span class="sxs-lookup"><span data-stu-id="69490-132">Anamorphic non-linear scaling.</span></span>
-   <span data-ttu-id="69490-133">Extended YCbCr (xwycc).</span><span class="sxs-lookup"><span data-stu-id="69490-133">Extended YCbCr (xvYCC).</span></span>

<span data-ttu-id="69490-134">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="69490-134">This section contains the following topics.</span></span>

-   [<span data-ttu-id="69490-135">Erstellen eines DXVA-HD-Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="69490-135">Creating a DXVA-HD Video Processor</span></span>](creating-a-dxva-hd-video-processor.md)
-   [<span data-ttu-id="69490-136">Überprüfen unterstützter DXVA-HD-Formate</span><span class="sxs-lookup"><span data-stu-id="69490-136">Checking Supported DXVA-HD Formats</span></span>](checking-supported-dxva-hd-formats.md)
-   [<span data-ttu-id="69490-137">Erstellen von DXVA-HD-Video Oberflächen</span><span class="sxs-lookup"><span data-stu-id="69490-137">Creating DXVA-HD Video Surfaces</span></span>](creating-dxva-hd-video-surfaces.md)
-   [<span data-ttu-id="69490-138">Festlegen von DXVA-HD-Zuständen</span><span class="sxs-lookup"><span data-stu-id="69490-138">Setting DXVA-HD States</span></span>](setting-dxva-hd-states.md)
-   [<span data-ttu-id="69490-139">Ausführen von DXVA-HD-Blit</span><span class="sxs-lookup"><span data-stu-id="69490-139">Performing the DXVA-HD Blit</span></span>](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a><span data-ttu-id="69490-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69490-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69490-141">DirectX-Video Beschleunigung 2,0</span><span class="sxs-lookup"><span data-stu-id="69490-141">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="69490-142">DXVA-HD-Beispiel</span><span class="sxs-lookup"><span data-stu-id="69490-142">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
</dt> </dl>

 

 



