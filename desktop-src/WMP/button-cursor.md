---
title: Button. Cursor
description: Das Cursor Attribut gibt den Cursor an oder ruft ihn ab, der angezeigt wird, wenn der Mauszeiger über die Schaltfläche bewegt wird.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- Button. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356428"
---
# <a name="buttoncursor"></a><span data-ttu-id="f5c59-104">Button. Cursor</span><span class="sxs-lookup"><span data-stu-id="f5c59-104">BUTTON.cursor</span></span>

<span data-ttu-id="f5c59-105">Das **Cursor** Attribut gibt den Cursor an oder ruft ihn ab, der angezeigt wird, wenn der Mauszeiger über die **Schaltfläche** bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="f5c59-105">The **cursor** attribute specifies or retrieves the cursor that appears when the mouse pointer hovers over the **BUTTON**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="f5c59-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f5c59-106">Possible Values</span></span>

<span data-ttu-id="f5c59-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f5c59-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="f5c59-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f5c59-108">Value</span></span>            | <span data-ttu-id="f5c59-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5c59-109">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c59-110">System</span><span class="sxs-lookup"><span data-stu-id="f5c59-110">system</span></span>           | <span data-ttu-id="f5c59-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="f5c59-111">Default.</span></span> <span data-ttu-id="f5c59-112">Platt Form abhängiger Cursor (in der Regel ein Pfeil).</span><span class="sxs-lookup"><span data-stu-id="f5c59-112">Platform-dependent cursor (usually an arrow).</span></span>                                     |
| <span data-ttu-id="f5c59-113">linken</span><span class="sxs-lookup"><span data-stu-id="f5c59-113">hand</span></span>             | <span data-ttu-id="f5c59-114">Linken.</span><span class="sxs-lookup"><span data-stu-id="f5c59-114">Hand.</span></span>                                                                                      |
| <span data-ttu-id="f5c59-115">help</span><span class="sxs-lookup"><span data-stu-id="f5c59-115">help</span></span>             | <span data-ttu-id="f5c59-116">Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f5c59-116">Arrow with question mark indicating Help is available.</span></span>                                     |
| <span data-ttu-id="f5c59-117">SizeAll</span><span class="sxs-lookup"><span data-stu-id="f5c59-117">sizeall</span></span>          | <span data-ttu-id="f5c59-118">Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.</span><span class="sxs-lookup"><span data-stu-id="f5c59-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                  |
| <span data-ttu-id="f5c59-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="f5c59-119">sizenesw</span></span>         | <span data-ttu-id="f5c59-120">Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.</span><span class="sxs-lookup"><span data-stu-id="f5c59-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                     |
| <span data-ttu-id="f5c59-121">SizeNS</span><span class="sxs-lookup"><span data-stu-id="f5c59-121">sizens</span></span>           | <span data-ttu-id="f5c59-122">Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.</span><span class="sxs-lookup"><span data-stu-id="f5c59-122">Double-pointed arrow pointing north and south.</span></span>                                             |
| <span data-ttu-id="f5c59-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="f5c59-123">sizenwse</span></span>         | <span data-ttu-id="f5c59-124">Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.</span><span class="sxs-lookup"><span data-stu-id="f5c59-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                     |
| <span data-ttu-id="f5c59-125">SizeWE</span><span class="sxs-lookup"><span data-stu-id="f5c59-125">sizewe</span></span>           | <span data-ttu-id="f5c59-126">Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.</span><span class="sxs-lookup"><span data-stu-id="f5c59-126">Double-pointed arrow pointing west and east.</span></span>                                               |
| <span data-ttu-id="f5c59-127">oben</span><span class="sxs-lookup"><span data-stu-id="f5c59-127">uparrow</span></span>          | <span data-ttu-id="f5c59-128">Vertikaler Pfeil nach oben.</span><span class="sxs-lookup"><span data-stu-id="f5c59-128">Vertical arrow pointing upward.</span></span>                                                            |
| <span data-ttu-id="f5c59-129">\*. ani oder \* . cur</span><span class="sxs-lookup"><span data-stu-id="f5c59-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="f5c59-130">Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden)</span><span class="sxs-lookup"><span data-stu-id="f5c59-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f5c59-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5c59-131">Remarks</span></span>

<span data-ttu-id="f5c59-132">Wenn das System den angegebenen Cursor Wert nicht erkennt, verbleibt der Cursor Wert am zuvor festgelegten Wert.</span><span class="sxs-lookup"><span data-stu-id="f5c59-132">If the system does not recognize the cursor value specified, the cursor value remains at the previously set value.</span></span>

<span data-ttu-id="f5c59-133">Cursor-Dateinamen Pfade werden ignoriert, sodass sich die Cursor Datei im Standardverzeichnis befinden muss.</span><span class="sxs-lookup"><span data-stu-id="f5c59-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c59-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5c59-134">Requirements</span></span>



| <span data-ttu-id="f5c59-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5c59-135">Requirement</span></span> | <span data-ttu-id="f5c59-136">Wert</span><span class="sxs-lookup"><span data-stu-id="f5c59-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f5c59-137">Version</span><span class="sxs-lookup"><span data-stu-id="f5c59-137">Version</span></span><br/> | <span data-ttu-id="f5c59-138">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f5c59-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5c59-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5c59-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c59-140">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="f5c59-140">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





