---
title: Portieren von Bildschirm-und Puffer Lösch Befehlen
description: OpenGL ersetzt eine Reihe von IRIS GL Clear-Funktionen (z. b. zclear, aclear, sClear usw.) durch eine einzelne Funktion, glClear. Geben Sie genau an, was Sie löschen möchten, indem Sie Masken an glClear übergeben.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- IRIS GL portieren, Löschen von Funktionen
- Portieren von IRIS GL, Löschen von Funktionen
- Portieren auf OpenGL von IRIS GL, Clear Functions
- OpenGL-Portierung von IRIS GL, Clear Functions
- Funktionen löschen
- IRIS GL Porting, Befehle zum Löschen von Bildschirmen
- portieren aus IRIS GL, Befehle zum Löschen von Bildschirmen
- Portieren auf OpenGL von IRIS GL, Befehle zum Löschen von Bildschirmen
- OpenGL-Portierung von IRIS GL, Befehle zum Löschen von Bildschirmen
- Bildschirm Lösch Befehle
- IRIS GL Porting, Befehle zum Löschen von Puffern
- Portieren von IRIS GL, Puffer Lösch Befehle
- Portieren von IRIS gl auf OpenGL, Puffer Lösch Befehle
- OpenGL-Portierung von IRIS GL, Puffer Lösch Befehle
- Puffer Lösch Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341463"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a><span data-ttu-id="ae27e-119">Portieren von Bildschirm-und Puffer Lösch Befehlen</span><span class="sxs-lookup"><span data-stu-id="ae27e-119">Porting Screen and Buffer Clearing Commands</span></span>

<span data-ttu-id="ae27e-120">OpenGL ersetzt eine Reihe von IRIS GL **Clear** -Funktionen (z. b. **zclear**, **aclear**, **sClear** usw.) durch eine einzelne Funktion, [**glClear**](glclear.md).</span><span class="sxs-lookup"><span data-stu-id="ae27e-120">OpenGL replaces a variety of IRIS GL **clear** functions (such as **zclear**, **aclear**, **sclear**, and so on) with a single function, [**glClear**](glclear.md).</span></span> <span data-ttu-id="ae27e-121">Geben Sie genau an, was Sie löschen möchten, indem Sie Masken an **glClear** übergeben.</span><span class="sxs-lookup"><span data-stu-id="ae27e-121">Specify exactly what you want to clear by passing masks to **glClear**.</span></span>

<span data-ttu-id="ae27e-122">Beachten Sie die folgenden Punkte, wenn Sie Bildschirm-und Puffer Befehle portieren:</span><span class="sxs-lookup"><span data-stu-id="ae27e-122">Keep the following points in mind when porting screen and buffer commands:</span></span>

-   <span data-ttu-id="ae27e-123">Bei OpenGL wird das Löschen von Farben getrennt von Zeichnungs Farben mit aufrufen wie " [**glclearcolor**](glclearcolor.md) " und " [**glclearindex**](glclearindex.md)" beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ae27e-123">OpenGL maintains clearing colors separately from drawing colors, with calls like [**glClearColor**](glclearcolor.md) and [**glClearIndex**](glclearindex.md).</span></span> <span data-ttu-id="ae27e-124">Stellen Sie sicher, dass Sie die klar Farbe für jeden Puffer vor dem Löschen festlegen.</span><span class="sxs-lookup"><span data-stu-id="ae27e-124">Be sure to set the clear color for each buffer before clearing.</span></span>
-   <span data-ttu-id="ae27e-125">Anstatt einen von mehreren unterschiedlichen benannten Clear-aufrufen zu verwenden, löschen Sie nun mehrere Puffer mit einem Aufruf, einem [**glClear**](glclear.md)- **oder** -up-Puffer Masken.</span><span class="sxs-lookup"><span data-stu-id="ae27e-125">Instead of using one of several differently named clear calls, you now clear several buffers with one call, [**glClear**](glclear.md), by **OR** ing together buffer masks.</span></span> <span data-ttu-id="ae27e-126">Beispielsweise wird " **czclear** " durch Folgendes ersetzt:</span><span class="sxs-lookup"><span data-stu-id="ae27e-126">For example, **czclear** is replaced by:</span></span>

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   <span data-ttu-id="ae27e-127">IRIS GL verweist auf den Polygon Stippel und die Farb schreibfrage.</span><span class="sxs-lookup"><span data-stu-id="ae27e-127">IRIS GL references the polygon stipple and the color writemask.</span></span> <span data-ttu-id="ae27e-128">OpenGL ignoriert den Polygon-Stippel, verweist jedoch auf die Farb schreibfrage.</span><span class="sxs-lookup"><span data-stu-id="ae27e-128">OpenGL ignores the polygon stipple but references the color writemask.</span></span> <span data-ttu-id="ae27e-129">(Die Funktion " **czclear** " ignoriert sowohl den Polygon Stippel als auch die Farb schreibfrage.)</span><span class="sxs-lookup"><span data-stu-id="ae27e-129">(The **czclear** function ignores both the polygon stipple and the color writemask.)</span></span>

