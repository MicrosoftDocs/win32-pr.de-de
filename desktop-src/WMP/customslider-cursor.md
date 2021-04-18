---
title: Customslider. Cursor
description: Das Cursor Attribut gibt den Wert des Schieberegler-Steuerelement Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich die Maus über dem Schieberegler befindet.
ms.assetid: 965c21ab-18a0-4459-9d5b-0a35ea2c212f
keywords:
- Customslider. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e836dc7ec6efececf81789efe43d8b19d0df1783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354788"
---
# <a name="customslidercursor"></a><span data-ttu-id="7ecbf-104">Customslider. Cursor</span><span class="sxs-lookup"><span data-stu-id="7ecbf-104">CUSTOMSLIDER.cursor</span></span>

<span data-ttu-id="7ecbf-105">Das **Cursor** Attribut gibt den Wert des Schieberegler-Steuerelement Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich die Maus über dem Schieberegler befindet.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-105">The **cursor** attribute specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="7ecbf-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7ecbf-106">Possible Values</span></span>

<span data-ttu-id="7ecbf-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="7ecbf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7ecbf-108">Value</span></span>            | <span data-ttu-id="7ecbf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ecbf-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ecbf-110">System</span><span class="sxs-lookup"><span data-stu-id="7ecbf-110">system</span></span>           | <span data-ttu-id="7ecbf-111">Platt Form abhängiger Cursor (in der Regel ein Pfeil).</span><span class="sxs-lookup"><span data-stu-id="7ecbf-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="7ecbf-112">linken</span><span class="sxs-lookup"><span data-stu-id="7ecbf-112">hand</span></span>             | <span data-ttu-id="7ecbf-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-113">Default.</span></span> <span data-ttu-id="7ecbf-114">Der Cursor ist eine Hand.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-114">Cursor is a hand.</span></span>                                                                  |
| <span data-ttu-id="7ecbf-115">help</span><span class="sxs-lookup"><span data-stu-id="7ecbf-115">help</span></span>             | <span data-ttu-id="7ecbf-116">Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="7ecbf-117">SizeAll</span><span class="sxs-lookup"><span data-stu-id="7ecbf-117">sizeall</span></span>          | <span data-ttu-id="7ecbf-118">Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="7ecbf-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="7ecbf-119">sizenesw</span></span>         | <span data-ttu-id="7ecbf-120">Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="7ecbf-121">SizeNS</span><span class="sxs-lookup"><span data-stu-id="7ecbf-121">sizens</span></span>           | <span data-ttu-id="7ecbf-122">Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="7ecbf-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="7ecbf-123">sizenwse</span></span>         | <span data-ttu-id="7ecbf-124">Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="7ecbf-125">SizeWE</span><span class="sxs-lookup"><span data-stu-id="7ecbf-125">sizewe</span></span>           | <span data-ttu-id="7ecbf-126">Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="7ecbf-127">oben</span><span class="sxs-lookup"><span data-stu-id="7ecbf-127">uparrow</span></span>          | <span data-ttu-id="7ecbf-128">Vertikaler Pfeil nach oben.</span><span class="sxs-lookup"><span data-stu-id="7ecbf-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="7ecbf-129">\*. ani oder \* . cur</span><span class="sxs-lookup"><span data-stu-id="7ecbf-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="7ecbf-130">Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden).</span><span class="sxs-lookup"><span data-stu-id="7ecbf-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7ecbf-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ecbf-131">Requirements</span></span>



| <span data-ttu-id="7ecbf-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ecbf-132">Requirement</span></span> | <span data-ttu-id="7ecbf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7ecbf-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7ecbf-134">Version</span><span class="sxs-lookup"><span data-stu-id="7ecbf-134">Version</span></span><br/> | <span data-ttu-id="7ecbf-135">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7ecbf-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ecbf-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ecbf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ecbf-137">**Customslider-Element**</span><span class="sxs-lookup"><span data-stu-id="7ecbf-137">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





