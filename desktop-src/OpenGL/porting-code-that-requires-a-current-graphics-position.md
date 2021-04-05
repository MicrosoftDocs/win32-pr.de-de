---
title: Port Code, der eine aktuelle Grafik Position benötigt
description: OpenGL behält keine aktuelle Grafik Position bei. IRIS GL-Funktionen, die von der aktuellen Grafik Position abhängig sind, z. b. Move, Draw und RMV, haben keine Entsprechungen in OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- IRIS GL portieren, aktuelle Grafik Position
- Portieren von IRIS GL, aktuelle Grafik Position
- Portieren auf OpenGL von IRIS GL, aktueller Grafik Position
- OpenGL-Portierung von IRIS GL, aktuelle Grafik Position
- aktuelle Grafik Position
- Raster Positionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "103719596"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a><span data-ttu-id="0854f-110">Port Code, der eine aktuelle Grafik Position benötigt</span><span class="sxs-lookup"><span data-stu-id="0854f-110">Port code that needs a current graphics position</span></span>

<span data-ttu-id="0854f-111">OpenGL behält keine aktuelle Grafik Position bei.</span><span class="sxs-lookup"><span data-stu-id="0854f-111">OpenGL does not maintain a current graphics position.</span></span> <span data-ttu-id="0854f-112">IRIS GL-Funktionen, die von der aktuellen Grafik Position abhängig sind, z. b. **Move**, **Draw** und **RMV**, haben keine Entsprechungen in OpenGL.</span><span class="sxs-lookup"><span data-stu-id="0854f-112">IRIS GL functions that depend on the current graphics position, such as **move**, **draw**, and **rmv**, have no equivalents in OpenGL.</span></span>

<span data-ttu-id="0854f-113">Ältere Versionen von IRIS GL enthielten Zeichnungs Befehle, die auf der aktuellen Grafik Position beruhten, obwohl ihre Verwendung davon abgeraten ist.</span><span class="sxs-lookup"><span data-stu-id="0854f-113">Older versions of IRIS GL included drawing commands that relied upon the current graphics position, though their use has been discouraged.</span></span> <span data-ttu-id="0854f-114">Sie müssen Ihren Code umschreiben, wenn Sie die aktuelle Grafik Position in irgendeiner Weise verwendet haben, oder eine der folgenden Routinen verwendet haben:</span><span class="sxs-lookup"><span data-stu-id="0854f-114">You will need to rewrite your code if you relied on the current graphics position in any way, or used any of the following routines:</span></span>

-   <span data-ttu-id="0854f-115">**Zeichnen** und **verschieben**</span><span class="sxs-lookup"><span data-stu-id="0854f-115">**draw** and **move**</span></span>
-   <span data-ttu-id="0854f-116">**pmv**, **PDR** und **PCLOS**</span><span class="sxs-lookup"><span data-stu-id="0854f-116">**pmv**, **pdr**, and **pclos**</span></span>
-   <span data-ttu-id="0854f-117">**rdr**, **RMV**, **rpdr** und **rpmv**</span><span class="sxs-lookup"><span data-stu-id="0854f-117">**rdr**, **rmv**, **rpdr**, and **rpmv**</span></span>
-   <span data-ttu-id="0854f-118">**getgpos**</span><span class="sxs-lookup"><span data-stu-id="0854f-118">**getgpos**</span></span>

<span data-ttu-id="0854f-119">OpenGL hat ein Konzept der Raster Position, das der aktuellen Zeichenposition von IRIS GL entspricht.</span><span class="sxs-lookup"><span data-stu-id="0854f-119">OpenGL has a concept of raster position that corresponds to IRIS GL's current character position.</span></span> <span data-ttu-id="0854f-120">Weitere Informationen zur Raster Positionierung finden Sie unter [Portieren von Pixel Vorgängen](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="0854f-120">For more information on raster positioning, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="0854f-121">Dieses Thema enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="0854f-121">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="0854f-122">Portieren von Bildschirm-und Puffer Lösch Befehlen</span><span class="sxs-lookup"><span data-stu-id="0854f-122">Porting Screen and Buffer Clearing Commands</span></span>](porting-screen-and-buffer-clearing-commands.md)
-   [<span data-ttu-id="0854f-123">Portieren von Matrix-und Transformations Funktionen</span><span class="sxs-lookup"><span data-stu-id="0854f-123">Porting Matrix and Transformation Functions</span></span>](porting-matrix-and-transformation-functions.md)
-   [<span data-ttu-id="0854f-124">Portieren von Code im msingle-Modus</span><span class="sxs-lookup"><span data-stu-id="0854f-124">Porting MSINGLE Mode Code</span></span>](porting-msingle-mode-code.md)
-   [<span data-ttu-id="0854f-125">Portieren von Funktionen, die Matrizen und Transformationen erhalten</span><span class="sxs-lookup"><span data-stu-id="0854f-125">Porting Functions that Get Matrices and Transformations</span></span>](porting-functions-that-get-matrices-and-transformations.md)
-   [<span data-ttu-id="0854f-126">Portieren von Viewports, screenmasken und scrboxes</span><span class="sxs-lookup"><span data-stu-id="0854f-126">Porting Viewports, Screenmasks, and Scrboxes</span></span>](porting-viewports--screenmasks--and-scrboxes.md)
-   [<span data-ttu-id="0854f-127">Portieren von Clippingebenen</span><span class="sxs-lookup"><span data-stu-id="0854f-127">Porting Clipping Planes</span></span>](porting-clipping-planes.md)

 

 




