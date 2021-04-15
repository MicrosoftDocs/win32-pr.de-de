---
description: Umschlag Segmente
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Umschlag Segmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521635"
---
# <a name="envelope-segments"></a><span data-ttu-id="fabac-103">Umschlag Segmente</span><span class="sxs-lookup"><span data-stu-id="fabac-103">Envelope Segments</span></span>

<span data-ttu-id="fabac-104">Eine Parameter Kurve besteht aus einem oder mehreren Umschlag Segmenten, die mithilfe der [**MP- \_ Umschlag \_ Segment**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) Struktur definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fabac-104">A parameter curve consists of one or more envelope segments, defined using the [**MP\_ENVELOPE\_SEGMENT**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) structure.</span></span> <span data-ttu-id="fabac-105">Diese Struktur enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="fabac-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="fabac-106">Die Start-und Endzeiten.</span><span class="sxs-lookup"><span data-stu-id="fabac-106">The start and end times.</span></span>
-   <span data-ttu-id="fabac-107">Die Anfangs-und Endwerte.</span><span class="sxs-lookup"><span data-stu-id="fabac-107">The starting and ending values.</span></span>
-   <span data-ttu-id="fabac-108">Der Kurven Typen (linear, Square usw.).</span><span class="sxs-lookup"><span data-stu-id="fabac-108">The curve type (linear, square, and so forth).</span></span>
-   <span data-ttu-id="fabac-109">Optionale Flags, die in Kürze beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fabac-109">Optional flags, described shortly.</span></span>

<span data-ttu-id="fabac-110">Der Client fügt einem Parameter Umschlag Segmente hinzu, indem er die [**imediaparams:: addenvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) -Methode aufrufen und ein Array von **MP- \_ Umschlag \_ Segment** Strukturen übergibt.</span><span class="sxs-lookup"><span data-stu-id="fabac-110">The client adds envelope segments to a parameter by calling the [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) method and passing in an array of **MP\_ENVELOPE\_SEGMENT** structures.</span></span> <span data-ttu-id="fabac-111">Der Client sollte die Segmente in aufsteigender Zeitreihen Folge sortieren, bevor die-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fabac-111">The client should sort the segments into ascending time order before calling the method.</span></span> <span data-ttu-id="fabac-112">Beim Verarbeiten von Daten durch DMO können Sie sich vorstellen, dass der Parameter über die einzelnen Umschlag Segmente hinausgeht, z. b. ein Auto, das eine Reihe von Hügeln steuert.</span><span class="sxs-lookup"><span data-stu-id="fabac-112">As the DMO processes data, you can imagine the parameter traveling over each envelope segment, like a car driving over a series of hills.</span></span> <span data-ttu-id="fabac-113">Die [**imediaparams:: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) -Methode gibt den letzten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fabac-113">The [**IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) method returns the most recent value.</span></span>

<span data-ttu-id="fabac-114">Zwei benachbarte Segmente können eine Lücke zwischen Ihnen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fabac-114">Two adjacent segments can have a gap between them.</span></span> <span data-ttu-id="fabac-115">Während der Lücken behält der-Parameter seinen vorherigen Wert wie folgt bei:</span><span class="sxs-lookup"><span data-stu-id="fabac-115">During gaps, the parameter retains its previous value, as follows:</span></span>

-   <span data-ttu-id="fabac-116">Vor dem ersten Segment ist der Wert der neutrale Wert.</span><span class="sxs-lookup"><span data-stu-id="fabac-116">Before the first segment, the value is the neutral value.</span></span>
-   <span data-ttu-id="fabac-117">Zwischen Segmenten ist der Wert der Endwert des vorherigen Segments.</span><span class="sxs-lookup"><span data-stu-id="fabac-117">Between segments, the value is the ending value of the previous segment.</span></span>
-   <span data-ttu-id="fabac-118">Nach dem letzten Segment verbleibt der Wert am Endwert dieses Segments.</span><span class="sxs-lookup"><span data-stu-id="fabac-118">After the last segment, the value remains at the ending value of that segment.</span></span>
-   <span data-ttu-id="fabac-119">Wenn der Client den DMO leert, wird der Wert auf den neutralen Wert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fabac-119">If the client flushes the DMO, the value reverts to the neutral value.</span></span>

<span data-ttu-id="fabac-120">Sie können ein Segment ändern, indem Sie eines der folgenden Flags festlegen:</span><span class="sxs-lookup"><span data-stu-id="fabac-120">You can alter a segment by setting either of the following flags:</span></span>

-   <span data-ttu-id="fabac-121">MPF- \_ VLP \_ Begin \_ CurrentVal.</span><span class="sxs-lookup"><span data-stu-id="fabac-121">MPF\_ENVLP\_BEGIN\_CURRENTVAL.</span></span> <span data-ttu-id="fabac-122">Der DMO verwendet den letzten Wert des-Parameters als Startwert für das Segment.</span><span class="sxs-lookup"><span data-stu-id="fabac-122">The DMO uses the most recent value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="fabac-123">Dies kann der neutrale Wert oder der Endwert des vorherigen Segments sein.</span><span class="sxs-lookup"><span data-stu-id="fabac-123">This might be the neutral value, or the ending value from the previous segment.</span></span> <span data-ttu-id="fabac-124">Der DMO ignoriert den **valstart** -Member der **MP- \_ Umschlag \_ Segment** Struktur.</span><span class="sxs-lookup"><span data-stu-id="fabac-124">The DMO ignores the **valStart** member of the **MP\_ENVELOPE\_SEGMENT** structure.</span></span>
-   <span data-ttu-id="fabac-125">MPF- \_ VLP \_ Begin \_ neutralval.</span><span class="sxs-lookup"><span data-stu-id="fabac-125">MPF\_ENVLP\_BEGIN\_NEUTRALVAL.</span></span> <span data-ttu-id="fabac-126">Der DMO verwendet den neutralen Wert des-Parameters als Startwert für das Segment.</span><span class="sxs-lookup"><span data-stu-id="fabac-126">The DMO uses the neutral value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="fabac-127">" **Valstart**" wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fabac-127">It ignores **valStart**.</span></span>

<span data-ttu-id="fabac-128">Sie können sich diese Flags vorstellen, wenn Sie den Startpunkt des Segments erfassen und nach oben oder unten verschieben, während der Endwert korrigiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="fabac-128">You can think of these flags as grabbing the starting point of the segment and moving it up or down, while the ending value remains fixed.</span></span> <span data-ttu-id="fabac-129">Das Segment wird entsprechend "gestreckt".</span><span class="sxs-lookup"><span data-stu-id="fabac-129">The segment will "stretch" accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fabac-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fabac-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fabac-131">Medien Parameter</span><span class="sxs-lookup"><span data-stu-id="fabac-131">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



