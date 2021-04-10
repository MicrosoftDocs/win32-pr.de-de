---
description: Beispiel für einen Synthesizer
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Beispiel für einen Synthesizer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868519"
---
# <a name="synth-filter-sample"></a><span data-ttu-id="ad427-103">Beispiel für einen Synthesizer</span><span class="sxs-lookup"><span data-stu-id="ad427-103">Synth Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="ad427-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad427-104">Description</span></span>

<span data-ttu-id="ad427-105">Der synfilterfilter ist ein Quell Filter, der audiowaveforms generiert.</span><span class="sxs-lookup"><span data-stu-id="ad427-105">The Synth filter is a source filter that generates audio waveforms.</span></span>

<span data-ttu-id="ad427-106">Dieser Filter veranschaulicht das dynamische Diagramm.</span><span class="sxs-lookup"><span data-stu-id="ad427-106">This filter illustrates dynamic graph building.</span></span> <span data-ttu-id="ad427-107">Er kann zwischen nicht komprimiertem PCM-Audiodaten und komprimiertem MS \_ ADPCM-Format (Microsoft Adaptive Delta Pulse Code Modulation) wechseln.</span><span class="sxs-lookup"><span data-stu-id="ad427-107">It can switch between uncompressed PCM audio and compressed MS\_ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) format.</span></span>

<span data-ttu-id="ad427-108">Dieser Filter wird in GraphEdit als "audiosynthesizer-Filter" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad427-108">This filter appears in GraphEdit as "Audio Synthesizer Filter."</span></span>

<span data-ttu-id="ad427-109">Weitere Informationen zum Aufbau dynamischer Diagramme finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="ad427-109">For more information about dynamic graph building, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="usage"></a><span data-ttu-id="ad427-110">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="ad427-110">Usage</span></span>

<span data-ttu-id="ad427-111">Mithilfe des synthingfilters kann der Benutzer die Wellenform, Häufigkeit, Anzahl der Kanäle und andere Eigenschaften über die Eigenschaften Seite festlegen.</span><span class="sxs-lookup"><span data-stu-id="ad427-111">The Synth filter enables the user to set the waveform, frequency, number of channels, and other properties through the property page.</span></span> <span data-ttu-id="ad427-112">Halten Sie die UMSCHALTTASTE gedrückt, während Sie den Schieberegler für die Häufigkeit anpassen.</span><span class="sxs-lookup"><span data-stu-id="ad427-112">To set either the upper or lower endpoint of the swept frequency range, hold down SHIFT while adjusting the frequency slider.</span></span> <span data-ttu-id="ad427-113">Der Filter unterstützt auch eine benutzerdefinierte Schnittstelle, ISynth2, um diese Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ad427-113">The filter also supports a custom interface, ISynth2, for setting these properties.</span></span>

<span data-ttu-id="ad427-114">Führen Sie die folgenden Schritte aus, um die Funktion zum entwickeln dynamischer Diagramme zu veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="ad427-114">To demonstrate the dynamic graph building feature, do the following:</span></span>

1.  <span data-ttu-id="ad427-115">Erstellen Sie den Filter, und registrieren Sie ihn mit dem regsvr32-Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="ad427-115">Build the filter and register it with the Regsvr32 utility.</span></span>
2.  <span data-ttu-id="ad427-116">Starten Sie GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="ad427-116">Launch GraphEdit.</span></span>
3.  <span data-ttu-id="ad427-117">Fügen Sie den audiosynthesizer-Filter ein.</span><span class="sxs-lookup"><span data-stu-id="ad427-117">Insert the Audio Synthesizer filter.</span></span> <span data-ttu-id="ad427-118">Sie wird in der Kategorie DirectShow-Filter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad427-118">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="ad427-119">Renderdas Ausgabe-PIN des Filters.</span><span class="sxs-lookup"><span data-stu-id="ad427-119">Render the filter's output pin.</span></span>
5.  <span data-ttu-id="ad427-120">Klicken Sie auf die Schaltfläche **abspielen** .</span><span class="sxs-lookup"><span data-stu-id="ad427-120">Click the **Play** button.</span></span>
6.  <span data-ttu-id="ad427-121">Öffnen Sie die Eigenschaften Seite des Filters.</span><span class="sxs-lookup"><span data-stu-id="ad427-121">Open the filter's property page.</span></span>
7.  <span data-ttu-id="ad427-122">Wählen Sie im Bereich Ausgabe Format die Option PCM oder Microsoft ADPCM aus.</span><span class="sxs-lookup"><span data-stu-id="ad427-122">In the Output Format area, select PCM or Microsoft ADPCM.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="ad427-123">Programmier Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad427-123">Programming Notes</span></span>

<span data-ttu-id="ad427-124">Dieses Beispiel enthält die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="ad427-124">This sample contains the following files:</span></span>

