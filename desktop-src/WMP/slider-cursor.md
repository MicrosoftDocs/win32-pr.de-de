---
title: Schieberegler. Cursor
description: Das Cursor Attribut gibt einen Wert an, der angibt, welcher Cursor angezeigt wird, wenn sich der Mauszeiger über dem Schieberegler-Steuerelement befindet
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- Schieberegler. Cursor Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357945"
---
# <a name="slidercursor"></a><span data-ttu-id="e04ce-104">Schieberegler. Cursor</span><span class="sxs-lookup"><span data-stu-id="e04ce-104">SLIDER.cursor</span></span>

<span data-ttu-id="e04ce-105">Das **Cursor** Attribut gibt einen Wert an, der angibt, welcher Cursor angezeigt wird, wenn sich der Mauszeiger über dem Schieberegler-Steuerelement befindet</span><span class="sxs-lookup"><span data-stu-id="e04ce-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the slider control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="e04ce-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e04ce-106">Possible Values</span></span>

<span data-ttu-id="e04ce-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="e04ce-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="e04ce-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e04ce-108">Value</span></span>            | <span data-ttu-id="e04ce-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e04ce-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e04ce-110">System</span><span class="sxs-lookup"><span data-stu-id="e04ce-110">system</span></span>           | <span data-ttu-id="e04ce-111">Platt Form abhängiger Cursor (in der Regel ein Pfeil).</span><span class="sxs-lookup"><span data-stu-id="e04ce-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="e04ce-112">linken</span><span class="sxs-lookup"><span data-stu-id="e04ce-112">hand</span></span>             | <span data-ttu-id="e04ce-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="e04ce-113">Default.</span></span> <span data-ttu-id="e04ce-114">Linken.</span><span class="sxs-lookup"><span data-stu-id="e04ce-114">Hand.</span></span>                                                                              |
| <span data-ttu-id="e04ce-115">help</span><span class="sxs-lookup"><span data-stu-id="e04ce-115">help</span></span>             | <span data-ttu-id="e04ce-116">Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e04ce-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="e04ce-117">SizeAll</span><span class="sxs-lookup"><span data-stu-id="e04ce-117">sizeall</span></span>          | <span data-ttu-id="e04ce-118">Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04ce-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="e04ce-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="e04ce-119">sizenesw</span></span>         | <span data-ttu-id="e04ce-120">Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04ce-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="e04ce-121">SizeNS</span><span class="sxs-lookup"><span data-stu-id="e04ce-121">sizens</span></span>           | <span data-ttu-id="e04ce-122">Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04ce-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="e04ce-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="e04ce-123">sizenwse</span></span>         | <span data-ttu-id="e04ce-124">Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04ce-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="e04ce-125">SizeWE</span><span class="sxs-lookup"><span data-stu-id="e04ce-125">sizewe</span></span>           | <span data-ttu-id="e04ce-126">Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.</span><span class="sxs-lookup"><span data-stu-id="e04ce-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="e04ce-127">oben</span><span class="sxs-lookup"><span data-stu-id="e04ce-127">uparrow</span></span>          | <span data-ttu-id="e04ce-128">Vertikaler Pfeil nach oben.</span><span class="sxs-lookup"><span data-stu-id="e04ce-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="e04ce-129">\*. ani oder \* . cur</span><span class="sxs-lookup"><span data-stu-id="e04ce-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="e04ce-130">Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden).</span><span class="sxs-lookup"><span data-stu-id="e04ce-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e04ce-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e04ce-131">Requirements</span></span>



| <span data-ttu-id="e04ce-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e04ce-132">Requirement</span></span> | <span data-ttu-id="e04ce-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e04ce-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e04ce-134">Version</span><span class="sxs-lookup"><span data-stu-id="e04ce-134">Version</span></span><br/> | <span data-ttu-id="e04ce-135">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e04ce-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e04ce-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e04ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04ce-137">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="e04ce-137">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





