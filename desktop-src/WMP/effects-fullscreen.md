---
title: Effekte. Fullscreen
description: Das Fullscreen-Attribut gibt einen Wert an, der angibt, ob die aktuelle Visualisierung voll Bildschirm angezeigt wird, oder ruft diesen ab. Dieses Attribut kann nur zur Laufzeit festgelegt werden.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- Effekte. Fullscreen-Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362102"
---
# <a name="effectsfullscreen"></a><span data-ttu-id="b5d26-105">Effekte. Fullscreen</span><span class="sxs-lookup"><span data-stu-id="b5d26-105">EFFECTS.fullScreen</span></span>

<span data-ttu-id="b5d26-106">Das **Fullscreen** -Attribut gibt einen Wert an, der angibt, ob die aktuelle Visualisierung voll Bildschirm angezeigt wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="b5d26-106">The **fullScreen** attribute specifies or retrieves a value indicating whether the current visualization is displayed full-screen.</span></span> <span data-ttu-id="b5d26-107">Dieses Attribut kann nur zur Laufzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b5d26-107">This attribute can only be set at run time.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="b5d26-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b5d26-108">Possible Values</span></span>

<span data-ttu-id="b5d26-109">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b5d26-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b5d26-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b5d26-110">Value</span></span> | <span data-ttu-id="b5d26-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5d26-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="b5d26-112">true</span><span class="sxs-lookup"><span data-stu-id="b5d26-112">true</span></span>  | <span data-ttu-id="b5d26-113">Die Visualisierung wird voll Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5d26-113">Visualization is displayed full-screen.</span></span>              |
| <span data-ttu-id="b5d26-114">false</span><span class="sxs-lookup"><span data-stu-id="b5d26-114">false</span></span> | <span data-ttu-id="b5d26-115">Standard.</span><span class="sxs-lookup"><span data-stu-id="b5d26-115">Default.</span></span> <span data-ttu-id="b5d26-116">Die Visualisierung wird nicht im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5d26-116">Visualization is not displayed full-screen.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b5d26-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5d26-117">Remarks</span></span>

<span data-ttu-id="b5d26-118">Eine Visualisierung kann nur dann in den Vollbildmodus versetzt werden, wenn Medien wiedergegeben oder angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="b5d26-118">A visualization can be put into full-screen mode only while media is playing or paused.</span></span> <span data-ttu-id="b5d26-119">Wenn *Player*. **currentMedia** ist ein Video, ein Video-Plug-in muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b5d26-119">If *Player*.**currentMedia** is video, a video plug-in must be present.</span></span> <span data-ttu-id="b5d26-120">Wenn es sich um Audiodaten handelt, muss ein Visualisierungs-Plug-in vorhanden sein, das die voll Bild Anzeige unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5d26-120">If it is audio, a visualization plug-in that supports full-screen display must be present.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d26-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5d26-121">Requirements</span></span>



| <span data-ttu-id="b5d26-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5d26-122">Requirement</span></span> | <span data-ttu-id="b5d26-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b5d26-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b5d26-124">Version</span><span class="sxs-lookup"><span data-stu-id="b5d26-124">Version</span></span><br/> | <span data-ttu-id="b5d26-125">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b5d26-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5d26-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5d26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d26-127">**Effects-Element**</span><span class="sxs-lookup"><span data-stu-id="b5d26-127">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





