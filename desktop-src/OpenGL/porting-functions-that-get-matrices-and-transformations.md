---
title: Portieren von Funktionen, die Matrizen und Transformationen erhalten
description: In der folgenden Tabelle werden die Iris GL-Funktionen aufgelistet, die den Status von Matrizen und Transformationen und deren OpenGL-Entsprechungen erhalten.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- IRIS GL portieren, Matrizen
- Portieren von IRIS GL, Matrizen
- Portieren auf OpenGL von IRIS GL, Matrizen
- OpenGL-Portierung von IRIS GL, Matrizen
- Matrizen
- IRIS GL portieren, Transformationen
- Portieren von IRIS GL, Transformationen
- Portieren auf OpenGL von IRIS GL, Transformationen
- OpenGL-Portierung von IRIS GL, Transformationen
- Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947822"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a><span data-ttu-id="02d6b-113">Portieren von Funktionen, die Matrizen und Transformationen erhalten</span><span class="sxs-lookup"><span data-stu-id="02d6b-113">Porting Functions that Get Matrices and Transformations</span></span>

<span data-ttu-id="02d6b-114">In der folgenden Tabelle werden die Iris GL-Funktionen aufgelistet, die den Status von Matrizen und Transformationen und deren OpenGL-Entsprechungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="02d6b-114">The following table lists the IRIS GL functions that get the state of matrices and transformations and their OpenGL equivalents.</span></span>



| <span data-ttu-id="02d6b-115">IRIS GL-Matrix Abfrage</span><span class="sxs-lookup"><span data-stu-id="02d6b-115">IRIS GL matrix query</span></span>                  | <span data-ttu-id="02d6b-116">OpenGL-glget-Matrix Abfrage</span><span class="sxs-lookup"><span data-stu-id="02d6b-116">OpenGL glGet matrix query</span></span>         | <span data-ttu-id="02d6b-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="02d6b-117">Meaning</span></span>                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="02d6b-118">**getmmode**</span><span class="sxs-lookup"><span data-stu-id="02d6b-118">**getmmode**</span></span>                          | <span data-ttu-id="02d6b-119">GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="02d6b-119">GL\_MATRIX\_MODE</span></span>                  | <span data-ttu-id="02d6b-120">Gibt den aktuellen Matrix Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-120">Returns the current matrix mode.</span></span>                                |
| <span data-ttu-id="02d6b-121">**getMatrix** im **MVIEW** -Modus</span><span class="sxs-lookup"><span data-stu-id="02d6b-121">**getmatrix** in **MVIEWING** mode</span></span>    | <span data-ttu-id="02d6b-122">GL- \_ Modelview- \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="02d6b-122">GL\_MODELVIEW\_MATRIX</span></span>             | <span data-ttu-id="02d6b-123">Gibt eine Kopie der aktuellen Modell Ansichts Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-123">Returns a copy of the current model-view matrix.</span></span>                |
| <span data-ttu-id="02d6b-124">**getMatrix** im **mprojection** -Modus</span><span class="sxs-lookup"><span data-stu-id="02d6b-124">**getmatrix** in **MPROJECTION** mode</span></span> | <span data-ttu-id="02d6b-125">GL- \_ Projektions \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="02d6b-125">GL\_PROJECTION\_MATRIX</span></span>            | <span data-ttu-id="02d6b-126">Gibt eine Kopie der aktuellen Projektions Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-126">Returns a copy of the current projection matrix.</span></span>                |
| <span data-ttu-id="02d6b-127">**getMatrix** im **mtexture** -Modus</span><span class="sxs-lookup"><span data-stu-id="02d6b-127">**getmatrix** in **MTEXTURE** mode</span></span>    | <span data-ttu-id="02d6b-128">GL- \_ Textur \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="02d6b-128">GL\_TEXTURE\_MATRIX</span></span>               | <span data-ttu-id="02d6b-129">Gibt eine Kopie der aktuellen Textur Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-129">Returns a copy of the current texture matrix.</span></span>                   |
| <span data-ttu-id="02d6b-130">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="02d6b-130">Not applicable.</span></span>                       | <span data-ttu-id="02d6b-131">\_Max. maximale \_ Modelview- \_ Stapel \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="02d6b-131">GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>  | <span data-ttu-id="02d6b-132">Gibt die maximal unterstützte Tiefe des Modell Ansichts Matrix Stapels zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-132">Returns maximum supported depth of the model-view matrix stack.</span></span> |
| <span data-ttu-id="02d6b-133">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="02d6b-133">Not applicable.</span></span>                       | <span data-ttu-id="02d6b-134">\_Maximale maximale \_ Projektions \_ Stapel \_ Tiefe von GL</span><span class="sxs-lookup"><span data-stu-id="02d6b-134">GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span> | <span data-ttu-id="02d6b-135">Gibt die maximal unterstützte Tiefe des Projektions Matrix Stapels zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-135">Returns maximum supported depth of the projection matrix stack.</span></span> |
| <span data-ttu-id="02d6b-136">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="02d6b-136">Not applicable.</span></span>                       | <span data-ttu-id="02d6b-137">\_Maximale maximale \_ Textur \_ Stapel \_ Tiefe von GL</span><span class="sxs-lookup"><span data-stu-id="02d6b-137">GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>    | <span data-ttu-id="02d6b-138">Gibt die maximal unterstützte Tiefe des Textur Matrix Stapels zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-138">Returns maximum supported depth of the texture matrix stack.</span></span>    |
| <span data-ttu-id="02d6b-139">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="02d6b-139">Not applicable.</span></span>                       | <span data-ttu-id="02d6b-140">\_ \_ Stapel Tiefe von GL Modelview \_</span><span class="sxs-lookup"><span data-stu-id="02d6b-140">GL\_MODELVIEW\_STACK\_DEPTH</span></span>       | <span data-ttu-id="02d6b-141">Gibt die Anzahl von Matrizen im Modell Ansichts Stapel zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-141">Returns number of matrices on the model view stack.</span></span>             |
| <span data-ttu-id="02d6b-142">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="02d6b-142">Not applicable.</span></span>                       | <span data-ttu-id="02d6b-143">\_ \_ Stapel \_ Tiefe der GL-Projektion</span><span class="sxs-lookup"><span data-stu-id="02d6b-143">GL\_PROJECTION\_STACK\_DEPTH</span></span>      | <span data-ttu-id="02d6b-144">Gibt die Anzahl von Matrizen auf dem Projektions Stapel zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-144">Returns number of matrices on the projection stack.</span></span>             |
| <span data-ttu-id="02d6b-145">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="02d6b-145">Not applicable.</span></span>                       | <span data-ttu-id="02d6b-146">GL- \_ Textur \_ Stapel \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="02d6b-146">GL\_TEXTURE\_STACK\_DEPTH</span></span>         | <span data-ttu-id="02d6b-147">Gibt die Anzahl von Matrizen auf dem Textur Stapel zurück.</span><span class="sxs-lookup"><span data-stu-id="02d6b-147">Returns number of matrices on the texture stack.</span></span>                |



 

<span data-ttu-id="02d6b-148">??</span><span class="sxs-lookup"><span data-stu-id="02d6b-148">??</span></span>

 

 




