---
description: Der Satz aller Stimmen mit den darin enthaltenen Effekten und deren Verbindungen wird als audioverarbeitungsgraph bezeichnet.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2-audiodiagramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218556"
---
# <a name="xaudio2-audio-graph"></a><span data-ttu-id="6b2f0-103">XAudio2-audiodiagramm</span><span class="sxs-lookup"><span data-stu-id="6b2f0-103">XAudio2 Audio Graph</span></span>

<span data-ttu-id="6b2f0-104">Der Satz aller Stimmen mit den darin enthaltenen Effekten und deren Verbindungen wird als audioverarbeitungsgraph bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-104">The set of all voices, with their contained effects and their interconnections, is referred to as the audio processing graph.</span></span> <span data-ttu-id="6b2f0-105">Das Diagramm übernimmt eine Reihe von Audiodatenströmen vom Client als Eingabe, verarbeitet sie und übergibt das Endergebnis an ein Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-105">The graph takes a set of audio streams from the client as input, processes them, and delivers the final result to an audio device.</span></span> <span data-ttu-id="6b2f0-106">Die gesamte Audioverarbeitung erfolgt in einem separaten Thread mit einer Periodizität, die durch das Quantum des Diagramms definiert wird (derzeit 10 Millisekunden unter Microsoft Windows und 5 1/3 Millisekunden auf Xbox 360).</span><span class="sxs-lookup"><span data-stu-id="6b2f0-106">All audio processing takes place in a separate thread with a periodicity defined by the graph's quantum (currently 10 milliseconds on Microsoft Windows, and 5 1/3 milliseconds on Xbox 360).</span></span> <span data-ttu-id="6b2f0-107">Jede Quantum-Millisekunde wird der Thread reaktiviert und die Quantum-Millisekunden der Audiodaten über das gesamte Diagramm verteilt.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-107">Every quantum milliseconds, the thread wakes up and disperses quantum milliseconds of audio data through the entire graph.</span></span> <span data-ttu-id="6b2f0-108">Ein Beispiel für das Erstellen eines einfachen audiodiagramms finden Sie unter Gewusst wie: [Erstellen eines einfachen audioverarbeitungdiagramms](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="6b2f0-108">For an example of building a basic audio graph, see How to: [Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span>

<span data-ttu-id="6b2f0-109">Ein einfaches audiodiagramm:</span><span class="sxs-lookup"><span data-stu-id="6b2f0-109">A simple audio graph:</span></span>

![ein einfaches audiodiagramm](images/xaudio2-audio-graph.png)

