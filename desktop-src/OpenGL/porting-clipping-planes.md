---
title: Portieren von Clippingebenen
description: OpenGL implementiert clippingplane ähnlich wie IRIS GL. Außerdem können Sie in OpenGL Clippingebenen Abfragen. In der folgenden Tabelle sind die Funktionen von IRIS GL Clipping Plane und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- IRIS GL portieren, Clipping-Ebenen
- Portieren von IRIS GL, Clipping-Ebenen
- Portieren auf OpenGL von IRIS GL, Clipping-Ebenen
- OpenGL-Portierung von IRIS GL, Clipping-Ebenen
- Clipping-Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713583"
---
# <a name="porting-clipping-planes"></a><span data-ttu-id="64fa6-110">Portieren von Clippingebenen</span><span class="sxs-lookup"><span data-stu-id="64fa6-110">Porting Clipping Planes</span></span>

<span data-ttu-id="64fa6-111">OpenGL implementiert clippingplane ähnlich wie IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="64fa6-111">OpenGL implements clipping planes similarly to IRIS GL.</span></span> <span data-ttu-id="64fa6-112">Außerdem können Sie in OpenGL Clippingebenen Abfragen.</span><span class="sxs-lookup"><span data-stu-id="64fa6-112">In addition, in OpenGL you can query clipping planes.</span></span> <span data-ttu-id="64fa6-113">In der folgenden Tabelle sind die Funktionen von IRIS GL Clipping Plane und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="64fa6-113">The following table lists IRIS GL clipping plane functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="64fa6-114">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="64fa6-114">IRIS GL function</span></span>                          | <span data-ttu-id="64fa6-115">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="64fa6-115">OpenGL function</span></span>                                                                               | <span data-ttu-id="64fa6-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64fa6-116">Meaning</span></span>                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="64fa6-117">**clipplane** (i, **CP \_ on**, Parametern)</span><span class="sxs-lookup"><span data-stu-id="64fa6-117">**clipplane** (i, **CP\_ON**, params)</span></span>     | <span data-ttu-id="64fa6-118">[**glEnable**](glenable.md) (GL- \_ Clip \_ planei)</span><span class="sxs-lookup"><span data-stu-id="64fa6-118">[**glEnable**](glenable.md) ( GL\_CLIP\_PLANEi )</span></span>                                             | <span data-ttu-id="64fa6-119">Aktiviert Clipping auf Ebene i.</span><span class="sxs-lookup"><span data-stu-id="64fa6-119">Enables clipping on plane i.</span></span>             |
| <span data-ttu-id="64fa6-120">**clipplane**(i, **CP \_ define**, Plane)</span><span class="sxs-lookup"><span data-stu-id="64fa6-120">**clipplane**( i, **CP\_DEFINE**, plane )</span></span> | <span data-ttu-id="64fa6-121">[**glclipplane**](glclipplane.md) (GL- \_ Clip \_ planei, Plane)</span><span class="sxs-lookup"><span data-stu-id="64fa6-121">[**glClipPlane**](glclipplane.md) ( GL\_CLIP\_PLANEi, plane )</span></span>                                | <span data-ttu-id="64fa6-122">Definiert die Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="64fa6-122">Defines clipping plane.</span></span>                  |
|                                           | [<span data-ttu-id="64fa6-123">**glgetclipplane**</span><span class="sxs-lookup"><span data-stu-id="64fa6-123">**glGetClipPlane**</span></span>](glgetclipplane.md)                                                      | <span data-ttu-id="64fa6-124">Gibt die Gleichung der Clipping-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="64fa6-124">Returns clipping plane equation.</span></span>         |
|                                           | <span data-ttu-id="64fa6-125">[**glisenabled**](glisenabled.md) (GL- \_ Clip \_ planei)</span><span class="sxs-lookup"><span data-stu-id="64fa6-125">[**glIsEnabled**](glisenabled.md) ( GL\_CLIP\_PLANEi )</span></span>                                       | <span data-ttu-id="64fa6-126">Gibt true zurück, wenn Clip Plane i aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="64fa6-126">Returns true if clip plane i is enabled.</span></span> |
| <span data-ttu-id="64fa6-127">**scrmask**</span><span class="sxs-lookup"><span data-stu-id="64fa6-127">**scrmask**</span></span>                               | [<span data-ttu-id="64fa6-128">**glscissor**</span><span class="sxs-lookup"><span data-stu-id="64fa6-128">**glScissor**</span></span>](glscissor.md)                                                                | <span data-ttu-id="64fa6-129">Definiert das Feld "Scheren".</span><span class="sxs-lookup"><span data-stu-id="64fa6-129">Defines the scissor box.</span></span>                 |
| <span data-ttu-id="64fa6-130">**getscrmask**</span><span class="sxs-lookup"><span data-stu-id="64fa6-130">**getscrmask**</span></span>                            | <span data-ttu-id="64fa6-131">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (Feld "GL \_ Scissor" \_ )</span><span class="sxs-lookup"><span data-stu-id="64fa6-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SCISSOR\_BOX )</span></span> | <span data-ttu-id="64fa6-132">Gibt das aktuelle Scheren Feld zurück.</span><span class="sxs-lookup"><span data-stu-id="64fa6-132">Returns the current scissor box.</span></span>         |



 

<span data-ttu-id="64fa6-133">Um den Scheren Test zu aktivieren, nennen Sie " **glEnable** " mithilfe von "GL \_ Scheren \_ Box" als Parameter.</span><span class="sxs-lookup"><span data-stu-id="64fa6-133">To turn on the scissor test, call **glEnable** using GL\_SCISSOR\_BOX as the parameter.</span></span>

<span data-ttu-id="64fa6-134">??</span><span class="sxs-lookup"><span data-stu-id="64fa6-134">??</span></span>

 

 




