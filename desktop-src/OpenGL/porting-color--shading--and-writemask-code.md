---
title: Portieren von Farb-, Schattierungs-und beschreibe-Code
description: Portieren von Farb-, Schattierungs-und beschreibe-Code
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- IRIS GL portieren, Farbe
- Portieren von IRIS GL, Color
- Portieren auf OpenGL von IRIS GL, Color
- OpenGL-Portierung von IRIS GL, Color
- IRIS GL portieren, Schattierung
- Portieren von IRIS GL, Schattierung
- Portieren auf OpenGL von IRIS GL, Schattierung
- OpenGL-Portierung von IRIS GL, Schattierung
- IRIS GL portieren, Write-Ask
- Portieren von IRIS GL, Write temask
- Portieren auf OpenGL von IRIS GL, Write temask
- OpenGL-Portierung von IRIS GL, Write temask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708466"
---
# <a name="porting-color-shading-and-writemask-code"></a><span data-ttu-id="ad100-115">Portieren von Farb-, Schattierungs-und beschreibe-Code</span><span class="sxs-lookup"><span data-stu-id="ad100-115">Porting Color, Shading, and Writemask Code</span></span>

<span data-ttu-id="ad100-116">Beachten Sie beim Portieren von Farb-, Schattierungs-und beschreibe-Code in OpenGL die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="ad100-116">When porting color, shading, and writemask code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="ad100-117">Obwohl Sie Farb Zuordnungs Indizes mit der OpenGL-Funktion " [glindex](glindex-functions.md) " festlegen können, verfügt OpenGL nicht über eine Funktion zum Laden von Farb Zuordnungs Indizes.</span><span class="sxs-lookup"><span data-stu-id="ad100-117">Though you can set color-map indexes with the OpenGL [glIndex](glindex-functions.md) function, OpenGL does not have a function for loading color-map indexes.</span></span>
-   <span data-ttu-id="ad100-118">Farbwerte werden in ihren Datentyp normalisiert.</span><span class="sxs-lookup"><span data-stu-id="ad100-118">Color values are normalized to their data type.</span></span> <span data-ttu-id="ad100-119">(Informationen zu Farbwerten finden Sie unter [glcolor](glcolor-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="ad100-119">(For information about color values, see [glColor](glcolor-functions.md)).</span></span>
-   <span data-ttu-id="ad100-120">Es gibt keine einfache Entsprechung für **CPack**.</span><span class="sxs-lookup"><span data-stu-id="ad100-120">There is no simple equivalent for **cpack**.</span></span>
-   <span data-ttu-id="ad100-121">Sie müssen möglicherweise Code, der die **c** -oder **Color** -Funktionen enthält, in [**glclearcolor**](glclearcolor.md) oder [**glclearindex**](glclearindex.md) anstelle von **glcolor** oder **glindex** übersetzen.</span><span class="sxs-lookup"><span data-stu-id="ad100-121">You may have to translate code that includes the **c** or **color** functions to [**glClearColor**](glclearcolor.md) or [**glClearIndex**](glclearindex.md) instead of **glColor** or **glIndex**.</span></span>
-   <span data-ttu-id="ad100-122">Die RGBA-Schreibweise wird für jede Komponente angewendet, aber nicht für jedes Bit.</span><span class="sxs-lookup"><span data-stu-id="ad100-122">The RGBA writemask applies to each component but not for each bit.</span></span>
-   <span data-ttu-id="ad100-123">IRIS GL bietet definierte Farb Konstanten: schwarz, blau, rot, grün, Magenta, Cyan, gelb und weiß.</span><span class="sxs-lookup"><span data-stu-id="ad100-123">IRIS GL provides defined color constants: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW, and WHITE.</span></span> <span data-ttu-id="ad100-124">OpenGL bietet diese Konstanten nicht.</span><span class="sxs-lookup"><span data-stu-id="ad100-124">OpenGL does not provide these constants.</span></span>

<span data-ttu-id="ad100-125">Dieses Thema enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="ad100-125">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="ad100-126">Portieren von Farb aufrufen</span><span class="sxs-lookup"><span data-stu-id="ad100-126">Porting Color Calls</span></span>](porting-color-calls.md)
-   [<span data-ttu-id="ad100-127">Portieren von Schattierungs Modellen</span><span class="sxs-lookup"><span data-stu-id="ad100-127">Porting Shading Models</span></span>](porting-shading-models.md)

 

 




