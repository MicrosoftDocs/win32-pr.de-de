---
title: Portieren von defs, Bindungen und Sätzen
description: Portieren von defs, Bindungen und Sätzen
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- IRIS GL portieren, Definitionen
- Portieren von IRIS GL, Definitionen
- Portieren auf OpenGL von IRIS GL, Definitionen
- OpenGL-Portierung von IRIS GL, Definitionen
- IRIS GL portieren, Bindungen
- Portieren von IRIS GL, Bindungen
- Portieren auf OpenGL von IRIS GL, Bindungen
- OpenGL-Portierung von IRIS GL, Bindungen
- IRIS GL Porting, Sets
- Portieren von IRIS GL, Sets
- Portieren auf OpenGL von IRIS GL, Sets
- OpenGL-Portierung von IRIS GL, Sets
- definitions
- miteinander
- Mengen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342244"
---
# <a name="porting-defs-binds-and-sets"></a><span data-ttu-id="289dd-118">Portieren von defs, Bindungen und Sätzen</span><span class="sxs-lookup"><span data-stu-id="289dd-118">Porting Defs, Binds, and Sets</span></span>

<span data-ttu-id="289dd-119">OpenGL hat keine Tabellen mit gespeicherten Definitionen. Sie können keine Beleuchtungs Modelle, Materialien, Texturen, Linienstile oder Muster als separate Objekte definieren, wie Sie es in IRIS GL haben.</span><span class="sxs-lookup"><span data-stu-id="289dd-119">OpenGL doesn't have tables of stored definitions; you can't define lighting models, material, textures, line styles, or patterns as separate objects as you can in IRIS GL.</span></span> <span data-ttu-id="289dd-120">Daher hat OpenGL keine direkten Entsprechungen für die folgenden IRIS GL-Funktionen:</span><span class="sxs-lookup"><span data-stu-id="289dd-120">Thus OpenGL has no direct equivalents to the following IRIS GL functions:</span></span>

-   <span data-ttu-id="289dd-121">**Imdef** und **imbind**</span><span class="sxs-lookup"><span data-stu-id="289dd-121">**Imdef** and **Imbind**</span></span>
-   <span data-ttu-id="289dd-122">**tevdef** und **tevbind**</span><span class="sxs-lookup"><span data-stu-id="289dd-122">**tevdef** and **tevbind**</span></span>
-   <span data-ttu-id="289dd-123">**textdef** und **textbind**</span><span class="sxs-lookup"><span data-stu-id="289dd-123">**textdef** and **textbind**</span></span>
-   <span data-ttu-id="289dd-124">**definestyle** und **SetStyle**</span><span class="sxs-lookup"><span data-stu-id="289dd-124">**definestyle** and **setstyle**</span></span>
-   <span data-ttu-id="289dd-125">**defpattern** und **SetPattern**</span><span class="sxs-lookup"><span data-stu-id="289dd-125">**defpattern** and **setpattern**</span></span>

<span data-ttu-id="289dd-126">Mithilfe der OpenGL-Anzeigelisten können Sie den Iris GL DEF/BIND-Mechanismus imitieren.</span><span class="sxs-lookup"><span data-stu-id="289dd-126">You can use OpenGL display lists to mimic the IRIS GL def/bind mechanism.</span></span> <span data-ttu-id="289dd-127">Hier ist beispielsweise eine Material Definition in IRIS GL:</span><span class="sxs-lookup"><span data-stu-id="289dd-127">For example, here is a material definition in IRIS GL:</span></span>


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



<span data-ttu-id="289dd-128">Im folgenden OpenGL-Codebeispiel wird das gleiche Material in einer Anzeigeliste definiert, auf die durch die von **myMaterial** definierte Listen Zahl verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="289dd-128">The following OpenGL code sample defines the same material in a display list that is referred to by the list number defined by **MYMATERIAL**.</span></span>


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




