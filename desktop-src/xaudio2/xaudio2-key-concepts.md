---
description: In dieser Übersicht werden einige wichtige Konzepte für die Verwendung von XAudio2 vorgestellt.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: XAudio2 Schlüsselkonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351061"
---
# <a name="xaudio2-key-concepts"></a><span data-ttu-id="cb0c5-103">XAudio2 Schlüsselkonzepte</span><span class="sxs-lookup"><span data-stu-id="cb0c5-103">XAudio2 Key Concepts</span></span>

<span data-ttu-id="cb0c5-104">In dieser Übersicht werden einige wichtige Konzepte für die Verwendung von XAudio2 vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-104">This overview introduces some key concepts for using XAudio2.</span></span>

-   [<span data-ttu-id="cb0c5-105">XAudio2-Engine</span><span class="sxs-lookup"><span data-stu-id="cb0c5-105">XAudio2 Engine</span></span>](#xaudio2-engine)
-   [<span data-ttu-id="cb0c5-106">Stimmen</span><span class="sxs-lookup"><span data-stu-id="cb0c5-106">Voices</span></span>](#voices)
-   [<span data-ttu-id="cb0c5-107">Audiodiagramm</span><span class="sxs-lookup"><span data-stu-id="cb0c5-107">Audio Graph</span></span>](#audio-graph)
-   [<span data-ttu-id="cb0c5-108">Rückrufe</span><span class="sxs-lookup"><span data-stu-id="cb0c5-108">Callbacks</span></span>](#callbacks)
-   [<span data-ttu-id="cb0c5-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cb0c5-109">Related Topics</span></span>](#related-topics)

## <a name="xaudio2-engine"></a><span data-ttu-id="cb0c5-110">XAudio2-Engine</span><span class="sxs-lookup"><span data-stu-id="cb0c5-110">XAudio2 Engine</span></span>

<span data-ttu-id="cb0c5-111">Die [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)-Schnittstelle bildet den Kern des XAudio2-Moduls.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-111">The [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface is the core of the XAudio2 engine.</span></span> <span data-ttu-id="cb0c5-112">Das Erstellen einer Instanz der **IXAudio2** -Schnittstelle ermöglicht es dem Client, die verfügbaren Audiogeräte aufzuzählen, globale API-Eigenschaften zu konfigurieren, stimmen zu erstellen und die Leistung zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-112">Creating an instance of the **IXAudio2** interface allows the client to enumerate the available audio devices, to configure global API properties, to create voices, and to monitor performance.</span></span> <span data-ttu-id="cb0c5-113">Die [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) Helper-Funktion führt Instanziierung und Initialisierungs Aufgaben für XAudio2 aus.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-113">The [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper function performs instantiation and initialization tasks for XAudio2.</span></span>

<span data-ttu-id="cb0c5-114">Sie können Instanzen von XAudio2 mehrmals innerhalb eines einzelnen Prozesses erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-114">You can create instances of XAudio2 multiple times within a single process.</span></span> <span data-ttu-id="cb0c5-115">Jedes XAudio2-Objekt wird unabhängig voneinander betrieben und verfügt über einen eigenen audioverarbeitungsthread.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-115">Each XAudio2 object operates independently, and has its own audio processing thread.</span></span> <span data-ttu-id="cb0c5-116">Nur die Debugeinstellungen werden freigegeben.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-116">Only the debug settings are shared.</span></span> <span data-ttu-id="cb0c5-117">Dies ist unter Windows wichtig, wenn mehrere verschiedene Komponenten in einem einzelnen Prozess geladen werden können.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-117">This is important on Windows where several different components may be loaded in a single process.</span></span> <span data-ttu-id="cb0c5-118">Internet Explorer kann z. b. mehrere XAudio2-Komponenten gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-118">For example, Internet Explorer might use multiple XAudio2 components simultaneously.</span></span> <span data-ttu-id="cb0c5-119">Obwohl es möglich ist, mehrere XAudio2-Engine-Objekte innerhalb einer einzelnen Client Anwendung zu erstellen, sollten Sie keine Informationen zwischen den jeweiligen Diagrammen übergeben.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-119">Although it is possible to create multiple XAudio2 engine objects within a single client application, you should not pass information between their respective graphs.</span></span>

<span data-ttu-id="cb0c5-120">Ein Beispiel für das Initialisieren der XAudio2-Engine finden [Sie unter Gewusst wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="cb0c5-120">For an example of initializing the XAudio2 engine, see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>

## <a name="voices"></a><span data-ttu-id="cb0c5-121">Stimmen</span><span class="sxs-lookup"><span data-stu-id="cb0c5-121">Voices</span></span>

<span data-ttu-id="cb0c5-122">Stimmen sind die Objekte, die XAudio2 zur Verarbeitung, Bearbeitung und Wiedergabe von Audiodaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-122">Voices are the objects XAudio2 use to process, to manipulate, and to play audio data.</span></span> <span data-ttu-id="cb0c5-123">In XAudio2 gibt es drei Arten von Stimmen.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-123">There are three types of voices in XAudio2.</span></span>

-   [<span data-ttu-id="cb0c5-124">**Quellen Stimmen**</span><span class="sxs-lookup"><span data-stu-id="cb0c5-124">**Source Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    <span data-ttu-id="cb0c5-125">Quell Stimmen stellen einen Stream von Audiodaten dar.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-125">Source voices represent a stream of audio data.</span></span> <span data-ttu-id="cb0c5-126">Quell Stimmen senden Ihre Daten an andere Arten von Stimmen.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-126">Source voices send their data to other types of voices.</span></span>

-   [<span data-ttu-id="cb0c5-127">**Teilmengen von Stimmen**</span><span class="sxs-lookup"><span data-stu-id="cb0c5-127">**Submix Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    <span data-ttu-id="cb0c5-128">Teilmischungs Stimmen führen eine gewisse Bearbeitung der Audiodaten aus, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-128">Submix voices perform some manipulation of audio data they receive.</span></span> <span data-ttu-id="cb0c5-129">Ein Beispiel für die Bearbeitung von Audiodaten könnte eine Stichproben Raten Konvertierung sein.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-129">One example of audio data manipulation might be sample rate conversion.</span></span> <span data-ttu-id="cb0c5-130">Nachdem eine unter Mischungs Sprache Daten verarbeitet hat, übergibt Sie diese Daten an eine andere Teil Mischungs Stimme oder an eine Master Stimme.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-130">After a submix voice processes data, it passes that data to another submix voice or to a master voice.</span></span>

-   [<span data-ttu-id="cb0c5-131">**Meistern von Stimmen**</span><span class="sxs-lookup"><span data-stu-id="cb0c5-131">**Mastering Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    <span data-ttu-id="cb0c5-132">Durch das beherrschen von Stimmen erhalten Sie Daten aus Quell Stimmen und Teil Mischungs Stimmen und sendet diese Daten an die Audiohardware.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-132">Mastering voices receive data from source voices and submix voices, and sends that data to the audio hardware.</span></span>

<span data-ttu-id="cb0c5-133">Unter [XAudio2 Voices](voices.md) finden Sie eine Übersicht über XAudio2 Stimmen.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-133">See [XAudio2 Voices](voices.md) for an overview of XAudio2 voices.</span></span>

## <a name="audio-graph"></a><span data-ttu-id="cb0c5-134">Audiodiagramm</span><span class="sxs-lookup"><span data-stu-id="cb0c5-134">Audio Graph</span></span>

<span data-ttu-id="cb0c5-135">Ein audiodiagramm ist eine Sammlung von XAudio2 Stimmen.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-135">An audio graph is a collection of XAudio2 voices.</span></span> <span data-ttu-id="cb0c5-136">Audiodaten werden an einer Seite eines audiodiagramms in den Quell Stimmen gestartet. optional wird eine oder mehrere Teil Mischungs Stimmen durchlaufen, und eine Stimme an.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-136">Audio starts at one side of an audio graph in source voices, optionally passes through one or more submix voices, and ends at a mastering voice.</span></span> <span data-ttu-id="cb0c5-137">Ein audiodiagramm enthält eine Quell Stimme für jeden aktuell wiedergegebenen Sound, 0 (null) oder mehr Teil Mischungs Stimmen und eine Stimme.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-137">An audio graph will contain a source voice for each sound currently playing, zero or more submix voices, and one mastering voice.</span></span> <span data-ttu-id="cb0c5-138">Das einfachste audiodiagramm und die Mindestanforderungen für die Durchführung eines Rauschens in XAudio2 ist eine einzelne Quelle, die direkt auf eine Mastering-Stimme aussteht.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-138">The simplest audio graph, and the minimum needed to make a noise in XAudio2, is a single source voice outputting directly to a mastering voice.</span></span> <span data-ttu-id="cb0c5-139">Ein Beispiel für die minimalen Schritte, die zur Wiedergabe eines Sounds mit XAudio2 erforderlich sind, finden Sie unter Gewusst [wie: Wiedergeben eines Sounds mit XAudio2](how-to--play-a-sound-with-xaudio2.md) .</span><span class="sxs-lookup"><span data-stu-id="cb0c5-139">See [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md) for an example of the minimum steps need to play a sound with XAudio2.</span></span>

<span data-ttu-id="cb0c5-140">Eine Übersicht über XAudio2-audiodiagramme finden Sie unter [XAudio2-audiodiagramm](audio-graphs.md) .</span><span class="sxs-lookup"><span data-stu-id="cb0c5-140">See [XAudio2 Audio Graph](audio-graphs.md) for an overview of XAudio2 audio graphs.</span></span>

## <a name="callbacks"></a><span data-ttu-id="cb0c5-141">Rückrufe</span><span class="sxs-lookup"><span data-stu-id="cb0c5-141">Callbacks</span></span>

<span data-ttu-id="cb0c5-142">Rückrufe sind der Mechanismus, den XAudio2 verwendet, um Client Code zu signalisieren, dass ein Ereignis in einer Stimme oder im Engine-Objekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-142">Callbacks are the mechanism XAudio2 uses to signal client code that some event has occurred in a voice or in the engine object.</span></span> <span data-ttu-id="cb0c5-143">Da die Audiowiedergabe in der XAudio2-Engine asynchron ist, stellen Rückrufe die einzige Möglichkeit dar, zu bestimmen, wann die Wiedergabe eines Sounds abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-143">Because audio playback is asynchronous in the XAudio2 engine, callbacks provide the only way to determine when a sound is finished playing.</span></span>

<span data-ttu-id="cb0c5-144">Eine Übersicht über XAudio2-Rückrufe finden Sie unter [XAudio2](callbacks.md) -Rückrufe.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-144">See [XAudio2 Callbacks](callbacks.md) for an overview of XAudio2 callbacks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb0c5-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb0c5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb0c5-146">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="cb0c5-146">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="cb0c5-147">XAudio2-Versionen</span><span class="sxs-lookup"><span data-stu-id="cb0c5-147">XAudio2 Versions</span></span>](xaudio2-versions.md)
</dt> <dt>

[<span data-ttu-id="cb0c5-148">So wird's gemacht: Initialisieren von XAudio2</span><span class="sxs-lookup"><span data-stu-id="cb0c5-148">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="cb0c5-149">Gewusst wie: Wiedergabe eines Sounds mit XAudio2</span><span class="sxs-lookup"><span data-stu-id="cb0c5-149">How to: Play a sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



