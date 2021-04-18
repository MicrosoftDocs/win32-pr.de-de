---
title: Portieren von Mischungs Code
description: Wenn Sie in IRIS gl auf den vorderen und den Hintergrund Puffer zeichnen, wird der Mischungs Vorgang durch das Lesen eines der Puffer, das Kombination mit dieser Farbe und das anschließende Schreiben des Ergebnisses in beide Puffer erfolgt. In OpenGL wird jeder Puffer jedoch nacheinander gelesen, gemischt und dann geschrieben.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- IRIS GL portieren, mischen
- Portieren von IRIS GL, Blending
- Portieren auf OpenGL von IRIS GL, Blending
- OpenGL-Portierung von IRIS GL, Blending
- Mischen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338612"
---
# <a name="porting-blending-code"></a><span data-ttu-id="1f148-109">Portieren von Mischungs Code</span><span class="sxs-lookup"><span data-stu-id="1f148-109">Porting Blending Code</span></span>

<span data-ttu-id="1f148-110">Wenn Sie in IRIS gl auf den vorderen und den Hintergrund Puffer zeichnen, wird der Mischungs Vorgang durch das Lesen eines der Puffer, das Kombination mit dieser Farbe und das anschließende Schreiben des Ergebnisses in beide Puffer erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1f148-110">In IRIS GL, when drawing to both front and back buffers, blending is done by reading one of the buffers, blending with that color, and then writing the result to both buffers.</span></span> <span data-ttu-id="1f148-111">In OpenGL wird jeder Puffer jedoch nacheinander gelesen, gemischt und dann geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1f148-111">In OpenGL, however, each buffer is read in turn, blended, and then written.</span></span>

<span data-ttu-id="1f148-112">In der folgenden Tabelle werden die Mischungs Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1f148-112">The following table lists IRIS GL blending functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="1f148-113">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f148-113">IRIS GL function</span></span>  | <span data-ttu-id="1f148-114">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f148-114">OpenGL function</span></span>                            | <span data-ttu-id="1f148-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1f148-115">Meaning</span></span>                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | <span data-ttu-id="1f148-116">[**glEnable**](glenable.md) (GL \_ Blend)</span><span class="sxs-lookup"><span data-stu-id="1f148-116">[**glEnable**](glenable.md) ( GL\_BLEND )</span></span> | <span data-ttu-id="1f148-117">Schaltet das Mischen ein.</span><span class="sxs-lookup"><span data-stu-id="1f148-117">Turns on blending.</span></span>          |
| <span data-ttu-id="1f148-118">**BLENDFUNCTION**</span><span class="sxs-lookup"><span data-stu-id="1f148-118">**blendfunction**</span></span> | [<span data-ttu-id="1f148-119">**glblendfunc**</span><span class="sxs-lookup"><span data-stu-id="1f148-119">**glBlendFunc**</span></span>](glblendfunc.md)         | <span data-ttu-id="1f148-120">Gibt eine Blend-Funktion an.</span><span class="sxs-lookup"><span data-stu-id="1f148-120">Specifies a blend function.</span></span> |



 

<span data-ttu-id="1f148-121">Die OpenGL-Funktion " **glblendfunc** " und die Iris GL **BLENDFUNCTION** -Funktion sind nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="1f148-121">The OpenGL **glBlendFunc** function and the IRIS GL **blendfunction** function are almost identical.</span></span> <span data-ttu-id="1f148-122">Die folgende Tabelle enthält die Iris GL-Faktoren und deren OpenGL-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="1f148-122">The following table lists IRIS GL blend factors and their OpenGL equivalents.</span></span>



