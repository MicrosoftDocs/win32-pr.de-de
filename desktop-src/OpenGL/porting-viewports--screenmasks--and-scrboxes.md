---
title: Portieren von Viewports, screenmasken und scrboxes
description: Die folgenden IRIS GL-viewportfunktionen haben keine OpenGL-Entsprechung.
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- IRIS GL Porting, Viewport-Funktionen
- Portieren von IRIS GL, Viewport-Funktionen
- Portieren auf OpenGL von IRIS GL, Viewport-Funktionen
- OpenGL-Portierung von IRIS GL, Viewport-Funktionen
- Viewport-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337149"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a><span data-ttu-id="0dc92-108">Portieren von Viewports, screenmasken und scrboxes</span><span class="sxs-lookup"><span data-stu-id="0dc92-108">Porting Viewports, Screenmasks, and Scrboxes</span></span>

<span data-ttu-id="0dc92-109">Die folgenden IRIS GL-viewportfunktionen haben keine OpenGL-Entsprechung:</span><span class="sxs-lookup"><span data-stu-id="0dc92-109">The following IRIS GL viewport functions have no OpenGL equivalent:</span></span>

-   <span data-ttu-id="0dc92-110">**reshapeviewport**</span><span class="sxs-lookup"><span data-stu-id="0dc92-110">**reshapeviewport**</span></span>
-   <span data-ttu-id="0dc92-111">**scrbox**</span><span class="sxs-lookup"><span data-stu-id="0dc92-111">**scrbox**</span></span>
-   <span data-ttu-id="0dc92-112">**getscrbox**</span><span class="sxs-lookup"><span data-stu-id="0dc92-112">**getscrbox**</span></span>

<span data-ttu-id="0dc92-113">Mit der Iris GL **Viewport** -Funktion geben Sie die x-Koordinaten (in Pixel) für den linken und rechten Rand eines Viewportrechtecks und die y-Koordinaten für den oberen und unteren Rand an.</span><span class="sxs-lookup"><span data-stu-id="0dc92-113">With the IRIS GL **viewport** function, you specify the x coordinates (in pixels) for the left and right of a viewport rectangle and the y coordinates for the top and bottom.</span></span> <span data-ttu-id="0dc92-114">Mit der OpenGL-Funktion " [**glViewport**](glviewport.md) " geben Sie jedoch die x-und y-Koordinaten (in Pixel) der unteren linken Ecke des Viewportrechtecks zusammen mit der Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="0dc92-114">With the OpenGL [**glViewport**](glviewport.md) function, however, you specify the x and y coordinates (in pixels) of the lower-left corner of the viewport rectangle along with its width and height.</span></span>

<span data-ttu-id="0dc92-115">In der folgenden Tabelle sind die Funktionen von IRIS GL Viewport und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0dc92-115">The following table lists IRIS GL viewport functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0dc92-116">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="0dc92-116">IRIS GL function</span></span>                          | <span data-ttu-id="0dc92-117">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="0dc92-117">OpenGL function</span></span>                                                                                         | <span data-ttu-id="0dc92-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0dc92-118">Meaning</span></span>                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="0dc92-119">**Viewport** (Links, rechts, unten, oben)</span><span class="sxs-lookup"><span data-stu-id="0dc92-119">**viewport** ( left, right, bottom, top )</span></span> | <span data-ttu-id="0dc92-120">[**glViewport**](glviewport.md) (x, y, Breite, Höhe)</span><span class="sxs-lookup"><span data-stu-id="0dc92-120">[**glViewport**](glviewport.md) ( x, y, width, height )</span></span>                                                | <span data-ttu-id="0dc92-121">Legt den Viewport fest.</span><span class="sxs-lookup"><span data-stu-id="0dc92-121">Sets the viewport.</span></span>           |
| <span data-ttu-id="0dc92-122">**popviewportpushviewport**</span><span class="sxs-lookup"><span data-stu-id="0dc92-122">**popviewportpushviewport**</span></span><br/>    | <span data-ttu-id="0dc92-123">[**glpopatpub**](glpopattrib.md)[**glpushatkarb**](glpushattrib.md) (GL- \_ \_ viewportbit)</span><span class="sxs-lookup"><span data-stu-id="0dc92-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL\_VIEWPORT\_BIT )</span></span><br/> | <span data-ttu-id="0dc92-124">Überträgt den Stapel und zeigt ihn an.</span><span class="sxs-lookup"><span data-stu-id="0dc92-124">Pushes and pops the stack.</span></span>   |
| <span data-ttu-id="0dc92-125">**getviewport**</span><span class="sxs-lookup"><span data-stu-id="0dc92-125">**getviewport**</span></span>                           | <span data-ttu-id="0dc92-126">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Viewport)</span><span class="sxs-lookup"><span data-stu-id="0dc92-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_VIEWPORT )</span></span>               | <span data-ttu-id="0dc92-127">Gibt viewportdimensionen zurück.</span><span class="sxs-lookup"><span data-stu-id="0dc92-127">Returns viewport dimensions.</span></span> |



 

<span data-ttu-id="0dc92-128">??</span><span class="sxs-lookup"><span data-stu-id="0dc92-128">??</span></span>

 

 





