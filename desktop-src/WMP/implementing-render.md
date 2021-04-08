---
title: Implementieren von Rendering
description: Implementieren von Rendering
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- Visualisierungen, zeitgesteuerte Ereignisse
- benutzerdefinierte Visualisierungen, zeitgesteuerte Ereignisse
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Visualisierungen, renderwindow-Funktion
- benutzerdefinierte Visualisierungen, renderwindow-Funktion
- Funktion "Rendering", Parameter
- Renderwindow-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038561"
---
# <a name="implementing-render"></a><span data-ttu-id="2029d-111">Implementieren von Rendering</span><span class="sxs-lookup"><span data-stu-id="2029d-111">Implementing Render</span></span>

<span data-ttu-id="2029d-112">Die einfachste Möglichkeit, die Visualisierungs Programmierung vorzustellen, besteht darin, dass Sie einen Handler für ein Zeit gesteuerter Ereignis erstellen.</span><span class="sxs-lookup"><span data-stu-id="2029d-112">The easiest way to think of visualization programming is that you are creating a handler for a timed event.</span></span> <span data-ttu-id="2029d-113">In bestimmten Intervallen nimmt Windows Media Player eine Momentaufnahme der Audiodaten, die Sie wiedergeben, und stellt die Moment Aufnahmedaten für die aktuell geladene Visualisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="2029d-113">At specific intervals, Windows Media Player takes a snapshot of the audio data it is playing, and provides the snapshot data to the currently loaded visualization.</span></span> <span data-ttu-id="2029d-114">Dies ähnelt der ereignisgesteuerten Programmierung und ist Teil des Programmiermodells von Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2029d-114">This is similar to event-driven programming and is part of the programming model of Microsoft Windows.</span></span> <span data-ttu-id="2029d-115">Sie schreiben Code und warten darauf, dass er von einem bestimmten Ereignis aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2029d-115">You write code and wait for it to be called by a particular event.</span></span>

<span data-ttu-id="2029d-116">Wenn Ihr Code eine Implementierung der [iwmpeffects::](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) Rendering-Funktion für das Rendering im fensterlosen Modus ist, empfängt er die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2029d-116">If your code is an implementation of the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function for rendering in windowless mode, it receives the following parameters:</span></span>

<span data-ttu-id="2029d-117">*Timedlevel*</span><span class="sxs-lookup"><span data-stu-id="2029d-117">*TimedLevel*</span></span>

<span data-ttu-id="2029d-118">Dies ist eine Struktur, die die Audiodaten definiert, die vom Code analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="2029d-118">This is a structure that defines the audio data your code will be analyzing.</span></span> <span data-ttu-id="2029d-119">Die Struktur besteht aus zwei Arrays.</span><span class="sxs-lookup"><span data-stu-id="2029d-119">The structure is composed of two arrays.</span></span> <span data-ttu-id="2029d-120">Das erste Array basiert auf Häufigkeits Informationen und enthält eine Momentaufnahme des Audiospektrums, das in 1024 Teile aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="2029d-120">The first array is based on frequency information and contains a snapshot of the audio spectrum divided into 1024 portions.</span></span> <span data-ttu-id="2029d-121">Jede Zelle des Arrays enthält einen Wert zwischen 0 und 255.</span><span class="sxs-lookup"><span data-stu-id="2029d-121">Each cell of the array contains a value from 0 to 255.</span></span> <span data-ttu-id="2029d-122">Die erste Zelle beginnt bei 20 Hz und der letzte bei 22050 Hz.</span><span class="sxs-lookup"><span data-stu-id="2029d-122">The first cell starts at 20 Hz and the last at 22050 Hz.</span></span> <span data-ttu-id="2029d-123">Das Array ist zweidimensional, um Stereo-Audiodaten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2029d-123">The array is two dimensional to represent stereo audio.</span></span> <span data-ttu-id="2029d-124">Das zweite Array basiert auf Wellenform-Informationen und entspricht der Audioleistung. je stärker die Welle ist, desto größer ist der Wert.</span><span class="sxs-lookup"><span data-stu-id="2029d-124">The second array is based on waveform information and corresponds to audio power, where the stronger the wave is, the larger the value.</span></span> <span data-ttu-id="2029d-125">Das Wellenform-Array ist eine präzise Momentaufnahme der letzten 1024 Slices von audiostromdaten, die in sehr kleinen Zeitintervallen entnommen wurden.</span><span class="sxs-lookup"><span data-stu-id="2029d-125">The waveform array is a granular snapshot of the last 1024 slices of audio power taken at very small time intervals.</span></span> <span data-ttu-id="2029d-126">Dieses Array ist auch zweidimensional, um Stereo-Audiodaten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2029d-126">This array also is two dimensional to represent stereo audio.</span></span>

<span data-ttu-id="2029d-127">*HDC*</span><span class="sxs-lookup"><span data-stu-id="2029d-127">*HDC*</span></span>

<span data-ttu-id="2029d-128">Dies ist ein Microsoft Windows-Handle für einen Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="2029d-128">This is a Microsoft Windows handle to a device context.</span></span> <span data-ttu-id="2029d-129">Dies bietet eine Möglichkeit, die Zeichen Oberfläche für Windows zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2029d-129">This gives a way to identify the drawing surface to Windows.</span></span> <span data-ttu-id="2029d-130">Sie müssen Sie nicht erstellen, sondern nur für bestimmte Zeichnungs Funktionsaufrufe verwenden.</span><span class="sxs-lookup"><span data-stu-id="2029d-130">You do not need to create it, you just need to use it for specific drawing function calls.</span></span>

<span data-ttu-id="2029d-131">*Rect*</span><span class="sxs-lookup"><span data-stu-id="2029d-131">*RECT*</span></span>

