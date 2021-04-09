---
description: Fehler können in XAudio2 auftreten. in diesem Thema wird erläutert, wie Sie gemeldet werden, und es gibt einige Ansätze zur Behebung dieser Fehler.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Debuggen von Audiostörungen in XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866495"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a><span data-ttu-id="8d1ec-103">Debuggen von Audiostörungen in XAudio2</span><span class="sxs-lookup"><span data-stu-id="8d1ec-103">Debugging Audio Glitches in XAudio2</span></span>

<span data-ttu-id="8d1ec-104">Fehler können in XAudio2 auftreten. in diesem Thema wird erläutert, wie Sie gemeldet werden, und es gibt einige Ansätze zur Behebung dieser Fehler.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-104">Glitches can occur in XAudio2, this topic covers how they are reported and some approaches to fixing them.</span></span>

<span data-ttu-id="8d1ec-105">In dieser Übersicht werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="8d1ec-105">This overview covers the following topics:</span></span>

-   [<span data-ttu-id="8d1ec-106">Ursachen für audioausgabeprobleme oder-Ausfälle</span><span class="sxs-lookup"><span data-stu-id="8d1ec-106">Causes of audio output problems or glitches</span></span>](#causes-of-audio-output-problems-or-glitches)
-   [<span data-ttu-id="8d1ec-107">So meldet XAudio2 Probleme</span><span class="sxs-lookup"><span data-stu-id="8d1ec-107">How XAudio2 reports problems</span></span>](#how-xaudio2-reports-problems)
-   [<span data-ttu-id="8d1ec-108">Ansätze zum Beheben von Problemen</span><span class="sxs-lookup"><span data-stu-id="8d1ec-108">Approaches to fixing problems</span></span>](#approaches-to-fixing-problems)
-   [<span data-ttu-id="8d1ec-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d1ec-109">Related topics</span></span>](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a><span data-ttu-id="8d1ec-110">Ursachen für audioausgabeprobleme oder-Ausfälle</span><span class="sxs-lookup"><span data-stu-id="8d1ec-110">Causes of audio output problems or glitches</span></span>

<span data-ttu-id="8d1ec-111">In der XAudio2-Ausgabe können aus verschiedenen Gründen Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-111">Glitches can occur in XAudio2 output for several reasons.</span></span>

-   <span data-ttu-id="8d1ec-112">Eine XAudio2-Quellsprache wird verhungert.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-112">An XAudio2 source voice is starved.</span></span> <span data-ttu-id="8d1ec-113">Der Client sendet nicht schnell genug neue Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-113">The client is not submitting fresh audio to it fast enough.</span></span> <span data-ttu-id="8d1ec-114">Sie erhalten eine Ruhe, weil Sie keine Daten für die Wiedergabe hat.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-114">You get silence because it has no data to play.</span></span>
-   <span data-ttu-id="8d1ec-115">XAudio2 als Ganzes ist überlastet.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-115">XAudio2 as a whole is overburdened.</span></span> <span data-ttu-id="8d1ec-116">Es dauert länger als *x* MS, bis *x* MS Audiodaten erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-116">It takes longer than *X* ms to produce *X* ms of audio.</span></span> <span data-ttu-id="8d1ec-117">Sie erhalten Dropouts, weil XAudio2 keine Daten so schnell wie möglich mit dem Audiogerät erzeugt.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-117">You get dropouts because XAudio2 can't produce data as fast as the audio device needs it.</span></span> <span data-ttu-id="8d1ec-118">Möglicherweise führen Sie zu viele Stimmen oder Effekte gleichzeitig aus, arbeiten in XAudio2-Rückrufen oder XAudio2-API-aufrufen zu häufig.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-118">You might be running too many voices or effects at a time, doing too much work in XAudio2 callbacks, or making XAudio2 API calls too frequently.</span></span>
-   <span data-ttu-id="8d1ec-119">Der Audioverarbeitungs Thread wird nicht ausgeführt, da die Implementierung eines XAudio2-Rückrufs durch den Client Dinge bewirkt, die den Thread blockieren können.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-119">The audio processing thread is stalling because the client's implementation of some XAudio2 callback is doing things that can block the thread.</span></span> <span data-ttu-id="8d1ec-120">Beispielsweise kann der Zugriff auf den Datenträger erfolgen, mit anderen Threads synchronisiert oder andere Funktionen aufgerufen werden, die blockieren können.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-120">For example, it might be accessing the disk, synchronizing with other threads, or calling other functions that may block.</span></span> <span data-ttu-id="8d1ec-121">Verwenden Sie einen Hintergrund Thread mit niedrigerer Priorität, den der Rückruf signalisieren kann, um solche Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-121">Use a lower-priority background thread that the callback can signal to perform such tasks.</span></span>
-   <span data-ttu-id="8d1ec-122">Das System wird als Ganzes überladen.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-122">The system as a whole is overloaded.</span></span> <span data-ttu-id="8d1ec-123">Andere Threads, die mit der gleichen oder einer höheren Priorität als XAudio2 ausgeführt werden, funktionieren zu viel.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-123">Other threads running at the same or higher priority than XAudio2 are doing too much work.</span></span> <span data-ttu-id="8d1ec-124">Sie konkurrieren mit dem audiothread für die CPU-Zeit.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-124">They are competing with the audio thread for CPU time.</span></span>

## <a name="how-xaudio2-reports-problems"></a><span data-ttu-id="8d1ec-125">So meldet XAudio2 Probleme</span><span class="sxs-lookup"><span data-stu-id="8d1ec-125">How XAudio2 reports problems</span></span>

<span data-ttu-id="8d1ec-126">XAudio2 kann im Debugbuild auf verschiedene Weise auf eine Weise kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-126">XAudio2 can communicate glitches in the debug build in several ways.</span></span>

-   <span data-ttu-id="8d1ec-127">Wenn eine Stimme verhungert wird, wird in XAudio2 eine Meldung in dieser Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-127">If a voice is being starved, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   <span data-ttu-id="8d1ec-128">Wenn der audiothread zu lange ausgeführt wird, wird in XAudio2 eine Meldung in dieser Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-128">If the audio thread runs for too long, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    <span data-ttu-id="8d1ec-129">In der Regel wird diese Meldung mit der nächsten Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-129">Typically, this message occurs with the next message.</span></span>

-   <span data-ttu-id="8d1ec-130">Wenn der Audiotreiber nicht rechtzeitig mit neuen Audiodaten versorgt werden kann, wird in XAudio2 eine Meldung in dieser Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-130">If the audio driver can't be fed new audio data on time, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   <span data-ttu-id="8d1ec-131">Durch Aufrufen von [**IXAudio2:: getperformancedata**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) werden XAudio2-Leistungsdaten bereitstellt, einschließlich der Gesamtzahl der seit dem Start der XAudio2-Engine erstellten Fehler.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-131">Calling [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) provides XAudio2 performance data, including the total number of glitches since the XAudio2 engine started.</span></span>

## <a name="approaches-to-fixing-problems"></a><span data-ttu-id="8d1ec-132">Ansätze zum Beheben von Problemen</span><span class="sxs-lookup"><span data-stu-id="8d1ec-132">Approaches to fixing problems</span></span>

<span data-ttu-id="8d1ec-133">Es gibt folgende Möglichkeiten, um audioglime zu reduzieren:</span><span class="sxs-lookup"><span data-stu-id="8d1ec-133">Possible ways to reduce audio glitches include the following.</span></span>

-   <span data-ttu-id="8d1ec-134">Bei der sprach Hungersnot: erhöhen Sie die Menge an Audiodaten, die in der Warteschlange einer Stimme in der Warteschlange stehen.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-134">In the voice starvation case: Increase the amount of audio data that is queued ahead on a voice.</span></span> <span data-ttu-id="8d1ec-135">Sie können [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) verwenden, um die Anzahl der Puffer zu ermitteln, die in der Warteschlange stehen.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-135">You can use [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) to discover the number of buffers queued at any moment.</span></span> <span data-ttu-id="8d1ec-136">Wenn weiterhin Probleme mit der sprach Hungersnot angezeigt werden, aber keine Fehler auftreten, stellen Sie sicher, dass Sie [**XAUDIO2 \_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)festlegen.**Flags** zum XAUDIO2- \_ Ende \_ des \_ Streams im letzten Puffer eines Sounds.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-136">If you still see voice starvation errors, but can't hear any glitch, make sure you are setting [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flags** to XAUDIO2\_END\_OF\_STREAM on the final buffer of a sound.</span></span> <span data-ttu-id="8d1ec-137">Dies weist darauf hin, dass XAudio2 nicht zu erwarten ist, dass mehr Puffer unbedingt verfügbar sind, sobald dieser Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-137">This tells XAudio2 not to expect any more buffers necessarily to be available as soon as this one completes.</span></span>

    <span data-ttu-id="8d1ec-138">In den anderen Fällen:</span><span class="sxs-lookup"><span data-stu-id="8d1ec-138">In the other cases:</span></span>

    -   <span data-ttu-id="8d1ec-139">Reduzieren Sie die Anzahl aktiver Stimmen und Effekte im Diagramm, insbesondere teure Effekte wie "Hall".</span><span class="sxs-lookup"><span data-stu-id="8d1ec-139">Reduce the number of active voices and effects in the graph, especially expensive effects like reverb.</span></span>
    -   <span data-ttu-id="8d1ec-140">Deaktivieren Sie stimmen und Effekte, die Sie nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-140">Disable voices and effects you're not using.</span></span>
    -   <span data-ttu-id="8d1ec-141">Verwenden Sie nach \_ Möglichkeit die Flags "XAUDIO2 Voice \_ nosrc" und "XAUDIO2 \_ Voice \_ nopitch" in [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).</span><span class="sxs-lookup"><span data-stu-id="8d1ec-141">Use the XAUDIO2\_VOICE\_NOSRC and XAUDIO2\_VOICE\_NOPITCH flags in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), whenever possible.</span></span> <span data-ttu-id="8d1ec-142">Die Stichproben Raten Konvertierung ist aufwendig.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-142">Sample rate conversion is costly.</span></span>
    -   <span data-ttu-id="8d1ec-143">Reduzieren Sie die Stichprobenrate einzelner Stimmen.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-143">Reduce the sample rate of individual voices.</span></span> <span data-ttu-id="8d1ec-144">Beispielsweise kann eine unter Mischungs Stimme, die einen Hall-Effekt als Host hat, eine niedrigere Samplingrate aufweisen als die an Sie gesendete Quell Stimme.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-144">For example, a submix voice hosting a reverb effect can have a lower sample rate than the source voice sending to it.</span></span> <span data-ttu-id="8d1ec-145">Sounds, wie z. b. Explosionen und schießshots, die keine hohe Treue erfordern, können auch zu niedrigeren Stichproben Raten aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-145">Sounds such as explosions and gunshots that don't need high fidelity can also be recorded at lower sample rates.</span></span>
    -   <span data-ttu-id="8d1ec-146">Stellen Sie sicher, dass Rückruf Implementierungen so wenig wie möglich funktionieren und nie blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-146">Ensure that callback implementations do as little work as possible and never block.</span></span>
    -   <span data-ttu-id="8d1ec-147">Nehmen Sie weniger Aufrufe an XAudio2 vor.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-147">Make fewer calls to XAudio2.</span></span> <span data-ttu-id="8d1ec-148">Audioparameter müssen in der Regel nicht für jeden Videorahmen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-148">Audio parameters usually don't need to be updated for every video frame.</span></span> <span data-ttu-id="8d1ec-149">Alle 30 ms sind ausreichend.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-149">Every 30 ms or so is sufficient.</span></span> <span data-ttu-id="8d1ec-150">Sie sollten redundante Aufrufe vermeiden, z. b. das Volume mehrmals in schneller Folge festlegen.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-150">You should eliminate redundant calls, such as setting volume several times in quick succession.</span></span>
    -   <span data-ttu-id="8d1ec-151">Reduzieren Sie die CPU-Gesamtauslastung des Spiels.</span><span class="sxs-lookup"><span data-stu-id="8d1ec-151">Reduce the game's overall CPU usage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d1ec-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d1ec-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d1ec-153">Debugging-Einrichtungen</span><span class="sxs-lookup"><span data-stu-id="8d1ec-153">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="8d1ec-154">XAudio2-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="8d1ec-154">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
