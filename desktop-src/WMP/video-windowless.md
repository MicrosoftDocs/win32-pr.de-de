---
title: Video. Windows less
description: Mit dem Fenster "Windows less" wird ein Wert angegeben oder abgerufen, der angibt, ob das Video Steuerelement Fenster-oder fensterlose Fenster enthält. Das heißt, ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist oder abgeschnitten werden kann.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- Video. fensterlose Windows-Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370706"
---
# <a name="videowindowless"></a><span data-ttu-id="f1c6c-104">Video. Windows less</span><span class="sxs-lookup"><span data-stu-id="f1c6c-104">VIDEO.windowless</span></span>

<span data-ttu-id="f1c6c-105">Mit dem **Fenster "Windows less** " wird ein Wert angegeben oder abgerufen, der angibt, ob das Video Steuerelement Fenster-oder fensterlose Fenster enthält. Das heißt, ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist oder abgeschnitten werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-105">The **windowless** attribute specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="f1c6c-106">Kann nur zur Entwurfszeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-106">Can only be set at design time.</span></span>

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a><span data-ttu-id="f1c6c-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f1c6c-107">Possible Values</span></span>

<span data-ttu-id="f1c6c-108">Dieses Attribut ist ein **boolescher** Wert, der zur Entwurfszeit angegeben wird, und anschließend schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="f1c6c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="f1c6c-109">Value</span></span> | <span data-ttu-id="f1c6c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1c6c-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="f1c6c-111">true</span><span class="sxs-lookup"><span data-stu-id="f1c6c-111">true</span></span>  | <span data-ttu-id="f1c6c-112">Das Video Steuerelement ist fensterloser.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-112">Video control will be windowless.</span></span>        |
| <span data-ttu-id="f1c6c-113">false</span><span class="sxs-lookup"><span data-stu-id="f1c6c-113">false</span></span> | <span data-ttu-id="f1c6c-114">Standard.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-114">Default.</span></span> <span data-ttu-id="f1c6c-115">Das Video Steuerelement wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-115">Video control will be windowed.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f1c6c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1c6c-116">Remarks</span></span>

<span data-ttu-id="f1c6c-117">Wenn ein nicht rechteckiges Videofenster gewünscht ist oder wenn Sie einen Teil des Videofensters mit einem Bild abdecken möchten, muss dieses Attribut auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-117">If a non-rectangular video window is desired, or if you want to cover any part of the video window with an image, this attribute must be set to true.</span></span> <span data-ttu-id="f1c6c-118">Dadurch wird eine gewisse Leistung erzielt, um das erforderliche Clipping durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="f1c6c-119">Die Video Wiedergabe ist für die nicht geklickte Wiedergabe optimiert.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-119">Video playback is optimized for unclipped playback.</span></span> <span data-ttu-id="f1c6c-120">In diesem Fall wird das **fensterlose** Attribut auf false festgelegt, und das gesamte Video Rechteck wird immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-120">In this case, the **windowless** attribute is set to false, and the entire video rectangle is always displayed.</span></span> <span data-ttu-id="f1c6c-121">Alle Bilder, die das Videofenster abdecken, werden ignoriert, und das Videofenster hat die oberste z-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-121">Any image covering the video window is ignored, and the video window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1c6c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1c6c-122">Requirements</span></span>



| <span data-ttu-id="f1c6c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1c6c-123">Requirement</span></span> | <span data-ttu-id="f1c6c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f1c6c-124">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f1c6c-125">Version</span><span class="sxs-lookup"><span data-stu-id="f1c6c-125">Version</span></span><br/> | <span data-ttu-id="f1c6c-126">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f1c6c-126">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1c6c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1c6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c6c-128">**Video-Element**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-128">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