| <span data-ttu-id="1f148-123">IRIS GL</span><span class="sxs-lookup"><span data-stu-id="1f148-123">IRIS GL</span></span>          | <span data-ttu-id="1f148-124">OpenGL</span><span class="sxs-lookup"><span data-stu-id="1f148-124">OpenGL</span></span>                     | <span data-ttu-id="1f148-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f148-125">Notes</span></span>             |
|------------------|----------------------------|-------------------|
| <span data-ttu-id="1f148-126">BF \_ null</span><span class="sxs-lookup"><span data-stu-id="1f148-126">BF\_ZERO</span></span>         | <span data-ttu-id="1f148-127">GL \_ null</span><span class="sxs-lookup"><span data-stu-id="1f148-127">GL\_ZERO</span></span>                   |                   |
| <span data-ttu-id="1f148-128">BF- \_ 1</span><span class="sxs-lookup"><span data-stu-id="1f148-128">BF\_ONE</span></span>          | <span data-ttu-id="1f148-129">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="1f148-129">GL\_ONE</span></span>                    |                   |
| <span data-ttu-id="1f148-130">BF \_ sa</span><span class="sxs-lookup"><span data-stu-id="1f148-130">BF\_SA</span></span>           | <span data-ttu-id="1f148-131">GL \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="1f148-131">GL\_SRC\_ALPHA</span></span>             |                   |
| <span data-ttu-id="1f148-132">BF- \_ MSA</span><span class="sxs-lookup"><span data-stu-id="1f148-132">BF\_MSA</span></span>          | <span data-ttu-id="1f148-133">GL \_ One \_ minus \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="1f148-133">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> |                   |
| <span data-ttu-id="1f148-134">BF- \_ da</span><span class="sxs-lookup"><span data-stu-id="1f148-134">BF\_DA</span></span>           | <span data-ttu-id="1f148-135">GL- \_ DST- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="1f148-135">GL\_DST\_ALPHA</span></span>             |                   |
| <span data-ttu-id="1f148-136">BF- \_ MDA</span><span class="sxs-lookup"><span data-stu-id="1f148-136">BF\_MDA</span></span>          | <span data-ttu-id="1f148-137">GL \_ 1 \_ minus \_ DST- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="1f148-137">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> |                   |
| <span data-ttu-id="1f148-138">BF \_ SC</span><span class="sxs-lookup"><span data-stu-id="1f148-138">BF\_SC</span></span>           | <span data-ttu-id="1f148-139">GL- \_ src- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="1f148-139">GL\_SRC\_COLOR</span></span>             |                   |
| <span data-ttu-id="1f148-140">BF \_ MSC</span><span class="sxs-lookup"><span data-stu-id="1f148-140">BF\_MSC</span></span>          | <span data-ttu-id="1f148-141">GL \_ 1 \_ minus \_ src- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="1f148-141">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="1f148-142">Nur Ziel.</span><span class="sxs-lookup"><span data-stu-id="1f148-142">Destination only.</span></span> |
| <span data-ttu-id="1f148-143">BF- \_ DC</span><span class="sxs-lookup"><span data-stu-id="1f148-143">BF\_DC</span></span>           | <span data-ttu-id="1f148-144">GL- \_ DST- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="1f148-144">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="1f148-145">Nur Quelle.</span><span class="sxs-lookup"><span data-stu-id="1f148-145">Source only.</span></span>      |
| <span data-ttu-id="1f148-146">BF- \_ MDC</span><span class="sxs-lookup"><span data-stu-id="1f148-146">BF\_MDC</span></span>          | <span data-ttu-id="1f148-147">GL \_ 1 \_ minus \_ DST- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="1f148-147">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="1f148-148">Nur Quelle.</span><span class="sxs-lookup"><span data-stu-id="1f148-148">Source only.</span></span>      |
| <span data-ttu-id="1f148-149">BF \_ Min. \_ sa- \_ MDA</span><span class="sxs-lookup"><span data-stu-id="1f148-149">BF\_MIN\_SA\_MDA</span></span> | <span data-ttu-id="1f148-150">GL \_ src \_ alpha- \_ vollständig</span><span class="sxs-lookup"><span data-stu-id="1f148-150">GL\_SRC\_ALPHA\_SATURATE</span></span>   |                   |



 

<span data-ttu-id="1f148-151">??</span><span class="sxs-lookup"><span data-stu-id="1f148-151">??</span></span>

 

 




