---
title: Entwickler Übersicht
description: Entwickler Übersicht
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Windows Media Player-Plug-ins, Visualisierungen
- Plug-ins, Visualisierungen
- Visualisierungen, Übersicht über Entwickler
- benutzerdefinierte Visualisierungen, Übersicht über Entwickler
- Visualisierungen, com-Steuerelemente
- benutzerdefinierte Visualisierungen, com-Steuerelemente
- Visualisierungen, Audioeingabe
- benutzerdefinierte Visualisierungen, Audioeingabe
- Visualisierungen, grafische Ausgabe
- benutzerdefinierte Visualisierungen, grafische Ausgabe
- Visualisierungen, Zeichnungs Tools
- benutzerdefinierte Visualisierungen, Zeichnungs Tools
- Visualisierungen, Programmiersprache
- benutzerdefinierte Visualisierungen, Programmiersprache
- Visualisierungen, Visual C++
- benutzerdefinierte Visualisierungen, Visual C++
- Visualisierungen, Plug-in-Assistent
- benutzerdefinierte Visualisierungen, Plug-in-Assistent
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310599"
---
# <a name="developer-overview"></a><span data-ttu-id="e1280-122">Entwickler Übersicht</span><span class="sxs-lookup"><span data-stu-id="e1280-122">Developer Overview</span></span>

<span data-ttu-id="e1280-123">Aus Sicht des Entwicklers sind Visualisierungen Softwareprogramme, die von Windows bereitgestellte Audiodaten akzeptieren Media Player und diese Daten in Grafiken konvertieren, um den Benutzer zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="e1280-123">From the developer's point of view, visualizations are software programs that take audio data provided by Windows Media Player and convert that data to graphics that will please the eye of the user.</span></span> <span data-ttu-id="e1280-124">Die wichtigsten Aspekte, die ein Entwickler kennen muss, um eine neue Visualisierung zu erstellen, sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="e1280-124">The main subjects a developer needs to understand to create a new visualization are the following:</span></span>

## <a name="visualization-packaging"></a><span data-ttu-id="e1280-125">Visualisierungs Verpackung</span><span class="sxs-lookup"><span data-stu-id="e1280-125">Visualization Packaging</span></span>

<span data-ttu-id="e1280-126">Visualisierungen sind com-Steuerelemente, die von Windows Media Player verwendet werden, um Audiowellen Formen in animierte Grafiken in Microsoft Windows umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="e1280-126">Visualizations are COM controls that Windows Media Player uses to turn audio waveforms into animated graphics in Microsoft Windows.</span></span> <span data-ttu-id="e1280-127">Die com-Steuerelemente werden als Microsoft Windows Dynamic-Link Libraries (DLLs) verpackt und müssen in der Windows-Registrierung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e1280-127">The COM controls are packaged as Microsoft Windows dynamic-link libraries (DLLs) and must be registered in the Windows registry.</span></span> <span data-ttu-id="e1280-128">Beim Ausführen von Windows Media Player werden registrierte benutzerdefinierte Visualisierungen geladen und entsprechend den Anweisungen der von Windows Media Player verwendeten Skin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1280-128">When Windows Media Player runs, registered custom visualizations are loaded and viewed in accordance with the instructions of the skin that Windows Media Player is using.</span></span>

## <a name="audio-input"></a><span data-ttu-id="e1280-129">Audioeingabe</span><span class="sxs-lookup"><span data-stu-id="e1280-129">Audio Input</span></span>

<span data-ttu-id="e1280-130">Windows Media Player bietet Ihren Code Momentaufnahmen von audiohäufigkeit und Wellenform Daten in zeitlich begrenzten Intervallen, gemessen in Sekundenbruchteilen.</span><span class="sxs-lookup"><span data-stu-id="e1280-130">Windows Media Player provides your code with snapshots of audio frequency and waveform data at timed intervals measured in fractions of a second.</span></span> <span data-ttu-id="e1280-131">Das Momentaufnahme Intervall wird intern vom Windows-Media Player festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1280-131">The snapshot interval is internally determined by the Windows Media Player.</span></span>

## <a name="graphical-output"></a><span data-ttu-id="e1280-132">Grafische Ausgabe</span><span class="sxs-lookup"><span data-stu-id="e1280-132">Graphical Output</span></span>

