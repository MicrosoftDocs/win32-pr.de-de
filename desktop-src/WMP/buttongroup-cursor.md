---
title: ButtonGroup. Cursor
description: Das Cursor Attribut gibt den Typ des Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich die Maus über einer Schaltfläche in der ButtonGroup befindet.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- ButtonGroup. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371186"
---
# <a name="buttongroupcursor"></a><span data-ttu-id="9b453-104">ButtonGroup. Cursor</span><span class="sxs-lookup"><span data-stu-id="9b453-104">BUTTONGROUP.cursor</span></span>

<span data-ttu-id="9b453-105">Das **Cursor** Attribut gibt den Typ des Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich die Maus über einer Schaltfläche in der **ButtonGroup** befindet.</span><span class="sxs-lookup"><span data-stu-id="9b453-105">The **cursor** attribute specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="9b453-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="9b453-106">Possible Values</span></span>

<span data-ttu-id="9b453-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="9b453-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="9b453-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9b453-108">Value</span></span>            | <span data-ttu-id="9b453-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b453-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b453-110">System</span><span class="sxs-lookup"><span data-stu-id="9b453-110">system</span></span>           | <span data-ttu-id="9b453-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="9b453-111">Default.</span></span> <span data-ttu-id="9b453-112">Platt Form abhängiger Cursor (in der Regel ein Pfeil).</span><span class="sxs-lookup"><span data-stu-id="9b453-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="9b453-113">linken</span><span class="sxs-lookup"><span data-stu-id="9b453-113">hand</span></span>             | <span data-ttu-id="9b453-114">Linken.</span><span class="sxs-lookup"><span data-stu-id="9b453-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="9b453-115">help</span><span class="sxs-lookup"><span data-stu-id="9b453-115">help</span></span>             | <span data-ttu-id="9b453-116">Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9b453-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="9b453-117">SizeAll</span><span class="sxs-lookup"><span data-stu-id="9b453-117">sizeall</span></span>          | <span data-ttu-id="9b453-118">Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b453-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="9b453-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="9b453-119">sizenesw</span></span>         | <span data-ttu-id="9b453-120">Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b453-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="9b453-121">SizeNS</span><span class="sxs-lookup"><span data-stu-id="9b453-121">sizens</span></span>           | <span data-ttu-id="9b453-122">Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b453-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="9b453-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="9b453-123">sizenwse</span></span>         | <span data-ttu-id="9b453-124">Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b453-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="9b453-125">SizeWE</span><span class="sxs-lookup"><span data-stu-id="9b453-125">sizewe</span></span>           | <span data-ttu-id="9b453-126">Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.</span><span class="sxs-lookup"><span data-stu-id="9b453-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="9b453-127">oben</span><span class="sxs-lookup"><span data-stu-id="9b453-127">uparrow</span></span>          | <span data-ttu-id="9b453-128">Vertikaler Pfeil nach oben.</span><span class="sxs-lookup"><span data-stu-id="9b453-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="9b453-129">\*. ani oder \* . cur</span><span class="sxs-lookup"><span data-stu-id="9b453-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="9b453-130">Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden).</span><span class="sxs-lookup"><span data-stu-id="9b453-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9b453-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b453-131">Remarks</span></span>

<span data-ttu-id="9b453-132">Der angegebene Cursor gilt für alle Schaltflächen in der **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="9b453-132">The cursor specified applies to all buttons in the **BUTTONGROUP**.</span></span>

<span data-ttu-id="9b453-133">Wenn Sie einen ungültigen Cursor Wert angeben, verbleibt er am zuvor festgelegten Wert.</span><span class="sxs-lookup"><span data-stu-id="9b453-133">If you specify an invalid cursor value, it remains at the previously set value.</span></span>

<span data-ttu-id="9b453-134">Cursor-Dateinamen Pfade werden ignoriert, sodass sich die Cursor Datei im Standardverzeichnis befinden muss.</span><span class="sxs-lookup"><span data-stu-id="9b453-134">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b453-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b453-135">Requirements</span></span>



| <span data-ttu-id="9b453-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b453-136">Requirement</span></span> | <span data-ttu-id="9b453-137">Wert</span><span class="sxs-lookup"><span data-stu-id="9b453-137">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9b453-138">Version</span><span class="sxs-lookup"><span data-stu-id="9b453-138">Version</span></span><br/> | <span data-ttu-id="9b453-139">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9b453-139">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b453-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b453-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b453-141">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="9b453-141">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





