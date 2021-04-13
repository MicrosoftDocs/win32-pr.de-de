---
title: Portieren von Dreiecken
description: Sie können drei Arten von Dreiecken in OpenGL zeichnen, indem Sie die Dreiecke, Dreiecks Streifen und Dreiecks Lüfter trennen.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- IRIS GL portieren, Dreiecke
- Portieren von IRIS GL, Dreiecke
- Portieren auf OpenGL von IRIS GL, Dreiecke
- OpenGL-Portierung von IRIS GL, Dreiecke
- Zeichnungsfunktionen, Dreiecke
- Dreiecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310535"
---
# <a name="porting-triangles"></a><span data-ttu-id="4031b-109">Portieren von Dreiecken</span><span class="sxs-lookup"><span data-stu-id="4031b-109">Porting Triangles</span></span>

<span data-ttu-id="4031b-110">Sie können drei Arten von Dreiecken in OpenGL zeichnen: separate Dreiecke, Dreiecks Streifen und Dreiecks Lüfter.</span><span class="sxs-lookup"><span data-stu-id="4031b-110">You can draw three types of triangles in OpenGL: separate triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="4031b-111">OpenGL hat keine Entsprechung für die Iris **GL-** Funktion "".</span><span class="sxs-lookup"><span data-stu-id="4031b-111">OpenGL has no equivalent for the IRIS GL **swaptmesh** function.</span></span> <span data-ttu-id="4031b-112">Sie können denselben Effekt erzielen, indem Sie eine Kombination aus Dreiecke, Dreiecks Streifen und Dreiecks Lüfter verwenden.</span><span class="sxs-lookup"><span data-stu-id="4031b-112">You can achieve the same effect using a combination of triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="4031b-113">In der folgenden Tabelle sind die Iris GL-Funktionen zum Zeichnen von Dreiecken und ihre entsprechenden OpenGL-Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4031b-113">The following table lists the IRIS GL functions for drawing triangles and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4031b-114">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="4031b-114">IRIS GL function</span></span>           | <span data-ttu-id="4031b-115">Äquivalenter glBegin-Parameter</span><span class="sxs-lookup"><span data-stu-id="4031b-115">Equivalent glBegin parameter</span></span> | <span data-ttu-id="4031b-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4031b-116">Meaning</span></span>                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | <span data-ttu-id="4031b-117">GL- \_ Dreiecke</span><span class="sxs-lookup"><span data-stu-id="4031b-117">GL\_TRIANGLES</span></span>                | <span data-ttu-id="4031b-118">Die als Dreiecke interpretierten Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="4031b-118">Triples of vertices interpreted as triangles.</span></span> |
| <span data-ttu-id="4031b-119">**bgntmesh**, **endtmesh**</span><span class="sxs-lookup"><span data-stu-id="4031b-119">**bgntmesh**, **endtmesh**</span></span> | <span data-ttu-id="4031b-120">GL- \_ Dreiecks \_ Streifen</span><span class="sxs-lookup"><span data-stu-id="4031b-120">GL\_TRIANGLE\_STRIP</span></span>          | <span data-ttu-id="4031b-121">Verknüpfte Streifen von Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="4031b-121">Linked strips of triangles.</span></span>                   |
|                            | <span data-ttu-id="4031b-122">GL- \_ Dreiecks \_ Lüfter</span><span class="sxs-lookup"><span data-stu-id="4031b-122">GL\_TRIANGLE\_FAN</span></span>            | <span data-ttu-id="4031b-123">Verknüpfte Fans von Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="4031b-123">Linked fans of triangles.</span></span>                     |



 

<span data-ttu-id="4031b-124">??</span><span class="sxs-lookup"><span data-stu-id="4031b-124">??</span></span>

 

 




