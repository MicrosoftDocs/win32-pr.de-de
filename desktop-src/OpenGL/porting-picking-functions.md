---
title: Portieren von Pick-Funktionen
description: Alle IRIS GL-Pick-Funktionen verfügen über OpenGL-Entsprechungen, mit Ausnahme von clearhitcode. In der folgenden Tabelle werden die Funktionen von IRIS GL Picking und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- IRIS GL Porting, Picking
- Portieren von IRIS GL, auswählen
- Portieren auf OpenGL von IRIS GL, auswählen
- OpenGL-Portierung von IRIS GL, Auswahl
- Pick
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339003"
---
# <a name="porting-picking-functions"></a><span data-ttu-id="a8b60-109">Portieren von Pick-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a8b60-109">Porting Picking Functions</span></span>

<span data-ttu-id="a8b60-110">Alle IRIS GL-Pick-Funktionen verfügen über OpenGL-Entsprechungen, mit Ausnahme von **clearhitcode**.</span><span class="sxs-lookup"><span data-stu-id="a8b60-110">All IRIS GL picking functions have OpenGL equivalents, with the exception of **clearhitcode**.</span></span> <span data-ttu-id="a8b60-111">In der folgenden Tabelle werden die Funktionen von IRIS GL Picking und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a8b60-111">The following table lists the IRIS GL picking functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a8b60-112">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8b60-112">IRIS GL function</span></span>                | <span data-ttu-id="a8b60-113">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8b60-113">OpenGL function</span></span>                                                                           | <span data-ttu-id="a8b60-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a8b60-114">Meaning</span></span>                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a8b60-115">**clearhitcode**</span><span class="sxs-lookup"><span data-stu-id="a8b60-115">**clearhitcode**</span></span>                | <span data-ttu-id="a8b60-116">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8b60-116">Not supported.</span></span>                                                                            | <span data-ttu-id="a8b60-117">Löscht die globale Variable und den hitcode.</span><span class="sxs-lookup"><span data-stu-id="a8b60-117">Clears global variable and hitcode.</span></span>    |
| <span data-ttu-id="a8b60-118">**pickselect**</span><span class="sxs-lookup"><span data-stu-id="a8b60-118">**pickselect**</span></span><br/>       | <span data-ttu-id="a8b60-119">[**glrendermode**](glrendermode.md) (GL \_ Select)</span><span class="sxs-lookup"><span data-stu-id="a8b60-119">[**glRenderMode**](glrendermode.md) ( GL\_SELECT )</span></span>                                       | <span data-ttu-id="a8b60-120">Wechselt zum Auswahl-oder Pick-Modus.</span><span class="sxs-lookup"><span data-stu-id="a8b60-120">Switches to selection or picking mode.</span></span> |
| <span data-ttu-id="a8b60-121">**endpickendselect**</span><span class="sxs-lookup"><span data-stu-id="a8b60-121">**endpickendselect**</span></span><br/> | <span data-ttu-id="a8b60-122">[**glrendermode**](glrendermode.md) (GL- \_ Rendering)</span><span class="sxs-lookup"><span data-stu-id="a8b60-122">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )</span></span>                                       | <span data-ttu-id="a8b60-123">Wechselt in den Renderingmodus.</span><span class="sxs-lookup"><span data-stu-id="a8b60-123">Switches to rendering mode.</span></span>            |
| <span data-ttu-id="a8b60-124">**picksize**</span><span class="sxs-lookup"><span data-stu-id="a8b60-124">**picksize**</span></span>                    | <span data-ttu-id="a8b60-125">[**glupickmatrix**](glupickmatrix.md)-[**glselectbuffer**](glselectbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="a8b60-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span></span><br/> | <span data-ttu-id="a8b60-126">Legt das Rückgabe Array fest.</span><span class="sxs-lookup"><span data-stu-id="a8b60-126">Sets the return array.</span></span>                 |
| <span data-ttu-id="a8b60-127">**initnames**</span><span class="sxs-lookup"><span data-stu-id="a8b60-127">**initnames**</span></span>                   | [<span data-ttu-id="a8b60-128">**glinitnames**</span><span class="sxs-lookup"><span data-stu-id="a8b60-128">**glInitNames**</span></span>](glinitnames.md)                                                        |                                        |
| <span data-ttu-id="a8b60-129">**pushnamepopname**</span><span class="sxs-lookup"><span data-stu-id="a8b60-129">**pushnamepopname**</span></span><br/>  | <span data-ttu-id="a8b60-130">[**glpushname**](glpushname.md)([**glpopname** )](glpopname.md)</span><span class="sxs-lookup"><span data-stu-id="a8b60-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span></span><br/>                 |                                        |
| <span data-ttu-id="a8b60-131">**loadname**</span><span class="sxs-lookup"><span data-stu-id="a8b60-131">**loadname**</span></span>                    | [<span data-ttu-id="a8b60-132">**glloadname**</span><span class="sxs-lookup"><span data-stu-id="a8b60-132">**glLoadName**</span></span>](glloadname.md)                                                          |                                        |



 

<span data-ttu-id="a8b60-133">Weitere Informationen zum Auswählen von finden Sie unter [**glupickmatrix**](glupickmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a8b60-133">For more information on picking, see [**gluPickMatrix**](glupickmatrix.md).</span></span>

 

 





