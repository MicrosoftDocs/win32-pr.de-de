---
title: Portieren von greset
description: OpenGL ersetzt die Iris GL-Funktion "greset" durch die Funktionen "glpushatpub" und "glpopatpub".
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- IRIS GL portieren, Zustandsvariablen
- Portieren von IRIS GL, Zustandsvariablen
- Portieren auf OpenGL von IRIS GL, Zustandsvariablen
- OpenGL-Portierung von IRIS GL, Zustandsvariablen
- Zustandsvariablen
- IRIS GL Porting, greset-Funktion
- Portieren von IRIS GL, greset-Funktion
- Portieren auf OpenGL von IRIS GL, greset-Funktion
- OpenGL-Portierung von IRIS GL, greset-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388490"
---
# <a name="porting-greset"></a><span data-ttu-id="e8405-112">Portieren von greset</span><span class="sxs-lookup"><span data-stu-id="e8405-112">Porting greset</span></span>

<span data-ttu-id="e8405-113">OpenGL ersetzt die Iris GL-Funktion " **greset**" durch die Funktionen " [**glpushatpub**](glpushattrib.md) " und " [**glpopatpub**](glpopattrib.md)".</span><span class="sxs-lookup"><span data-stu-id="e8405-113">OpenGL replaces the IRIS GL function, **greset**, with the functions, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="e8405-114">Verwenden Sie diese Funktionen, um Gruppen von Zustandsvariablen zu speichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="e8405-114">Use these functions to save and restore groups of state variables.</span></span> <span data-ttu-id="e8405-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e8405-115">For example,</span></span>

``` syntax
void glPushAttrib( GLbitfield mask );
```

<span data-ttu-id="e8405-116">In diesem Beispiel wird eine bitweise OR-Eigenschaft von symbolischen Konstanten angenommen, die angibt, welche Gruppen von Zustandsvariablen in einem Attribut Stapel abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e8405-116">This example takes a bitwise OR of symbolic constants, indicating which groups of state variables to push onto an attribute stack.</span></span> <span data-ttu-id="e8405-117">Jede Konstante verweist auf eine Gruppe von Zustandsvariablen.</span><span class="sxs-lookup"><span data-stu-id="e8405-117">Each constant refers to a group of state variables.</span></span> <span data-ttu-id="e8405-118">In der folgenden Tabelle werden die Attribut Gruppen mit den entsprechenden symbolischen Konstanten Namen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8405-118">The following table shows the attribute groups with their equivalent symbolic constant names.</span></span> <span data-ttu-id="e8405-119">Eine komplette Liste der OpenGL-Zustandsvariablen, die den einzelnen Konstanten zugeordnet sind, finden Sie unter [**glpushatfferb**](glpushattrib.md).</span><span class="sxs-lookup"><span data-stu-id="e8405-119">For a complete list of the OpenGL state variables associated with each constant, see [**glPushAttrib**](glpushattrib.md).</span></span>



