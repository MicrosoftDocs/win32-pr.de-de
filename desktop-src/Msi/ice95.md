---
description: ICE95 überprüft die Tabelle "Control Table" und die Tabelle "bbcontrol", um zu überprüfen, ob die Billboard-Steuerelemente auf alle
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217649"
---
# <a name="ice95"></a><span data-ttu-id="44454-103">ICE95</span><span class="sxs-lookup"><span data-stu-id="44454-103">ICE95</span></span>

<span data-ttu-id="44454-104">ICE95 überprüft die Tabelle " [Control Table](control-table.md) " und die [Tabelle "bbcontrol](bbcontrol-table.md) ", um zu überprüfen, ob die Billboard-Steuerelemente auf alle</span><span class="sxs-lookup"><span data-stu-id="44454-104">ICE95 checks the [Control table](control-table.md) and [BBControl table](bbcontrol-table.md) to verify that the billboard controls fit onto all the billboards.</span></span>

## <a name="result"></a><span data-ttu-id="44454-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="44454-105">Result</span></span>

<span data-ttu-id="44454-106">Wenn einer der folgenden Punkte zutrifft, kann ein Billboard-Steuerelement nicht in ein Plakat eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="44454-106">If any of the following are true, a billboard control fails to fit on a billboard.</span></span> <span data-ttu-id="44454-107">ICE95 gibt die folgenden Warnungen aus.</span><span class="sxs-lookup"><span data-stu-id="44454-107">ICE95 posts the following warnings.</span></span>



| <span data-ttu-id="44454-108">ICE95-Warnung</span><span class="sxs-lookup"><span data-stu-id="44454-108">ICE95 warning</span></span>                                                                                                                                                                                                              | <span data-ttu-id="44454-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44454-109">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="44454-110">Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt.</span><span class="sxs-lookup"><span data-stu-id="44454-110">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="44454-111">Die X-Koordinate überschreitet die Grenze der Mindestbreite des Billboard-Steuer Elements% s.</span><span class="sxs-lookup"><span data-stu-id="44454-111">The X coordinate exceeds the boundary of the minimum billboard control width %s</span></span>                   | <span data-ttu-id="44454-112">Die X-Koordinate des Steuer Elements liegt außerhalb der Breite des Billboard.</span><span class="sxs-lookup"><span data-stu-id="44454-112">The control's X coordinate is outside the width of the billboard.</span></span>                          |
| <span data-ttu-id="44454-113">Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt.</span><span class="sxs-lookup"><span data-stu-id="44454-113">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="44454-114">Die Y-Koordinate überschreitet die Grenze der minimalen Größe des Billboard-Steuer Elements% s.</span><span class="sxs-lookup"><span data-stu-id="44454-114">The Y coordinate exceeds the boundary of the minimum billboard control height %s</span></span>                  | <span data-ttu-id="44454-115">Die Y-Koordinate des Steuer Elements befindet sich unter dem unteren Rand des Billboard.</span><span class="sxs-lookup"><span data-stu-id="44454-115">The control's Y coordinate is below the bottom of the billboard.</span></span>                           |
| <span data-ttu-id="44454-116">Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt.</span><span class="sxs-lookup"><span data-stu-id="44454-116">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="44454-117">Die X-Koordinate und die zusammen kombinierte Breite überschreiten die Mindestbreite des Billboard-Steuer Elements% s.</span><span class="sxs-lookup"><span data-stu-id="44454-117">The X coordinate and the width combined together exceeds the minimum billboard control width %s</span></span>   | <span data-ttu-id="44454-118">Die X-Koordinate des Steuer Elements und die Breite des Steuer Elements liegen außerhalb der Breite des Billboard.</span><span class="sxs-lookup"><span data-stu-id="44454-118">The control's X coordinate plus the control's width is outside the width of the billboard.</span></span> |
| <span data-ttu-id="44454-119">Das bbcontrol-Element ' \[ 1 \] . \[ 2 \] ' in der Tabelle ' bbcontrol ' ist nicht in alle Billboard-Steuerelemente in der Steuerelement Tabelle passt.</span><span class="sxs-lookup"><span data-stu-id="44454-119">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="44454-120">Die Y-Koordinate und die kombinierte Höhe überschreiten die minimale Größe des Billboard-Steuer Elements% s.</span><span class="sxs-lookup"><span data-stu-id="44454-120">The Y coordinate and the height combined together exceeds the minimum billboard control height %s</span></span> | <span data-ttu-id="44454-121">Die Y-Koordinate des Steuer Elements und die Höhe des Steuer Elements liegen unter dem unteren Rand des Billboard.</span><span class="sxs-lookup"><span data-stu-id="44454-121">The control's Y coordinate plus the control's height is below the bottom of the billboard.</span></span> |



 

## <a name="example"></a><span data-ttu-id="44454-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="44454-122">Example</span></span>

<span data-ttu-id="44454-123">ICE95 meldet die folgenden Warnungen für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="44454-123">ICE95 reports the following warnings for the example:</span></span>

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

<span data-ttu-id="44454-124">Control-Tabelle (partiell) (partiell)</span><span class="sxs-lookup"><span data-stu-id="44454-124">Control Table (partial) (partial)</span></span>



| <span data-ttu-id="44454-125">Control</span><span class="sxs-lookup"><span data-stu-id="44454-125">Control</span></span>  | <span data-ttu-id="44454-126">type</span><span class="sxs-lookup"><span data-stu-id="44454-126">Type</span></span>      | <span data-ttu-id="44454-127">Breite</span><span class="sxs-lookup"><span data-stu-id="44454-127">Width</span></span> | <span data-ttu-id="44454-128">Höhe</span><span class="sxs-lookup"><span data-stu-id="44454-128">Height</span></span> |
|----------|-----------|-------|--------|
| <span data-ttu-id="44454-129">control1</span><span class="sxs-lookup"><span data-stu-id="44454-129">control1</span></span> | <span data-ttu-id="44454-130">Billboard</span><span class="sxs-lookup"><span data-stu-id="44454-130">Billboard</span></span> | <span data-ttu-id="44454-131">300</span><span class="sxs-lookup"><span data-stu-id="44454-131">300</span></span>   | <span data-ttu-id="44454-132">100</span><span class="sxs-lookup"><span data-stu-id="44454-132">100</span></span>    |
| <span data-ttu-id="44454-133">Control2</span><span class="sxs-lookup"><span data-stu-id="44454-133">Control2</span></span> | <span data-ttu-id="44454-134">Billboard</span><span class="sxs-lookup"><span data-stu-id="44454-134">Billboard</span></span> | <span data-ttu-id="44454-135">100</span><span class="sxs-lookup"><span data-stu-id="44454-135">100</span></span>   | <span data-ttu-id="44454-136">300</span><span class="sxs-lookup"><span data-stu-id="44454-136">300</span></span>    |



 

[<span data-ttu-id="44454-137">Bbcontrol-Tabelle</span><span class="sxs-lookup"><span data-stu-id="44454-137">BBControl table</span></span>](bbcontrol-table.md)



| <span data-ttu-id="44454-138">Billboard\_</span><span class="sxs-lookup"><span data-stu-id="44454-138">Billboard\_</span></span> | <span data-ttu-id="44454-139">Bbcontrol</span><span class="sxs-lookup"><span data-stu-id="44454-139">BBControl</span></span>  | <span data-ttu-id="44454-140">X</span><span class="sxs-lookup"><span data-stu-id="44454-140">X</span></span>   | <span data-ttu-id="44454-141">J</span><span class="sxs-lookup"><span data-stu-id="44454-141">Y</span></span>   | <span data-ttu-id="44454-142">Breite</span><span class="sxs-lookup"><span data-stu-id="44454-142">Width</span></span> | <span data-ttu-id="44454-143">Höhe</span><span class="sxs-lookup"><span data-stu-id="44454-143">Height</span></span> |
|-------------|------------|-----|-----|-------|--------|
| <span data-ttu-id="44454-144">billboard1</span><span class="sxs-lookup"><span data-stu-id="44454-144">billboard1</span></span>  | <span data-ttu-id="44454-145">bbcontrol1</span><span class="sxs-lookup"><span data-stu-id="44454-145">bbcontrol1</span></span> | <span data-ttu-id="44454-146">200</span><span class="sxs-lookup"><span data-stu-id="44454-146">200</span></span> | <span data-ttu-id="44454-147">0</span><span class="sxs-lookup"><span data-stu-id="44454-147">0</span></span>   | <span data-ttu-id="44454-148">100</span><span class="sxs-lookup"><span data-stu-id="44454-148">100</span></span>   | <span data-ttu-id="44454-149">100</span><span class="sxs-lookup"><span data-stu-id="44454-149">100</span></span>    |
| <span data-ttu-id="44454-150">billboard1</span><span class="sxs-lookup"><span data-stu-id="44454-150">billboard1</span></span>  | <span data-ttu-id="44454-151">bbcontrol2</span><span class="sxs-lookup"><span data-stu-id="44454-151">bbcontrol2</span></span> | <span data-ttu-id="44454-152">0</span><span class="sxs-lookup"><span data-stu-id="44454-152">0</span></span>   | <span data-ttu-id="44454-153">200</span><span class="sxs-lookup"><span data-stu-id="44454-153">200</span></span> | <span data-ttu-id="44454-154">100</span><span class="sxs-lookup"><span data-stu-id="44454-154">100</span></span>   | <span data-ttu-id="44454-155">100</span><span class="sxs-lookup"><span data-stu-id="44454-155">100</span></span>    |
| <span data-ttu-id="44454-156">billboard1</span><span class="sxs-lookup"><span data-stu-id="44454-156">billboard1</span></span>  | <span data-ttu-id="44454-157">bbcontrol3</span><span class="sxs-lookup"><span data-stu-id="44454-157">bbcontrol3</span></span> | <span data-ttu-id="44454-158">50</span><span class="sxs-lookup"><span data-stu-id="44454-158">50</span></span>  | <span data-ttu-id="44454-159">0</span><span class="sxs-lookup"><span data-stu-id="44454-159">0</span></span>   | <span data-ttu-id="44454-160">100</span><span class="sxs-lookup"><span data-stu-id="44454-160">100</span></span>   | <span data-ttu-id="44454-161">50</span><span class="sxs-lookup"><span data-stu-id="44454-161">50</span></span>     |
| <span data-ttu-id="44454-162">billboard1</span><span class="sxs-lookup"><span data-stu-id="44454-162">billboard1</span></span>  | <span data-ttu-id="44454-163">bbcontrol4</span><span class="sxs-lookup"><span data-stu-id="44454-163">bbcontrol4</span></span> | <span data-ttu-id="44454-164">0</span><span class="sxs-lookup"><span data-stu-id="44454-164">0</span></span>   | <span data-ttu-id="44454-165">50</span><span class="sxs-lookup"><span data-stu-id="44454-165">50</span></span>  | <span data-ttu-id="44454-166">50</span><span class="sxs-lookup"><span data-stu-id="44454-166">50</span></span>    | <span data-ttu-id="44454-167">100</span><span class="sxs-lookup"><span data-stu-id="44454-167">100</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="44454-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44454-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44454-169">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="44454-169">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



