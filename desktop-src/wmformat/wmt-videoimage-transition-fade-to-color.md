---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (wmsdkidl. h)
description: Der Übergang zwischen den Farben wird vom Bild zu einem Frame mit voll Tonfarbe aufgelöst.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369495"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a><span data-ttu-id="094bc-104">WMT \_ Videoimage \_ - \_ Übergang \_ in \_ Farbe ausblenden</span><span class="sxs-lookup"><span data-stu-id="094bc-104">WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR</span></span>

<span data-ttu-id="094bc-105">Der Übergang zwischen den Farben wird vom Bild zu einem Frame mit voll Tonfarbe aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="094bc-105">The fade-to-color transition dissolves from the image to a frame of solid color.</span></span>

## <a name="parameters"></a><span data-ttu-id="094bc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="094bc-106">Parameters</span></span>

<span data-ttu-id="094bc-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="094bc-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



| <span data-ttu-id="094bc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="094bc-108">Parameter</span></span>         | <span data-ttu-id="094bc-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="094bc-109">Structure member</span></span> | <span data-ttu-id="094bc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="094bc-110">Description</span></span>                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="094bc-111">Red</span><span class="sxs-lookup"><span data-stu-id="094bc-111">Red</span></span>               | <span data-ttu-id="094bc-112">**fEffectPara0**</span><span class="sxs-lookup"><span data-stu-id="094bc-112">**fEffectPara0**</span></span> | <span data-ttu-id="094bc-113">Roter Wert der Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="094bc-113">Red value of the background color.</span></span> <span data-ttu-id="094bc-114">Legen Sie auf eine Zahl zwischen 0 und 255 fest.</span><span class="sxs-lookup"><span data-stu-id="094bc-114">Set to a number between 0 and 255.</span></span>                                                                                                                                                     |
| <span data-ttu-id="094bc-115">Grün</span><span class="sxs-lookup"><span data-stu-id="094bc-115">Green</span></span>             | <span data-ttu-id="094bc-116">**fEffectPara1**</span><span class="sxs-lookup"><span data-stu-id="094bc-116">**fEffectPara1**</span></span> | <span data-ttu-id="094bc-117">Grüner Wert der Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="094bc-117">Green value of the background color.</span></span> <span data-ttu-id="094bc-118">Legen Sie auf eine Zahl zwischen 0 und 255 fest.</span><span class="sxs-lookup"><span data-stu-id="094bc-118">Set to a number between 0 and 255.</span></span>                                                                                                                                                   |
| <span data-ttu-id="094bc-119">Blau</span><span class="sxs-lookup"><span data-stu-id="094bc-119">Blue</span></span>              | <span data-ttu-id="094bc-120">**fEffectPara2**</span><span class="sxs-lookup"><span data-stu-id="094bc-120">**fEffectPara2**</span></span> | <span data-ttu-id="094bc-121">Der blaue Wert der Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="094bc-121">Blue value of the background color.</span></span> <span data-ttu-id="094bc-122">Legen Sie auf eine Zahl zwischen 0 und 255 fest.</span><span class="sxs-lookup"><span data-stu-id="094bc-122">Set to a number between 0 and 255.</span></span>                                                                                                                                                    |
| <span data-ttu-id="094bc-123">Hintergrund Gewichtung</span><span class="sxs-lookup"><span data-stu-id="094bc-123">Background weight</span></span> | <span data-ttu-id="094bc-124">**fEffectPara3**</span><span class="sxs-lookup"><span data-stu-id="094bc-124">**fEffectPara3**</span></span> | <span data-ttu-id="094bc-125">Gewichtung der Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="094bc-125">Weight of the background color.</span></span> <span data-ttu-id="094bc-126">Dieser Parameter gibt den Prozentsatz der Hintergrundfarbe in der Mischung als Dezimalwert an.</span><span class="sxs-lookup"><span data-stu-id="094bc-126">This parameter expresses the percentage of the background color in the mix as a decimal.</span></span> <span data-ttu-id="094bc-127">Um z. b. die Hintergrundfarbe um 30% zu mischen und das Bild 70% der Mischung zu erstellen, legen Sie auf 0,30 fest.</span><span class="sxs-lookup"><span data-stu-id="094bc-127">For example, to blend the background color at 30%, making the image 70% of the mix, set to 0.30.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="094bc-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="094bc-128">Requirements</span></span>



| <span data-ttu-id="094bc-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="094bc-129">Requirement</span></span> | <span data-ttu-id="094bc-130">Wert</span><span class="sxs-lookup"><span data-stu-id="094bc-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="094bc-131">Header</span><span class="sxs-lookup"><span data-stu-id="094bc-131">Header</span></span><br/> | <dl> <span data-ttu-id="094bc-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="094bc-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="094bc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="094bc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094bc-134">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="094bc-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