-   <span data-ttu-id="ad427-125">Dynsrc. h, dynsrc. cpp: enthält zwei Basisklassen für Quell Filter, die die dynamische Diagramm Erbauung, cdynamicsource und cdynamicsourcestream unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ad427-125">Dynsrc.h, Dynsrc.cpp: Contains two base classes for source filters that support dynamic graph building, CDynamicSource and CDynamicSourceStream.</span></span>
-   <span data-ttu-id="ad427-126">Isynth. h: deklariert die benutzerdefinierte ISynth2-Schnittstelle für das Festlegen von Eigenschaften für den Filter.</span><span class="sxs-lookup"><span data-stu-id="ad427-126">ISynth.h: Declares the custom ISynth2 interface for setting properties on the filter.</span></span>
-   <span data-ttu-id="ad427-127">Resource. h: enthält Ressourcen Konstanten.</span><span class="sxs-lookup"><span data-stu-id="ad427-127">Resource.h: Contains resource constants.</span></span>
-   <span data-ttu-id="ad427-128">Synth. DEF: exportiert die DLL-Funktionen, die von der com-Bibliothek benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad427-128">Synth.def: Exports the DLL functions needed by the COM library.</span></span>
-   <span data-ttu-id="ad427-129">Synth. h, Synth. cpp: enthält die caudiosynth-Klasse, die die Audiodaten generiert, und die csynthfilter-Klasse, die den Filter implementiert.</span><span class="sxs-lookup"><span data-stu-id="ad427-129">Synth.h, Synth.cpp: Contains the CAudioSynth class, which generates the audio data, and the CSynthFilter class, which implements the filter.</span></span>
-   <span data-ttu-id="ad427-130">Synth. RC: enthält Ressourcen, die vom Filter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad427-130">Synth.rc: Contains resources used by the filter.</span></span>
-   <span data-ttu-id="ad427-131">Synthprp. h, synthprp. cpp: Implementiert die Eigenschaften Seite des Filters.</span><span class="sxs-lookup"><span data-stu-id="ad427-131">Synthprp.h, Synthprp.cpp: Implements the filter's property page.</span></span>

<span data-ttu-id="ad427-132">Die cdynamicsource-Klasse wird von der [**CSource**](csource.md) -Basisklasse angepasst.</span><span class="sxs-lookup"><span data-stu-id="ad427-132">The CDynamicSource class is adapted from the [**CSource**](csource.md) base class.</span></span> <span data-ttu-id="ad427-133">Sie verwendet mindestens einen aus der cdynamicsourcestream-Klasse abgeleiteten Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="ad427-133">It uses one or more output pins derived from the CDynamicSourceStream class.</span></span> <span data-ttu-id="ad427-134">Die cdynamicsourcestream-Klasse wird von der [**csourcestream**](csourcestream.md) -Klasse angepasst, wird jedoch von der [**cdynamicoutputpin**](cdynamicoutputpin.md) -Klasse anstelle der [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ad427-134">The CDynamicSourceStream class is adapted from the [**CSourceStream**](csourcestream.md) class, but derives from the [**CDynamicOutputPin**](cdynamicoutputpin.md) class rather than the [**CBaseOutputPin**](cbaseoutputpin.md) class.</span></span>

<span data-ttu-id="ad427-135">Die cdynamicsource-Klasse verfügt über die folgenden Methoden, die in [**CSource**](csource.md)nicht gefunden werden:</span><span class="sxs-lookup"><span data-stu-id="ad427-135">The CDynamicSource class has the following methods not found in [**CSource**](csource.md):</span></span>

-   <span data-ttu-id="ad427-136">Stop: signalisiert das Stop-Ereignis ([**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md)) und fährt den Arbeits Thread für alle nicht verbundenen Pins herunter.</span><span class="sxs-lookup"><span data-stu-id="ad427-136">Stop: Signals the stop event ([**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md)), and shuts down the worker thread for all unconnected pins.</span></span> <span data-ttu-id="ad427-137">Bei einer verbundenen PIN wird der Arbeitsthread von der inaktiven PIN der PIN heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="ad427-137">On a connected pin, the pin's Inactive method will shut down the worker thread.</span></span>
-   <span data-ttu-id="ad427-138">Anhalten: setzt das anhalteereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="ad427-138">Pause: Resets the stop event.</span></span>
-   <span data-ttu-id="ad427-139">Joinfiltergraph: Ruft die [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md) -Methode für jede PIN auf.</span><span class="sxs-lookup"><span data-stu-id="ad427-139">JoinFilterGraph: Calls the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method on each pin.</span></span>

<span data-ttu-id="ad427-140">Die cdynamicsourcestream-Klasse verfügt über die folgenden Methoden, die nicht in [**csourcestream**](csourcestream.md)gefunden wurden:</span><span class="sxs-lookup"><span data-stu-id="ad427-140">The CDynamicSourceStream class has the following methods not found in [**CSourceStream**](csourcestream.md):</span></span>

-   <span data-ttu-id="ad427-141">Destroysourcethread: schließt den Arbeits Thread.</span><span class="sxs-lookup"><span data-stu-id="ad427-141">DestroySourceThread: Shuts down the worker thread.</span></span>
-   <span data-ttu-id="ad427-142">FatalError: signalisiert dem Filter Diagramm-Manager einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="ad427-142">FatalError: Signals an error to the filter graph manager.</span></span>
-   <span data-ttu-id="ad427-143">Outputpinneedstobereconnected: signalisiert, dass die Ausgabe-PIN erneut verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad427-143">OutputPinNeedsToBeReconnected: Signals that the output pin should be reconnected.</span></span> <span data-ttu-id="ad427-144">Wenn diese Methode aufgerufen wird, ruft der Arbeits Thread die [**cdynamicoutputpin::D ynamikreconnect**](cdynamicoutputpin-dynamicreconnect.md) -Methode auf, um die PIN erneut zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ad427-144">When this method is called, the worker thread calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to reconnect the pin.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="ad427-145">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ad427-145">Downloading the Sample</span></span>

<span data-ttu-id="ad427-146">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad427-146">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="ad427-147">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] root* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Synthesizer.</span><span class="sxs-lookup"><span data-stu-id="ad427-147">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Synth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad427-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad427-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad427-149">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad427-149">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



