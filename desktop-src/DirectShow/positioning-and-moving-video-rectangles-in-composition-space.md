---
title: Positionieren und Verschieben von Videorechtecke im Kompositionsraum
description: Positionieren und Verschieben von Videorechtecke im Kompositionsraum
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909628"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="91c89-103">Positionieren und Verschieben von Videorechtecke im Kompositionsraum</span><span class="sxs-lookup"><span data-stu-id="91c89-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="91c89-104">Wenn der VMR mehrere Eingabedatenströme gemischt, positioniert er jeden Stream innerhalb eines normalisierten Rechtecks, das als "Kompositionsraum" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="91c89-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="91c89-105">Innerhalb des Kompositionsraums bilden die Koordinaten (0,0, 0,0) bis (1,0, 1,0) das sichtbare Videorechteck.</span><span class="sxs-lookup"><span data-stu-id="91c89-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="91c89-106">Alle Koordinaten, die außerhalb dieses Rechtecks liegen, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="91c89-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="91c89-107">Eine Anwendung kann Sondereffekte beim Verschieben, Strecken und Verkleinern des Videos aus einem Eingabestream ausführen, indem das Zielrechteck im Kompositionsraum für diesen Stream geändert wird.</span><span class="sxs-lookup"><span data-stu-id="91c89-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="91c89-108">Wenn das angegebene Rechteck eine andere Größe als das native Videorechteck hat, wird das native Video verkleinert oder gestreckt, damit es passt.</span><span class="sxs-lookup"><span data-stu-id="91c89-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="91c89-109">Das Zielrechteck wird durch Aufrufen der [**IVMRMixerControl::SetOutputRect-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) angegeben.</span><span class="sxs-lookup"><span data-stu-id="91c89-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="91c89-110">Angenommen, Stream 0 (entspricht Pin 0) enthält den Hauptvideostream, und Stream 1 (entspricht Pin 1) enthält ein sekundäres Video.</span><span class="sxs-lookup"><span data-stu-id="91c89-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="91c89-111">Stream 1 kann vollständig im Offscreen positioniert werden, indem ein normalisiertes Rechteck von { -1,0f, 0,0f, 0,0f, 1,0f } angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="91c89-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="91c89-112">Stream 1 kann dann in den sichtbaren Bereich verschoben werden, indem die linke und rechte Seite des Rechtecks bei nachfolgenden Aufrufen von **SetOutputRect geändert wird:**</span><span class="sxs-lookup"><span data-stu-id="91c89-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



| <span data-ttu-id="91c89-113">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="91c89-113">Label</span></span> | <span data-ttu-id="91c89-114">Wert</span><span class="sxs-lookup"><span data-stu-id="91c89-114">Value</span></span> |
|--------|-----------------------------|
| <span data-ttu-id="91c89-115">Zeit</span><span class="sxs-lookup"><span data-stu-id="91c89-115">Time</span></span>   | <span data-ttu-id="91c89-116">Rechteck</span><span class="sxs-lookup"><span data-stu-id="91c89-116">Rectangle</span></span>                   |
| <span data-ttu-id="91c89-117">t + 0</span><span class="sxs-lookup"><span data-stu-id="91c89-117">t + 0</span></span>  | <span data-ttu-id="91c89-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="91c89-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="91c89-119">t + 1</span><span class="sxs-lookup"><span data-stu-id="91c89-119">t + 1</span></span>  | <span data-ttu-id="91c89-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="91c89-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="91c89-121">t + 2</span><span class="sxs-lookup"><span data-stu-id="91c89-121">t + 2</span></span>  | <span data-ttu-id="91c89-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="91c89-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="91c89-123">...</span><span class="sxs-lookup"><span data-stu-id="91c89-123">...</span></span>    | <span data-ttu-id="91c89-124">...</span><span class="sxs-lookup"><span data-stu-id="91c89-124">...</span></span>                         |
| <span data-ttu-id="91c89-125">t + 10</span><span class="sxs-lookup"><span data-stu-id="91c89-125">t + 10</span></span> | <span data-ttu-id="91c89-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="91c89-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![Verschieben eines Videostreams im Kompositionsbereich](images/composition-space.png)

<span data-ttu-id="91c89-128">Zum Zeitpunkt t+10 ist das Video aus Stream 1 vollständig sichtbar.</span><span class="sxs-lookup"><span data-stu-id="91c89-128">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="91c89-129">In diesem Beispiel wurde die native Größe von Stream 1 beibehalten, während er verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="91c89-129">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="91c89-130">Sie können das Rechteck auch strecken oder verkleinern, um interessante Effekte zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="91c89-130">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="91c89-131">Sie können das Video auch vertikal drehen, indem Sie einen höheren Wert für den oberen als den unteren Wert angeben, oder das Video horizontal spiegeln, indem Sie einen höheren Wert für die linke als die rechte Seite angeben.</span><span class="sxs-lookup"><span data-stu-id="91c89-131">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91c89-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91c89-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91c89-133">Verwenden des VMR-Gemischtmodus</span><span class="sxs-lookup"><span data-stu-id="91c89-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



