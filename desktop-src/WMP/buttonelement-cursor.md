---
title: ButtonElement. Cursor
description: Das Cursor Attribut gibt den Wert des ButtonElement-Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über dem ButtonElement befindet.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- ButtonElement. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374035"
---
# <a name="buttonelementcursor"></a><span data-ttu-id="111c0-104">ButtonElement. Cursor</span><span class="sxs-lookup"><span data-stu-id="111c0-104">BUTTONELEMENT.cursor</span></span>

<span data-ttu-id="111c0-105">Das **Cursor** Attribut gibt den Wert des **ButtonElement** -Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über dem **ButtonElement** befindet.</span><span class="sxs-lookup"><span data-stu-id="111c0-105">The **cursor** attribute specifies or retrieves the value of the **BUTTONELEMENT** cursor that appears when the mouse is over the **BUTTONELEMENT**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="111c0-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="111c0-106">Possible Values</span></span>

<span data-ttu-id="111c0-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="111c0-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="111c0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="111c0-108">Value</span></span>            | <span data-ttu-id="111c0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="111c0-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="111c0-110">System</span><span class="sxs-lookup"><span data-stu-id="111c0-110">system</span></span>           | <span data-ttu-id="111c0-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="111c0-111">Default.</span></span> <span data-ttu-id="111c0-112">Platt Form abhängiger Cursor (in der Regel ein Pfeil).</span><span class="sxs-lookup"><span data-stu-id="111c0-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="111c0-113">linken</span><span class="sxs-lookup"><span data-stu-id="111c0-113">hand</span></span>             | <span data-ttu-id="111c0-114">Linken.</span><span class="sxs-lookup"><span data-stu-id="111c0-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="111c0-115">help</span><span class="sxs-lookup"><span data-stu-id="111c0-115">help</span></span>             | <span data-ttu-id="111c0-116">Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="111c0-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="111c0-117">SizeAll</span><span class="sxs-lookup"><span data-stu-id="111c0-117">sizeall</span></span>          | <span data-ttu-id="111c0-118">Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.</span><span class="sxs-lookup"><span data-stu-id="111c0-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="111c0-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="111c0-119">sizenesw</span></span>         | <span data-ttu-id="111c0-120">Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.</span><span class="sxs-lookup"><span data-stu-id="111c0-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="111c0-121">SizeNS</span><span class="sxs-lookup"><span data-stu-id="111c0-121">sizens</span></span>           | <span data-ttu-id="111c0-122">Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.</span><span class="sxs-lookup"><span data-stu-id="111c0-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="111c0-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="111c0-123">sizenwse</span></span>         | <span data-ttu-id="111c0-124">Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.</span><span class="sxs-lookup"><span data-stu-id="111c0-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="111c0-125">SizeWE</span><span class="sxs-lookup"><span data-stu-id="111c0-125">sizewe</span></span>           | <span data-ttu-id="111c0-126">Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.</span><span class="sxs-lookup"><span data-stu-id="111c0-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="111c0-127">oben</span><span class="sxs-lookup"><span data-stu-id="111c0-127">uparrow</span></span>          | <span data-ttu-id="111c0-128">Vertikaler Pfeil nach oben.</span><span class="sxs-lookup"><span data-stu-id="111c0-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="111c0-129">\*. ani oder \* . cur</span><span class="sxs-lookup"><span data-stu-id="111c0-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="111c0-130">Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden).</span><span class="sxs-lookup"><span data-stu-id="111c0-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="111c0-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="111c0-131">Remarks</span></span>

<span data-ttu-id="111c0-132">Wenn ein ungültiger Wert angegeben wird, wird der vorherige Wert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="111c0-132">If an invalid value is specified, the previous value is maintained.</span></span>

<span data-ttu-id="111c0-133">Cursor-Dateinamen Pfade werden ignoriert, sodass sich die Cursor Datei im Standardverzeichnis befinden muss.</span><span class="sxs-lookup"><span data-stu-id="111c0-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="111c0-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="111c0-134">Requirements</span></span>



| <span data-ttu-id="111c0-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="111c0-135">Requirement</span></span> | <span data-ttu-id="111c0-136">Wert</span><span class="sxs-lookup"><span data-stu-id="111c0-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="111c0-137">Version</span><span class="sxs-lookup"><span data-stu-id="111c0-137">Version</span></span><br/> | <span data-ttu-id="111c0-138">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="111c0-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="111c0-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="111c0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111c0-140">**ButtonElement-Element**</span><span class="sxs-lookup"><span data-stu-id="111c0-140">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> </dl>

 

 