<span data-ttu-id="ae27e-130">In der folgenden Tabelle werden die verschiedenen "IRIS GL Clear"-Funktionen mit ihren entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ae27e-130">The following table lists the various IRIS GL clear functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ae27e-131">IRIS GL-Befehl</span><span class="sxs-lookup"><span data-stu-id="ae27e-131">IRIS GL call</span></span>         | <span data-ttu-id="ae27e-132">OpenGL-Befehl</span><span class="sxs-lookup"><span data-stu-id="ae27e-132">OpenGL call</span></span>                                                               | <span data-ttu-id="ae27e-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ae27e-133">Meaning</span></span>                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ae27e-134">**acbuf**(AC \_ Clear)</span><span class="sxs-lookup"><span data-stu-id="ae27e-134">**acbuf**(AC\_CLEAR)</span></span> | <span data-ttu-id="ae27e-135">**glClear**(GL- \_ Accum- \_ Puffer \_ Bit)</span><span class="sxs-lookup"><span data-stu-id="ae27e-135">**glClear**( GL\_ACCUM\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="ae27e-136">Löschen Sie den Akkumulations Puffer.</span><span class="sxs-lookup"><span data-stu-id="ae27e-136">Clear the accumulation buffer.</span></span>                    |
|                      | <span data-ttu-id="ae27e-137">**glclearcolor**</span><span class="sxs-lookup"><span data-stu-id="ae27e-137">**glClearColor**</span></span>                                                          | <span data-ttu-id="ae27e-138">Legen Sie die RGBA-Clear-Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="ae27e-138">Set the RGBA clear color.</span></span>                         |
|                      | <span data-ttu-id="ae27e-139">**glclearindex**</span><span class="sxs-lookup"><span data-stu-id="ae27e-139">**glClearIndex**</span></span>                                                          | <span data-ttu-id="ae27e-140">Legen Sie den Clear-Color-Index fest.</span><span class="sxs-lookup"><span data-stu-id="ae27e-140">Set the clear-color index.</span></span>                        |
| <span data-ttu-id="ae27e-141">**Löschen**</span><span class="sxs-lookup"><span data-stu-id="ae27e-141">**clear**</span></span>            | <span data-ttu-id="ae27e-142">**glClear**(GL- \_ Farb \_ Puffer \_ Bit)</span><span class="sxs-lookup"><span data-stu-id="ae27e-142">**glClear**( GL\_COLOR\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="ae27e-143">Löschen Sie den Farb Puffer.</span><span class="sxs-lookup"><span data-stu-id="ae27e-143">Clear the color buffer.</span></span>                           |
|                      | <span data-ttu-id="ae27e-144">**glcleartiefe**</span><span class="sxs-lookup"><span data-stu-id="ae27e-144">**glClearDepth**</span></span>                                                          | <span data-ttu-id="ae27e-145">Geben Sie den undeutlichen Wert für den tiefen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="ae27e-145">Specify the clear value for the depth buffer.</span></span>     |
| <span data-ttu-id="ae27e-146">**zclear**</span><span class="sxs-lookup"><span data-stu-id="ae27e-146">**zclear**</span></span>           | <span data-ttu-id="ae27e-147">**glClear**(GL- \_ Tiefe- \_ Puffer \_ Bit)</span><span class="sxs-lookup"><span data-stu-id="ae27e-147">**glClear**( GL\_DEPTH\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="ae27e-148">Löschen Sie den tiefen Puffer.</span><span class="sxs-lookup"><span data-stu-id="ae27e-148">Clear the depth buffer.</span></span>                           |
| <span data-ttu-id="ae27e-149">**czclear**</span><span class="sxs-lookup"><span data-stu-id="ae27e-149">**czclear**</span></span>          | <span data-ttu-id="ae27e-150">**glClear**(GL- \_ Farb \_ Puffer Bit-GL- \_ \| \_ tiefen \_ Puffer \_ Bit)</span><span class="sxs-lookup"><span data-stu-id="ae27e-150">**glClear**( GL\_COLOR\_BUFFER\_BIT \|GL\_DEPTH\_BUFFER\_BIT )</span></span><br/> | <span data-ttu-id="ae27e-151">Löschen Sie den Farb Puffer und den tiefen Puffer.</span><span class="sxs-lookup"><span data-stu-id="ae27e-151">Clear the color buffer and the depth buffer.</span></span>      |
|                      | <span data-ttu-id="ae27e-152">**glclearaccum**</span><span class="sxs-lookup"><span data-stu-id="ae27e-152">**glClearAccum**</span></span>                                                          | <span data-ttu-id="ae27e-153">Geben Sie eindeutige Werte für den Akkumulations Puffer an.</span><span class="sxs-lookup"><span data-stu-id="ae27e-153">Specify clear values for the accumulation buffer.</span></span> |
|                      | <span data-ttu-id="ae27e-154">**glclearstencil**</span><span class="sxs-lookup"><span data-stu-id="ae27e-154">**glClearStencil**</span></span>                                                        | <span data-ttu-id="ae27e-155">Geben Sie den undeutlichen Wert für den Schablonen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="ae27e-155">Specify the clear value for the stencil buffer.</span></span>   |
| <span data-ttu-id="ae27e-156">**sClear**</span><span class="sxs-lookup"><span data-stu-id="ae27e-156">**sclear**</span></span>           | <span data-ttu-id="ae27e-157">**glClear**(GL- \_ Schablone- \_ Puffer \_ Bit)</span><span class="sxs-lookup"><span data-stu-id="ae27e-157">**glClear**( GL\_STENCIL\_BUFFER\_BIT )</span></span>                                   | <span data-ttu-id="ae27e-158">Löschen Sie den Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="ae27e-158">Clear the stencil buffer.</span></span>                         |



 

<span data-ttu-id="ae27e-159">Wenn Ihr IRIS GL-Code sowohl **gclear** als auch **sClear** verwendet, können Sie diese in einem einzelnen **glClear** -Befehl kombinieren. kann die Leistung des Programms verbessern.</span><span class="sxs-lookup"><span data-stu-id="ae27e-159">When your IRIS GL code uses both **gclear** and **sclear**, you can combine them into a single **glClear** call; can improve your program's performance.</span></span>

 

 





