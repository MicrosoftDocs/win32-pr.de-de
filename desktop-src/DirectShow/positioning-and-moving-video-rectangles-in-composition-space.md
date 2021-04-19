---
title: Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich
description: Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345400"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="3c131-103">Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich</span><span class="sxs-lookup"><span data-stu-id="3c131-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="3c131-104">Wenn der VMR mehrere Eingabedaten Ströme mischt, positioniert er jeden Stream innerhalb eines normalisierten Rechtecks, das als "Kompositions Raum" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3c131-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="3c131-105">Innerhalb des Kompositions Raums bilden die Koordinaten (0,0, 0,0) bis (1,0, 1,0) das sichtbare Video Rechteck.</span><span class="sxs-lookup"><span data-stu-id="3c131-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="3c131-106">Alle Koordinaten, die außerhalb dieses Rechtecks liegen, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="3c131-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="3c131-107">Eine Anwendung kann besondere Effekte durch das Verschieben, Strecken und Verkleinern des Videos aus einem Eingabestream durch Ändern des Ziel Rechtecks im Kompositions Raum für diesen Stream durchführen.</span><span class="sxs-lookup"><span data-stu-id="3c131-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="3c131-108">Wenn das angegebene Rechteck eine andere Größe hat als das systemeigene Video Rechteck, wird das native Video verkleinert oder gestreckt.</span><span class="sxs-lookup"><span data-stu-id="3c131-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="3c131-109">Das Ziel Rechteck wird durch Aufrufen der [**ivmrmixercontrol:: setoutputrect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) -Methode angegeben.</span><span class="sxs-lookup"><span data-stu-id="3c131-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="3c131-110">Nehmen wir beispielsweise an, dass Stream 0 (entspricht Pin 0) den hauptvideostream enthält, und Stream 1 (entspricht Pin 1) enthält ein sekundäres Video.</span><span class="sxs-lookup"><span data-stu-id="3c131-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="3c131-111">Stream 1 kann durch Angabe eines normalisierten Rechtecks ({-1.0 f, 0,0 f, 0,0 f, 1.0 f}) vollständig ausgelagert werden.</span><span class="sxs-lookup"><span data-stu-id="3c131-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="3c131-112">Stream 1 kann dann in den sichtbaren Bereich verschoben werden, indem die linke und die Rechte Seite des Rechtecks bei aufeinander folgenden Aufrufen von **setoutputrect** geändert werden:</span><span class="sxs-lookup"><span data-stu-id="3c131-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



|        |                             |
|--------|-----------------------------|
| <span data-ttu-id="3c131-113">Time</span><span class="sxs-lookup"><span data-stu-id="3c131-113">Time</span></span>   | <span data-ttu-id="3c131-114">Rechteck</span><span class="sxs-lookup"><span data-stu-id="3c131-114">Rectangle</span></span>                   |
| <span data-ttu-id="3c131-115">t + 0</span><span class="sxs-lookup"><span data-stu-id="3c131-115">t + 0</span></span>  | <span data-ttu-id="3c131-116">{-1.0 f, 0,0 f, 0,0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="3c131-116">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="3c131-117">t + 1</span><span class="sxs-lookup"><span data-stu-id="3c131-117">t + 1</span></span>  | <span data-ttu-id="3c131-118">{-0.9 f, 0,0 f, 0,1 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="3c131-118">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="3c131-119">t + 2</span><span class="sxs-lookup"><span data-stu-id="3c131-119">t + 2</span></span>  | <span data-ttu-id="3c131-120">{-0,8 f, 0,0 f, 0,2 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="3c131-120">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="3c131-121">...</span><span class="sxs-lookup"><span data-stu-id="3c131-121">...</span></span>    | <span data-ttu-id="3c131-122">...</span><span class="sxs-lookup"><span data-stu-id="3c131-122">...</span></span>                         |
| <span data-ttu-id="3c131-123">t + 10</span><span class="sxs-lookup"><span data-stu-id="3c131-123">t + 10</span></span> | <span data-ttu-id="3c131-124">{0,0 f, 0,0 f, 1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="3c131-124">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![Verschieben eines Videodaten Stroms im Kompositions Bereich](images/composition-space.png)

<span data-ttu-id="3c131-126">Zum Zeitpunkt t + 10 ist das Video aus Stream 1 vollständig sichtbar.</span><span class="sxs-lookup"><span data-stu-id="3c131-126">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="3c131-127">In diesem Beispiel wurde die systemeigene Größe von Stream 1 während der Verschiebung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="3c131-127">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="3c131-128">Sie können das Rechteck auch Strecken oder verkleinern, um interessante Effekte zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="3c131-128">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="3c131-129">Sie können das Video auch vertikal kippen, indem Sie einen größeren Wert für den oberen als den unteren Wert angeben oder das Video horizontal spiegeln, indem Sie einen größeren Wert für Links als die Rechte angeben.</span><span class="sxs-lookup"><span data-stu-id="3c131-129">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c131-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c131-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c131-131">Verwenden des VMR-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="3c131-131">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



