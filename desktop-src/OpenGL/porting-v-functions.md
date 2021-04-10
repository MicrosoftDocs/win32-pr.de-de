---
title: Portieren von v-Funktionen
description: In IRIS GL verwenden Sie Variationen der v-Funktion, um Vertices anzugeben. Die entsprechende OpenGL-Funktion ist "glVertex" unten sind Beispiele für "glVertex".
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- IRIS GL portieren, Vertices
- Portieren von IRIS GL, Vertices
- Portieren auf OpenGL von IRIS GL, Vertices
- OpenGL-Portierung von IRIS GL, Vertices
- Zeichnungsfunktionen, Vertices
- Vertices, Portieren von IRIS GL
- IRIS GL Porting, v Functions
- Portieren von IRIS GL, v Functions
- Portieren auf OpenGL von IRIS GL, v Functions
- OpenGL-Portierung von IRIS GL, v Functions
- Zeichnungsfunktionen, v-Funktionen
- v-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309751"
---
# <a name="porting-v-functions"></a><span data-ttu-id="7e36e-116">Portieren von v-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7e36e-116">Porting v Functions</span></span>

<span data-ttu-id="7e36e-117">In IRIS GL verwenden Sie Variationen der **v** -Funktion, um Vertices anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7e36e-117">In IRIS GL, you use variations on the **v** function to specify vertices.</span></span> <span data-ttu-id="7e36e-118">Die entsprechende OpenGL-Funktion ist " [glVertex](glvertex-functions.md)": im folgenden finden Sie Beispiele für " **glVertex**".</span><span class="sxs-lookup"><span data-stu-id="7e36e-118">The equivalent OpenGL function is [glVertex](glvertex-functions.md): Below are examples of **glVertex**.</span></span>

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

<span data-ttu-id="7e36e-119">Die **glVertex** -Funktion nimmt Suffixe auf dieselbe Weise wie andere OpenGL-Aufrufe auf.</span><span class="sxs-lookup"><span data-stu-id="7e36e-119">The **glVertex** function takes suffixes the same way other OpenGL calls do.</span></span> <span data-ttu-id="7e36e-120">Die Vektor Versionen des Aufrufes übernehmen Arrays der richtigen Größe als Argumente.</span><span class="sxs-lookup"><span data-stu-id="7e36e-120">The vector versions of the call take arrays of the proper size as arguments.</span></span> <span data-ttu-id="7e36e-121">In der 2D-Version z = 0 und w = 1.</span><span class="sxs-lookup"><span data-stu-id="7e36e-121">In the 2-D version, z=0 and w=1.</span></span> <span data-ttu-id="7e36e-122">In der 3D-Version ist w = 1.</span><span class="sxs-lookup"><span data-stu-id="7e36e-122">In the 3-D version, w=1.</span></span>

 

 