<span data-ttu-id="2029d-132">Dies ist ein Microsoft Windows-Rechteck, das die Größe einer Zeichen Oberfläche definiert.</span><span class="sxs-lookup"><span data-stu-id="2029d-132">This is a Microsoft Windows rectangle that defines the size of a drawing surface.</span></span> <span data-ttu-id="2029d-133">Dabei handelt es sich um ein einfaches Rechteck mit vier Eigenschaften: **Links**, **Rechts**, **oben** und **unten**.</span><span class="sxs-lookup"><span data-stu-id="2029d-133">This is a simple rectangle with four properties: **left**, **right**, **top**, and **bottom**.</span></span> <span data-ttu-id="2029d-134">Die tatsächlichen Werte werden von Windows Media Player bereitgestellt, damit Sie bestimmen können, wie der Benutzer oder der Skin-Entwickler das Fenster, das Sie zeichnen, skaliert hat.</span><span class="sxs-lookup"><span data-stu-id="2029d-134">The actual values are supplied by Windows Media Player so that you can determine how the user or skin developer has sized the window you will draw on.</span></span> <span data-ttu-id="2029d-135">Außerdem wird die Position auf dem HDC festgelegt, in der der Effekt dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2029d-135">It also determines the position on the HDC that the effect is supposed to render on.</span></span>

<span data-ttu-id="2029d-136">Wenn Ihr Code eine Implementierung der **IWMPEffects2:: renderwindowed** -Funktion für das Rendering in einem Fenster ist, empfängt er die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="2029d-136">If your code is an implementation of the **IWMPEffects2::RenderWindowed** function for rendering in a window, it receives the following parameters:</span></span>

<span data-ttu-id="2029d-137">*Timedlevel*</span><span class="sxs-lookup"><span data-stu-id="2029d-137">*TimedLevel*</span></span>

<span data-ttu-id="2029d-138">Dies sind die gleichen Informationen, die von der Funktion " **Rendering** " empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="2029d-138">This is the same information that the **Render** function receives.</span></span>

<span data-ttu-id="2029d-139">*frequiredrender*</span><span class="sxs-lookup"><span data-stu-id="2029d-139">*fRequiredRender*</span></span>

<span data-ttu-id="2029d-140">Der Parameter " *frequiredrender* " informiert Sie darüber, dass sich ihre Visualisierung selbst neu zeichnen muss, z. –. Wenn ein anderes Fenster darauf gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="2029d-140">The *fRequiredRender* parameter informs you that your visualization must repaint itself—for example, when another window is dragged over it.</span></span> <span data-ttu-id="2029d-141">Wenn dieser Wert false ist, können Sie den Renderingcode gefahrlos überspringen, wenn das aktuelle Medien Element beendet oder angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="2029d-141">When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused.</span></span> <span data-ttu-id="2029d-142">So können Sie unnötige CPU-Zyklen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2029d-142">This lets you avoid consuming CPU cycles unnecessarily.</span></span>

<span data-ttu-id="2029d-143">Das Beispiel-Plug-in, das vom Plug-in-Assistenten generiert wurde, stellt keine benutzerdefinierte Implementierung für **renderwindowed** bereit.</span><span class="sxs-lookup"><span data-stu-id="2029d-143">The sample plug-in generated by the Plug-in Wizard does not provide a custom implementation for **RenderWindowed**.</span></span> <span data-ttu-id="2029d-144">Stattdessen ruft der Beispiel-Plug-in-Code den Gerätekontext aus dem übergeordneten Fenster ab, das von der Windows-Media Player in [IWMPEffects2:: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)bereitgestellt wird. Anschließend wird die Dimension des übergeordneten Fensters als Rect-Struktur abgerufen, und dann wird aufgerufen **, um mithilfe** des Geräte Kontexts, des Rect und des Zeigers auf der Zeitüberschreitung von **renderwindowed** geren</span><span class="sxs-lookup"><span data-stu-id="2029d-144">Instead, the sample plug-in code retrieves the device context from the parent window provided by Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), then retrieves the dimensions of the parent window as a RECT structure, and then calls through to **Render** using the device context, the RECT, and the timed level pointer from **RenderWindowed**.</span></span>

<span data-ttu-id="2029d-145">In den folgenden Abschnitten finden Sie weitere Informationen zur Implementierung von " **Rendering**":</span><span class="sxs-lookup"><span data-stu-id="2029d-145">The following sections provide more information about implementing **Render**:</span></span>

-   [<span data-ttu-id="2029d-146">Verwenden von zeitgesteuerten Ebenen</span><span class="sxs-lookup"><span data-stu-id="2029d-146">Using Timed Levels</span></span>](using-timed-levels.md)
-   [<span data-ttu-id="2029d-147">Verwenden von Geräte Kontexten</span><span class="sxs-lookup"><span data-stu-id="2029d-147">Using Device Contexts</span></span>](using-device-contexts.md)
-   [<span data-ttu-id="2029d-148">Verwenden von Rechtecke</span><span class="sxs-lookup"><span data-stu-id="2029d-148">Using Rectangles</span></span>](using-rectangles.md)
-   [<span data-ttu-id="2029d-149">Beispiel-Rendering-Code</span><span class="sxs-lookup"><span data-stu-id="2029d-149">Sample Render Code</span></span>](sample-render-code.md)

## <a name="related-topics"></a><span data-ttu-id="2029d-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2029d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2029d-151">**Implementieren des Codes**</span><span class="sxs-lookup"><span data-stu-id="2029d-151">**Implementing Your Code**</span></span>](implementing-your-code.md)
</dt> </dl>

 

 




