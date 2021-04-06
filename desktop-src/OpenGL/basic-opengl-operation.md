---
title: Grundlegender OpenGL-Vorgang
description: Grundlegender OpenGL-Vorgang
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, grundlegende Vorgänge
- OpenGL, Datenverarbeitung
- OpenGL, Verarbeitungsphasen
- OpenGL, Anzeigen von Listen
- Anzeigelisten OpenGL
- OpenGL, Evaluators
- Evaluatoren OpenGL
- OpenGL-Vorgänge pro Scheitelpunkt
- pro-Vertex-Vorgänge OpenGL
- OpenGL, primitive Assembly
- primitiver Assembly OpenGL
- OpenGL, rasterization
- Rasterung OpenGL
- OpenGL-Vorgänge pro Fragment
- pro-Fragment-Vorgänge OpenGL
- Framebuffers, grundlegende Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961072"
---
# <a name="basic-opengl-operation"></a><span data-ttu-id="cc4ca-119">Grundlegender OpenGL-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cc4ca-119">Basic OpenGL Operation</span></span>

<span data-ttu-id="cc4ca-120">Im folgenden Diagramm wird veranschaulicht, wie OpenGL Daten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-120">The following diagram illustrates how OpenGL processes data.</span></span> <span data-ttu-id="cc4ca-121">Wie gezeigt, geben Befehle von Links aus ein und durchlaufen eine Verarbeitungs Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-121">As shown, commands enter from the left and proceed through a processing pipeline.</span></span> <span data-ttu-id="cc4ca-122">Einige Befehle geben geometrische Objekte an, die gezeichnet werden sollen, und andere Steuern, wie die Objekte während verschiedener Verarbeitungsphasen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-122">Some commands specify geometric objects to be drawn, and others control how the objects are handled during various processing stages.</span></span>

![Diagramm mit den OpenGL-Datenverarbeitungs-Pipeline Stufen.](images/basic01.png)

<span data-ttu-id="cc4ca-124">Die Verarbeitungsstufen im grundlegenden OpenGL-Vorgang lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cc4ca-124">The processing stages in basic OpenGL operation are as follows:</span></span>

-   <span data-ttu-id="cc4ca-125">**Liste anzeigen** Anstatt alle Befehle direkt durch die Pipeline zu übertragen, können Sie einige davon in einer Anzeigeliste für die spätere Verarbeitung sammeln.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-125">**Display list** Rather than having all commands proceed immediately through the pipeline, you can choose to accumulate some of them in a display list for processing later.</span></span>
-   <span data-ttu-id="cc4ca-126">**Evaluator** Die Auswertungs Phase der Verarbeitung bietet eine effiziente Möglichkeit, um die Kurven-und Oberflächengeometrie durch Auswerten von polynomialen Befehlen von Eingabe Werten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-126">**Evaluator** The evaluator stage of processing provides an efficient way to approximate curve and surface geometry by evaluating polynomial commands of input values.</span></span>
-   <span data-ttu-id="cc4ca-127">**Pro-Vertex-Vorgänge und primitive Assembly** OpenGL verarbeitet geometrische primitivespunkte, Liniensegmente und polygonsalle, die von Vertices beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-127">**Per-vertex operations and primitive assembly** OpenGL processes geometric primitivespoints, line segments, and polygonsall of which are described by vertices.</span></span> <span data-ttu-id="cc4ca-128">Vertices werden transformiert und beleuchtet, und primitive werden auf den Viewport zugeschnitten, um die rasterisierung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-128">Vertices are transformed and lit, and primitives are clipped to the viewport in preparation for rasterization.</span></span>
-   <span data-ttu-id="cc4ca-129">**Rasterisierung** Die Rasterung-Phase erzeugt eine Reihe von Frame Puffer Adressen und zugeordneten Werten unter Verwendung einer zweidimensionalen Beschreibung eines Punkts, eines Linien Segments oder eines Polygons.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-129">**Rasterization** The rasterization stage produces a series of frame-buffer addresses and associated values using a two-dimensional description of a point, line segment, or polygon.</span></span> <span data-ttu-id="cc4ca-130">Jedes Fragment, das erstellt wird, wird in die letzte Phase, pro-Fragment-Vorgängen, eingefügt.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-130">Each fragment so produced is fed into the last stage, per-fragment operations.</span></span>
-   <span data-ttu-id="cc4ca-131">**Vorgänge pro Fragment** Dies sind die abschließenden Vorgänge, die für die Daten ausgeführt werden, bevor Sie als Pixel im Framebuffer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-131">**Per-fragment operations** These are the final operations performed on the data before it is stored as pixels in the framebuffer.</span></span>

    <span data-ttu-id="cc4ca-132">Pro-Fragment-Vorgänge enthalten bedingte Aktualisierungen des framepufferers auf der Grundlage eingehender und zuvor gespeicherter z-Werte (bei z-Pufferung) und der Mischung eingehender Pixel Farben mit gespeicherten Farben sowie Maskierung und anderen logischen Vorgängen bei Pixelwerten.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-132">Per-fragment operations include conditional updates to the framebuffer based on incoming and previously stored z values (for z buffering) and blending of incoming pixel colors with stored colors, as well as masking and other logical operations on pixel values.</span></span>

<span data-ttu-id="cc4ca-133">Daten können in Form von Pixeln anstelle von Vertices eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-133">Data can be input in the form of pixels rather than vertices.</span></span> <span data-ttu-id="cc4ca-134">Daten in Form von Pixeln, wie z. b. ein Bild zur Verwendung in der Textur Zuordnung beschreiben, überspringen die erste Phase der oben beschriebenen Verarbeitung und werden stattdessen als Pixel in der Phase Pixel Vorgänge verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-134">Data in the form of pixels, such as might describe an image for use in texture mapping, skips the first stage of processing described above and instead is processed as pixels, in the pixel operations stage.</span></span> <span data-ttu-id="cc4ca-135">Die Pixeldaten sind folgende Pixel Vorgänge:</span><span class="sxs-lookup"><span data-stu-id="cc4ca-135">Following pixel operations, the pixel data is either:</span></span>

-   <span data-ttu-id="cc4ca-136">Wird als Texturspeicher für die Verwendung in der Rasterung-Phase gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-136">Stored as texture memory, for use in the rasterization stage.</span></span>
-   <span data-ttu-id="cc4ca-137">Rasterized, wobei die resultierenden Fragmente in den Frame Puffer zusammengeführt werden, als ob Sie aus geometrischen Daten generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cc4ca-137">Rasterized, with the resulting fragments merged into the framebuffer just as if they were generated from geometric data.</span></span>

 

 