<span data-ttu-id="6b2f0-111">Der Client kann den Status des Diagramms dynamisch steuern, während er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-111">The client can control the graph's state dynamically while it is running.</span></span> <span data-ttu-id="6b2f0-112">Steuerungs Aktionen können das Hinzufügen und Entfernen von Eingaben und Ausgaben, das Ändern der internen Effekte und der Verbindungen, das Festlegen von Parametern für die Effekte, das Aktivieren und Deaktivieren von Teilen des Diagramms usw. umfassen.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-112">Control actions might include adding and removing inputs and outputs, changing the internal effects and interconnections, setting parameters on the effects, enabling and disabling parts of the graph, and so on.</span></span> <span data-ttu-id="6b2f0-113">Ein Beispiel für das dynamische Ändern eines audiodiagramms finden [Sie unter Gewusst wie: Dynamisches Hinzufügen oder Entfernen von Stimmen aus einem audiodiagramm](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="6b2f0-113">For an example of dynamically changing an audio graph, see [How to: Dynamically Add or Remove Voices From an Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span></span>

## <a name="processing-the-graph"></a><span data-ttu-id="6b2f0-114">Verarbeiten des Diagramms</span><span class="sxs-lookup"><span data-stu-id="6b2f0-114">Processing the Graph</span></span>

<span data-ttu-id="6b2f0-115">Jeder Methodenaufruf, der sich auf ein Objekt im Diagramm auswirkt, wird als Auswirkung einer Diagramm Zustandsänderung betrachtet.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-115">Any method call that affects any object in the graph is considered to be effecting a graph state change.</span></span> <span data-ttu-id="6b2f0-116">Die Änderungen des Graph-Zustands umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6b2f0-116">Graph state changes include the following:</span></span>

-   <span data-ttu-id="6b2f0-117">Erstellen und zerstören von Stimmen</span><span class="sxs-lookup"><span data-stu-id="6b2f0-117">Creating and destroying voices</span></span>
-   <span data-ttu-id="6b2f0-118">Starten oder Beenden von Stimmen</span><span class="sxs-lookup"><span data-stu-id="6b2f0-118">Starting or stopping voices</span></span>
-   <span data-ttu-id="6b2f0-119">Ändern der Ziele einer Stimme</span><span class="sxs-lookup"><span data-stu-id="6b2f0-119">Changing the destinations of a voice</span></span>
-   <span data-ttu-id="6b2f0-120">Ändern von Effektketten</span><span class="sxs-lookup"><span data-stu-id="6b2f0-120">Modifying effect chains</span></span>
-   <span data-ttu-id="6b2f0-121">Aktivieren oder Deaktivieren von Effekten</span><span class="sxs-lookup"><span data-stu-id="6b2f0-121">Enabling or disabling effects</span></span>
-   <span data-ttu-id="6b2f0-122">Festlegen von Parametern für die Auswirkungen oder die integrierten SRCS, Filter, Volumes und Mixer</span><span class="sxs-lookup"><span data-stu-id="6b2f0-122">Setting parameters on the effects or on the built-in SRCs, filters, volumes, and mixers</span></span>

<span data-ttu-id="6b2f0-123">Jeder Satz von Diagramm Zustandsänderungen kann kombiniert und als atomarische Transaktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-123">Any set of graph state changes can be combined and performed as an atomic transaction.</span></span> <span data-ttu-id="6b2f0-124">Diese atomaren Vorgänge werden als Vorgangs Sätze bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-124">These atomic operations are known as operation sets.</span></span> <span data-ttu-id="6b2f0-125">Diese werden in der Übersicht über [XAudio2-Vorgangs Sätze](xaudio2-operation-sets.md) erläutert.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-125">They are discussed in the [XAudio2 Operation Sets](xaudio2-operation-sets.md) overview.</span></span>

## <a name="internal-data-representation"></a><span data-ttu-id="6b2f0-126">Interne Datendarstellung</span><span class="sxs-lookup"><span data-stu-id="6b2f0-126">Internal Data Representation</span></span>

<span data-ttu-id="6b2f0-127">Audiodaten innerhalb des XAudio2-Diagramms werden stets in 32-Bit-PCM-Gleit Komma Formularen gespeichert und verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-127">Audio data within the XAudio2 graph is always stored and processed in 32-bit floating-point PCM form.</span></span> <span data-ttu-id="6b2f0-128">Allerdings können die Anzahl der Kanäle und die Stichprobenrate innerhalb des Diagramms variieren.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-128">However, the channel count and sample rate can vary within the graph.</span></span> <span data-ttu-id="6b2f0-129">Das Format, in dem eine bestimmte Stimme das audioverfahren verarbeitet, wird durch den voicetype und die Parameter bestimmt, die zum Erstellen der Stimme verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-129">The format in which a given voice processes audio is determined by the voice type and parameters used to create the voice.</span></span>



| <span data-ttu-id="6b2f0-130">Sprachtyp</span><span class="sxs-lookup"><span data-stu-id="6b2f0-130">Voice Type</span></span>                                                                                                      | <span data-ttu-id="6b2f0-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b2f0-131">Parameters</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b2f0-132">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="6b2f0-132">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | <span data-ttu-id="6b2f0-133">Die Anzahl der Kanäle und die Samplingrate der Stimmen, an die die Quell Stimme Audiodaten sendet.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-133">The channel count and sample rate of the voices to which the source voice sends audio.</span></span>         |
| <span data-ttu-id="6b2f0-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) und [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span><span class="sxs-lookup"><span data-stu-id="6b2f0-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) and [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span></span> | <span data-ttu-id="6b2f0-135">Die *inputchannels* -und *inputsamplerate* -Argumente, die zum Erstellen der unter Mischung/der Mastering-Stimme verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-135">The *InputChannels* and *InputSampleRate* arguments used to create the submix/mastering voice.</span></span> |



 

## <a name="format-conversion"></a><span data-ttu-id="6b2f0-136">Format Konvertierung</span><span class="sxs-lookup"><span data-stu-id="6b2f0-136">Format Conversion</span></span>

<span data-ttu-id="6b2f0-137">XAudio2 verarbeitet jede Samplingrate oder Kanal Konvertierungen, die bei der Audioübertragung von einer Sprache zu einer anderen erforderlich sind, wobei die folgenden Einschränkungen gelten:</span><span class="sxs-lookup"><span data-stu-id="6b2f0-137">XAudio2 handles any sample rate or channel conversions that are required as audio travels from one voice to another, with the following limitations:</span></span>

-   <span data-ttu-id="6b2f0-138">Alle Ziel Stimmen für eine bestimmte Stimme müssen mit der gleichen Stichprobenrate ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-138">All destination voices for a particular voice must be running at the same sample rate</span></span>
-   <span data-ttu-id="6b2f0-139">Auswirkungen in einer Effekt Kette können die Kanalanzahl der Audiodaten ändern, aber nicht die Abtastrate.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-139">Effects in an effect chain can change the audio's channel count, but not its sample rate</span></span>
-   <span data-ttu-id="6b2f0-140">Die Anzahl der Ausgabekanäle einer Effekt Kette muss mit der Anzahl der von ihr gesendeten Stimmen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-140">An effect chain's output channel count must match that of the voices to which it sends</span></span>
-   <span data-ttu-id="6b2f0-141">Es kann keine dynamische Diagramm Änderung vorgenommen werden, die die oben genannten Regeln unterbricht.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-141">No dynamic graph change can be made which would break the rules above</span></span>

<span data-ttu-id="6b2f0-142">Auf der Eingabe Seite können Quell Stimmen Daten in jedem gültigen PCM-Format oder in einem der komprimierten Formate lesen, die von XAudio2 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-142">On the input side, source voices can read data in any valid PCM format, or in any of the compressed formats supported by XAudio2.</span></span> <span data-ttu-id="6b2f0-143">Wenn die Eingabedaten komprimiert werden, werden Sie vor der weiteren Verarbeitung in ein Gleit Komma-PCM decodiert.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-143">If the input data is compressed, it is decoded to floating-point PCM before any further processing is done.</span></span>

<span data-ttu-id="6b2f0-144">Auf der Ausgabe Seite können durch Mastering Stimmen nur PCM-Daten erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-144">On the output side, mastering voices can only produce PCM data.</span></span> <span data-ttu-id="6b2f0-145">Diese Daten erfüllen immer die gleichen Einschränkungen, die oben für die Eingabe von PCM-Daten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6b2f0-145">This data will always satisfy the same restrictions described above for input PCM data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b2f0-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b2f0-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b2f0-147">Audiodiagramme</span><span class="sxs-lookup"><span data-stu-id="6b2f0-147">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="6b2f0-148">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="6b2f0-148">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6b2f0-149">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="6b2f0-149">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="6b2f0-150">So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm</span><span class="sxs-lookup"><span data-stu-id="6b2f0-150">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[<span data-ttu-id="6b2f0-151">So wird's gemacht: Verwenden von Submixstimmen</span><span class="sxs-lookup"><span data-stu-id="6b2f0-151">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="6b2f0-152">So wird's gemacht: Erstellen einer Effektkette</span><span class="sxs-lookup"><span data-stu-id="6b2f0-152">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