| <span data-ttu-id="e8405-120">Attribut</span><span class="sxs-lookup"><span data-stu-id="e8405-120">Attribute</span></span>                       | <span data-ttu-id="e8405-121">Konstante</span><span class="sxs-lookup"><span data-stu-id="e8405-121">Constant</span></span>                  |
|---------------------------------|---------------------------|
| <span data-ttu-id="e8405-122">Wert für Kumulations Puffer Clear</span><span class="sxs-lookup"><span data-stu-id="e8405-122">accumulation buffer clear value</span></span> | <span data-ttu-id="e8405-123">GL- \_ Accum- \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-123">GL\_ACCUM\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="e8405-124">Farb Puffer</span><span class="sxs-lookup"><span data-stu-id="e8405-124">color buffer</span></span>                    | <span data-ttu-id="e8405-125">GL- \_ Farb \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-125">GL\_COLOR\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="e8405-126">Aktuell</span><span class="sxs-lookup"><span data-stu-id="e8405-126">current</span></span>                         | <span data-ttu-id="e8405-127">GL \_ Aktuelles \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-127">GL\_CURRENT\_BIT</span></span>          |
| <span data-ttu-id="e8405-128">tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="e8405-128">depth buffer</span></span>                    | <span data-ttu-id="e8405-129">GL- \_ Tiefe- \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-129">GL\_DEPTH\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="e8405-130">enable</span><span class="sxs-lookup"><span data-stu-id="e8405-130">enable</span></span>                          | <span data-ttu-id="e8405-131">GL \_ enable \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-131">GL\_ENABLE\_BIT</span></span>           |
| <span data-ttu-id="e8405-132">Auswertungen</span><span class="sxs-lookup"><span data-stu-id="e8405-132">evaluators</span></span>                      | <span data-ttu-id="e8405-133">EGL- \_ Val- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-133">EGL\_VAL\_BIT</span></span>             |
| <span data-ttu-id="e8405-134">Nebel</span><span class="sxs-lookup"><span data-stu-id="e8405-134">fog</span></span>                             | <span data-ttu-id="e8405-135">GL \_ - \_ nebelbit</span><span class="sxs-lookup"><span data-stu-id="e8405-135">GL\_FOG\_BIT</span></span>              |
| <span data-ttu-id="e8405-136">\_ \_ Basis Einstellung der GL-Liste</span><span class="sxs-lookup"><span data-stu-id="e8405-136">GL\_LIST\_BASE setting</span></span>          | <span data-ttu-id="e8405-137">GL- \_ Listen \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-137">GL\_LIST\_BIT</span></span>             |
| <span data-ttu-id="e8405-138">Hinweis Variablen</span><span class="sxs-lookup"><span data-stu-id="e8405-138">hint variables</span></span>                  | <span data-ttu-id="e8405-139">GL- \_ Hinweis \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-139">GL\_HINT\_BIT</span></span>             |
| <span data-ttu-id="e8405-140">Beleuchtungs Variablen</span><span class="sxs-lookup"><span data-stu-id="e8405-140">lighting variables</span></span>              | <span data-ttu-id="e8405-141">GL- \_ Beleuchtungs \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-141">GL\_LIGHTING\_BIT</span></span>         |
| <span data-ttu-id="e8405-142">Zeilen Zeichnungsmodus</span><span class="sxs-lookup"><span data-stu-id="e8405-142">line drawing mode</span></span>               | <span data-ttu-id="e8405-143">GL \_ - \_ linienbit</span><span class="sxs-lookup"><span data-stu-id="e8405-143">GL\_LINE\_BIT</span></span>             |
| <span data-ttu-id="e8405-144">Pixel Modus-Variablen</span><span class="sxs-lookup"><span data-stu-id="e8405-144">pixel mode variables</span></span>            | <span data-ttu-id="e8405-145">GL- \_ Pixel \_ Modus- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-145">GL\_PIXEL\_MODE\_BIT</span></span>      |
| <span data-ttu-id="e8405-146">Punkt Variablen</span><span class="sxs-lookup"><span data-stu-id="e8405-146">point variables</span></span>                 | <span data-ttu-id="e8405-147">GL \_ - \_ punktbit</span><span class="sxs-lookup"><span data-stu-id="e8405-147">GL\_POINT\_BIT</span></span>            |
| <span data-ttu-id="e8405-148">polygon</span><span class="sxs-lookup"><span data-stu-id="e8405-148">polygon</span></span>                         | <span data-ttu-id="e8405-149">GL- \_ Polygon- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-149">GL\_POLYGON\_BIT</span></span>          |
| <span data-ttu-id="e8405-150">Polygon-Stippel</span><span class="sxs-lookup"><span data-stu-id="e8405-150">polygon stipple</span></span>                 | <span data-ttu-id="e8405-151">GL- \_ Polygon- \_ Stippel \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-151">GL\_POLYGON\_STIPPLE\_BIT</span></span> |
| <span data-ttu-id="e8405-152">Scheren</span><span class="sxs-lookup"><span data-stu-id="e8405-152">scissor</span></span>                         | <span data-ttu-id="e8405-153">GL- \_ Scheren- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-153">GL\_SCISSOR\_BIT</span></span>          |
| <span data-ttu-id="e8405-154">Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="e8405-154">stencil buffer</span></span>                  | <span data-ttu-id="e8405-155">GL- \_ Schablone- \_ Puffer \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-155">GL\_STENCIL\_BUFFER\_BIT</span></span>  |
| <span data-ttu-id="e8405-156">Struktur</span><span class="sxs-lookup"><span data-stu-id="e8405-156">texture</span></span>                         | <span data-ttu-id="e8405-157">GL- \_ Textur \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-157">GL\_TEXTURE\_BIT</span></span>          |
| <span data-ttu-id="e8405-158">Transformieren</span><span class="sxs-lookup"><span data-stu-id="e8405-158">transform</span></span>                       | <span data-ttu-id="e8405-159">GL- \_ Transform- \_ Bit</span><span class="sxs-lookup"><span data-stu-id="e8405-159">GL\_TRANSFORM\_BIT</span></span>        |
| <span data-ttu-id="e8405-160">Viewport</span><span class="sxs-lookup"><span data-stu-id="e8405-160">viewport</span></span>                        | <span data-ttu-id="e8405-161">GL- \_ \_ viewportbit</span><span class="sxs-lookup"><span data-stu-id="e8405-161">GL\_VIEWPORT\_BIT</span></span>         |
|                                 | <span data-ttu-id="e8405-162">GL \_ alle \_ attrb- \_ Bits</span><span class="sxs-lookup"><span data-stu-id="e8405-162">GL\_ALL\_ATTRIB\_BITS</span></span>     |



 

<span data-ttu-id="e8405-163">Um die Werte der Zustandsvariablen wiederherzustellen, die mit dem letzten [**glpushatpub**](glpushattrib.md)gespeichert wurden, nennen Sie einfach " [**glpopatpub**](glpopattrib.md)".</span><span class="sxs-lookup"><span data-stu-id="e8405-163">To restore the values of the state variables to those saved with the last [**glPushAttrib**](glpushattrib.md), simply call [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="e8405-164">Die Variablen, die Sie nicht gespeichert haben, bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="e8405-164">The variables you didn't save will remain unchanged.</span></span> <span data-ttu-id="e8405-165">Der Attribut Stapel hat eine endliche Tiefe von mindestens 16.</span><span class="sxs-lookup"><span data-stu-id="e8405-165">The attribute stack has a finite depth of at least 16.</span></span>

 

 




