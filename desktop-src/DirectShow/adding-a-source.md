---
description: Hinzufügen einer Quelle
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Hinzufügen einer Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342963"
---
# <a name="adding-a-source"></a><span data-ttu-id="41d1d-103">Hinzufügen einer Quelle</span><span class="sxs-lookup"><span data-stu-id="41d1d-103">Adding a Source</span></span>

<span data-ttu-id="41d1d-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="41d1d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="41d1d-105">Erstellen Sie ein Quell Objekt auf die gleiche Weise, wie Sie andere Timeline-Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="41d1d-105">Create a source object the same way you create other timeline objects.</span></span> <span data-ttu-id="41d1d-106">Vor dem Einfügen in die Zeitachse müssen Sie jedoch mindestens die folgenden Eigenschaften für die Quelle angeben.</span><span class="sxs-lookup"><span data-stu-id="41d1d-106">Before inserting it into the timeline, however, you must specify at least the following properties on the source.</span></span>

-   <span data-ttu-id="41d1d-107">Die Start-und Endzeit Zeiten, relativ zur Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="41d1d-107">The start and stop times, relative to the timeline.</span></span> <span data-ttu-id="41d1d-108">Aufrufen der [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="41d1d-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span>
-   <span data-ttu-id="41d1d-109">Die Mediendatei, die als Quelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="41d1d-109">The media file to use as a source.</span></span> <span data-ttu-id="41d1d-110">Aufrufen der [**iamtimelinesrc:: setmedianame**](iamtimelinesrc-setmedianame.md) -Methode mit einer breit Zeichen-Zeichenfolge, die den Namen der Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="41d1d-110">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) method with a wide-character string representing the name of the file.</span></span>
-   <span data-ttu-id="41d1d-111">Die Start-und Endzeiten der Medien, die relativ zur ursprünglichen Datei sind.</span><span class="sxs-lookup"><span data-stu-id="41d1d-111">The media start and stop times, which are relative to the original file.</span></span> <span data-ttu-id="41d1d-112">Aufrufen der [**iamtimelinesrc:: setmediatimes**](iamtimelinesrc-setmediatimes.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="41d1d-112">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="41d1d-113">Weitere Informationen zu Medien Zeiten finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="41d1d-113">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="41d1d-114">Im folgenden Beispiel startet der Quellclip vier Sekunden in der Datei.</span><span class="sxs-lookup"><span data-stu-id="41d1d-114">In the following example, the source clip starts four seconds into the file.</span></span> <span data-ttu-id="41d1d-115">Die Medien Dauer beträgt 10 Sekunden, doppelt so lang die Dauer der Zeitachse, was bedeutet, dass die Quelle mit der doppelten normalen Geschwindigkeit wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="41d1d-115">The media duration is 10 seconds, twice the length of the timeline duration, meaning the source will play at twice normal speed.</span></span> <span data-ttu-id="41d1d-116">Die Konstanten Einheiten werden als 10 Millionen (10 ^ 7) definiert und sind gleich einer Sekunde.</span><span class="sxs-lookup"><span data-stu-id="41d1d-116">The constant UNITS is defined as 10000000 (10^7) and equals one second.</span></span>


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> <span data-ttu-id="41d1d-117">Derzeit kann des nicht gleichzeitig mehr als 75 Quellen gleichzeitig erzeugen, die mit Video Compression Manager-Codecs (VCM) komprimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="41d1d-117">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="41d1d-118">Wenn das Projekt als Ganzes mehr als 75 derartige Quellen enthält, müssen Sie auch die dynamische Neuverbindung verwenden, oder des kann das Projekt nicht in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="41d1d-118">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="41d1d-119">Weitere Informationen finden Sie unter " [**unenderengine:: setdynamikreconnectlevel**](irenderengine-setdynamicreconnectlevel.md)".</span><span class="sxs-lookup"><span data-stu-id="41d1d-119">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

 

<span data-ttu-id="41d1d-120">Weitere Informationen zu Quellen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="41d1d-120">For more information about sources, see [Working with Sources](working-with-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41d1d-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41d1d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41d1d-122">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="41d1d-122">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



