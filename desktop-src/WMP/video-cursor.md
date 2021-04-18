---
title: Video. Cursor
description: Das Cursor Attribut gibt den Cursor Wert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft ihn ab.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- Video. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371227"
---
# <a name="videocursor"></a><span data-ttu-id="0d87a-104">Video. Cursor</span><span class="sxs-lookup"><span data-stu-id="0d87a-104">VIDEO.cursor</span></span>

<span data-ttu-id="0d87a-105">Das **Cursor** Attribut gibt den Cursor Wert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="0d87a-105">The **cursor** attribute specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="0d87a-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0d87a-106">Possible Values</span></span>

<span data-ttu-id="0d87a-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="0d87a-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="0d87a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0d87a-108">Value</span></span>            | <span data-ttu-id="0d87a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d87a-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d87a-110">System</span><span class="sxs-lookup"><span data-stu-id="0d87a-110">system</span></span>           | <span data-ttu-id="0d87a-111">Platt Form abhängiger Cursor (in der Regel ein Pfeil).</span><span class="sxs-lookup"><span data-stu-id="0d87a-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="0d87a-112">linken</span><span class="sxs-lookup"><span data-stu-id="0d87a-112">hand</span></span>             | <span data-ttu-id="0d87a-113">Linken.</span><span class="sxs-lookup"><span data-stu-id="0d87a-113">Hand.</span></span>                                                                                       |
| <span data-ttu-id="0d87a-114">help</span><span class="sxs-lookup"><span data-stu-id="0d87a-114">help</span></span>             | <span data-ttu-id="0d87a-115">Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0d87a-115">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="0d87a-116">SizeAll</span><span class="sxs-lookup"><span data-stu-id="0d87a-116">sizeall</span></span>          | <span data-ttu-id="0d87a-117">Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.</span><span class="sxs-lookup"><span data-stu-id="0d87a-117">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="0d87a-118">sizenesw</span><span class="sxs-lookup"><span data-stu-id="0d87a-118">sizenesw</span></span>         | <span data-ttu-id="0d87a-119">Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.</span><span class="sxs-lookup"><span data-stu-id="0d87a-119">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="0d87a-120">SizeNS</span><span class="sxs-lookup"><span data-stu-id="0d87a-120">sizens</span></span>           | <span data-ttu-id="0d87a-121">Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.</span><span class="sxs-lookup"><span data-stu-id="0d87a-121">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="0d87a-122">sizenwse</span><span class="sxs-lookup"><span data-stu-id="0d87a-122">sizenwse</span></span>         | <span data-ttu-id="0d87a-123">Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.</span><span class="sxs-lookup"><span data-stu-id="0d87a-123">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="0d87a-124">SizeWE</span><span class="sxs-lookup"><span data-stu-id="0d87a-124">sizewe</span></span>           | <span data-ttu-id="0d87a-125">Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.</span><span class="sxs-lookup"><span data-stu-id="0d87a-125">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="0d87a-126">oben</span><span class="sxs-lookup"><span data-stu-id="0d87a-126">uparrow</span></span>          | <span data-ttu-id="0d87a-127">Vertikaler Pfeil nach oben.</span><span class="sxs-lookup"><span data-stu-id="0d87a-127">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="0d87a-128">\*. ani oder \* . cur</span><span class="sxs-lookup"><span data-stu-id="0d87a-128">\*.ani or \*.cur</span></span> | <span data-ttu-id="0d87a-129">Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden).</span><span class="sxs-lookup"><span data-stu-id="0d87a-129">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0d87a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d87a-130">Remarks</span></span>

<span data-ttu-id="0d87a-131">Zu Renderingzwecken ist System der Standard Cursor.</span><span class="sxs-lookup"><span data-stu-id="0d87a-131">For rendering purposes, system is the default cursor.</span></span> <span data-ttu-id="0d87a-132">Der Standardwert, der von diesem Attribut abgerufen wird, ist "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="0d87a-132">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d87a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d87a-133">Requirements</span></span>



| <span data-ttu-id="0d87a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d87a-134">Requirement</span></span> | <span data-ttu-id="0d87a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0d87a-135">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0d87a-136">Version</span><span class="sxs-lookup"><span data-stu-id="0d87a-136">Version</span></span><br/> | <span data-ttu-id="0d87a-137">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0d87a-137">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d87a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d87a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d87a-139">**Video-Element**</span><span class="sxs-lookup"><span data-stu-id="0d87a-139">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