<span data-ttu-id="e1280-133">Die grafische Ausgabe der Visualisierung ist ein Microsoft Windows-Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="e1280-133">The graphical output from your visualization is a Microsoft Windows device context.</span></span> <span data-ttu-id="e1280-134">Dies ist eine standardmäßige Windows-Zeichen Oberfläche, die Sie bei jeder Bereitstellung einer audiomomentaufnahme zeichnen können.</span><span class="sxs-lookup"><span data-stu-id="e1280-134">This is a standard Windows drawing surface that you can draw upon every time an audio snapshot is provided.</span></span> <span data-ttu-id="e1280-135">Alle Hintergrund-Windows-Technologien werden für Sie erledigt.</span><span class="sxs-lookup"><span data-stu-id="e1280-135">All of the background Windows technology is taken care of for you.</span></span> <span data-ttu-id="e1280-136">Sie müssen lediglich den Gerätekontext mit den bereitgestellten Audiodaten zeichnen.</span><span class="sxs-lookup"><span data-stu-id="e1280-136">You just have to draw on the device context with the audio data provided.</span></span>

## <a name="drawing-tools"></a><span data-ttu-id="e1280-137">Zeichnungs Tools</span><span class="sxs-lookup"><span data-stu-id="e1280-137">Drawing Tools</span></span>

<span data-ttu-id="e1280-138">Sie können den Gerätekontext mit standardmäßigen Microsoft Windows Graphics Device Interface (GDI)-Funktionen zeichnen, indem Sie Stifte und Pinsel verwenden, um Entwürfe zu erstellen, die von den Audiodaten geändert werden, die Ihnen von Windows Media Player bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e1280-138">You can draw on the device context with standard Microsoft Windows Graphics Device Interface (GDI) functions, using pens and brushes to create designs that are modified by the audio data supplied to you by Windows Media Player.</span></span> <span data-ttu-id="e1280-139">GDI stellt einen umfangreichen Satz von Zeichnungs Tools bereit, die viele Arten von visuellen Effekten erzeugen können.</span><span class="sxs-lookup"><span data-stu-id="e1280-139">GDI provides a rich set of drawing tools that can create many kinds of visual effects.</span></span>

## <a name="programming-language"></a><span data-ttu-id="e1280-140">Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="e1280-140">Programming Language</span></span>

<span data-ttu-id="e1280-141">Microsoft Visual C++ 6,0 und höher ist die einzige unterstützte Sprache zum Erstellen von benutzerdefinierten Visualisierungen.</span><span class="sxs-lookup"><span data-stu-id="e1280-141">Microsoft Visual C++ 6.0 and higher is the only supported language for creating custom visualizations.</span></span>

## <a name="plug-in-wizard"></a><span data-ttu-id="e1280-142">Plug-in-Assistent</span><span class="sxs-lookup"><span data-stu-id="e1280-142">Plug-in Wizard</span></span>

<span data-ttu-id="e1280-143">Windows Media Player stellt einen com-Assistenten bereit, den Sie Visual C++ hinzufügen können, der den zugrunde liegenden Code generiert, der für ihre Visualisierung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e1280-143">Windows Media Player provides a COM wizard that you can add to Visual C++ that will generate the underlying code needed for your visualization.</span></span> <span data-ttu-id="e1280-144">Es werden nicht nur alle Quelldateien bereitgestellt, sondern es wird eine Beispiel Skin generiert, um das Testen der Visualisierung zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="e1280-144">Not only are all source files provided, but a sample skin is generated to make it easy to test your visualization.</span></span> <span data-ttu-id="e1280-145">Der generierte Code erstellt eine Visualisierung ähnlich wie Balken mit zwei Voreinstellungen.</span><span class="sxs-lookup"><span data-stu-id="e1280-145">The generated code creates a visualization similar to Bars, with two presets.</span></span> <span data-ttu-id="e1280-146">Anschließend können Sie den Code ändern, um eine eigene Visualisierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1280-146">You can then modify the code to create your own visualization.</span></span> <span data-ttu-id="e1280-147">Außerdem wird eine Registrierungsdatei generiert, um die Visualisierung zu registrieren, sodass Sie von Windows Media Player geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e1280-147">A registry file is also generated to register your visualization so that Windows Media Player can load it.</span></span>

<span data-ttu-id="e1280-148">Im folgenden Thema wird beschrieben, wie Visualisierungs Code Audiodaten verarbeitet:</span><span class="sxs-lookup"><span data-stu-id="e1280-148">The following topic describes how visualization code processes audio data:</span></span>

-   [<span data-ttu-id="e1280-149">Ablauf Steuerung</span><span class="sxs-lookup"><span data-stu-id="e1280-149">Flow of Control</span></span>](flow-of-control.md)

## <a name="related-topics"></a><span data-ttu-id="e1280-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1280-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1280-151">**Informationen zu benutzerdefinierten Visualisierungen**</span><span class="sxs-lookup"><span data-stu-id="e1280-151">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




