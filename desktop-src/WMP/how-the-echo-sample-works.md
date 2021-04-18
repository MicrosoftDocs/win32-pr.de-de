---
title: Funktionsweise des Echo-Beispiels
description: Funktionsweise des Echo-Beispiels
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Windows Media Player-Plug-ins, Übersicht über ECHO Beispiele
- Plug-ins, Echo Sample Overview
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Overview
- DSP-Plug-ins, Übersicht über ECHO Beispiele
- Echo DSP-Plug-in-Beispiel, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341242"
---
# <a name="how-the-echo-sample-works"></a><span data-ttu-id="c5e49-108">Funktionsweise des Echo-Beispiels</span><span class="sxs-lookup"><span data-stu-id="c5e49-108">How the Echo Sample Works</span></span>

<span data-ttu-id="c5e49-109">Der Code erstellt den Echo Effekt durch Zuordnen eines Puffers, der ausreichend groß genug ist, um genau die Menge an Audiodaten zu erhalten, die in dem durch den Verzögerungs Zeitwert angegebenen Zeitrahmen gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="c5e49-109">The code creates the echo effect by allocating a buffer large enough to contain exactly the amount of audio data that can be rendered in the time frame specified by the delay time value.</span></span> <span data-ttu-id="c5e49-110">Die Größe des Puffers wird in Bytes mit der folgenden Formel berechnet:</span><span class="sxs-lookup"><span data-stu-id="c5e49-110">The size of the buffer is calculated, in bytes, by the following formula:</span></span>

<span data-ttu-id="c5e49-111">Puffergröße = Verzögerungszeit \* Stichprobenrate/1000 \* Block Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="c5e49-111">buffer size = delay time \* sample rate / 1000 \* block alignment</span></span>

<span data-ttu-id="c5e49-112">Die Verzögerungszeit beträgt Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="c5e49-112">The delay time is in milliseconds.</span></span> <span data-ttu-id="c5e49-113">Die Werte für die Stichprobenrate und die Block Ausrichtung werden in einer WaveFormatEx-Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="c5e49-113">The sample rate and block alignment values are given in a WAVEFORMATEX structure.</span></span> <span data-ttu-id="c5e49-114">Die Stichprobenrate beträgt Stichproben pro Sekunde. Division durch 1000 ergibt Stichproben pro Millisekunde.</span><span class="sxs-lookup"><span data-stu-id="c5e49-114">The sample rate is in samples per second; dividing by 1000 yields samples per millisecond.</span></span> <span data-ttu-id="c5e49-115">Die Block Ausrichtung entspricht dem Produkt der Anzahl von Kanälen (1 für Mono, 2 für Stereo) und der Anzahl von Bits pro Stichprobe (8 oder 16) dividiert durch 8 (Bits pro Byte).</span><span class="sxs-lookup"><span data-stu-id="c5e49-115">The block alignment is equal to the product of the number of channels (1 for mono, 2 for stereo) and the number of bits per sample (8 or 16) divided by 8 (bits per byte).</span></span>

<span data-ttu-id="c5e49-116">Zusätzlich zu der Zeiger Variablen, die auf den Anfang des Verzögerungs Puffers zeigt, erstellt der Code einen verschiebbaren Zeiger, der die Daten im Puffer in der Synchronisierung mit der Verarbeitungs Schleife in der **DoProcess Output** -Funktion durchläuft.</span><span class="sxs-lookup"><span data-stu-id="c5e49-116">In addition to the pointer variable that points to the head of the delay buffer, the code creates a movable pointer that steps through the data in the buffer in synchronization with the processing loop in the **DoProcessOutput** function.</span></span> <span data-ttu-id="c5e49-117">Wenn der verschiebbare Zeiger das Ende des Verzögerungs Puffers erreicht, wechselt er zurück zum Anfang des Puffers.</span><span class="sxs-lookup"><span data-stu-id="c5e49-117">When the movable pointer reaches the end of the delay buffer, it moves back to the head of the buffer.</span></span> <span data-ttu-id="c5e49-118">Ein auf diese Weise verwendeter Puffer wird als Zirkel Puffer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c5e49-118">A buffer used in this manner is called a circular buffer.</span></span>

<span data-ttu-id="c5e49-119">Sobald der Verzögerungs Puffer vorhanden ist und Windows Media Player einen Eingabepuffer zum Bereitstellen von Audiodaten und einen Ausgabepuffer zum Empfangen der verarbeiteten Audiodaten zugeordnet hat, wird die Echo Verarbeitung wie folgt fortgesetzt:</span><span class="sxs-lookup"><span data-stu-id="c5e49-119">Once the delay buffer exists, and Windows Media Player has allocated an input buffer to supply audio data and an output buffer to receive processed audio data, the echo processing proceeds like this:</span></span>

1.  <span data-ttu-id="c5e49-120">Geben Sie eine Schleife ein, die die Verarbeitung der einzelnen Audiobeispiele im Eingabepuffer zulässt.</span><span class="sxs-lookup"><span data-stu-id="c5e49-120">Enter a loop that allows processing of each audio sample in the input buffer.</span></span>
2.  <span data-ttu-id="c5e49-121">Rufen Sie ein Beispiel aus dem Eingabepuffer ab.</span><span class="sxs-lookup"><span data-stu-id="c5e49-121">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="c5e49-122">Verschieben Sie dann den Eingabepuffer Zeiger auf das nächste Beispiel, um die nächste Schleifen Iterations Vorbereitung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="c5e49-122">Then, move the input buffer pointer forward to the next sample to prepare for the next loop iteration.</span></span>
3.  <span data-ttu-id="c5e49-123">Rufen Sie ein Beispiel aus dem verzögerten Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="c5e49-123">Retrieve a sample from the delay buffer.</span></span>
4.  <span data-ttu-id="c5e49-124">Kopieren Sie das Beispiel aus dem Eingabepuffer an den gleichen Speicherort im Verzögerungs Puffer, von dem aus die letzte Verzögerungs Stichprobe abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c5e49-124">Copy the sample from the input buffer to the same location in the delay buffer from which the last delay sample was retrieved.</span></span>
5.  <span data-ttu-id="c5e49-125">Verschieben Sie den Verzögerungs Puffer Zeiger auf das nächste Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c5e49-125">Move the delay buffer pointer forward to the next sample.</span></span> <span data-ttu-id="c5e49-126">Wenn sich der Zeiger über das Ende des Puffers bewegt, verschieben Sie ihn an den Anfang des Puffers.</span><span class="sxs-lookup"><span data-stu-id="c5e49-126">If the pointer moves past the end of the buffer, move it to the head of the buffer.</span></span>
6.  <span data-ttu-id="c5e49-127">Kombinieren Sie das Beispiel aus dem Eingabepuffer mit dem Beispiel aus dem verzögerten Puffer.</span><span class="sxs-lookup"><span data-stu-id="c5e49-127">Combine the sample from the input buffer with the sample from the delay buffer.</span></span>
7.  <span data-ttu-id="c5e49-128">Kopieren Sie das Ergebnis in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="c5e49-128">Copy the result to the output buffer.</span></span> <span data-ttu-id="c5e49-129">Verschieben Sie dann den Ausgabepuffer Zeiger auf die nächste Einheit, um die nächste Schleifen Iterations Vorbereitung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="c5e49-129">Then, move the output buffer pointer forward to the next unit to prepare for the next loop iteration.</span></span>
8.  <span data-ttu-id="c5e49-130">Wiederholen Sie den Vorgang, bis alle Beispiele verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="c5e49-130">Repeat until all the samples are processed.</span></span>

<span data-ttu-id="c5e49-131">Wenn ein Eingabe Beispiel, das in Schritt 2 abgerufen wird, in den Verzögerungs Puffer in Schritt 4 kopiert wird, bleibt es so lange, bis der verschiebbare Zeiger durch die einzelnen Beispiele im Verzögerungs Puffer geht und schließlich an dieselbe Position zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="c5e49-131">When an input sample retrieved in step 2 is copied to the delay buffer in step 4, it remains there until the movable pointer steps through each sample in the delay buffer and finally returns to the same position.</span></span> <span data-ttu-id="c5e49-132">Da die Größe des Verzögerungs Puffers so konzipiert ist, dass Sie mit der Verzögerungszeit übereinstimmt, wird die verstrichene Zeit zwischen dem Beispiel, das in den Verzögerungs Puffer kopiert wird, und dem abgerufenen Beispiel gleich der angegebenen Verzögerung (zuzüglich der von der eigentlichen Verarbeitung eingeführten Latenzzeit) wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="c5e49-132">Because the size of the delay buffer is designed to correspond to the delay time, the elapsed time between the sample being copied to the delay buffer and the sample being retrieved once again equals the specified delay (plus any latency introduced by the actual processing).</span></span>

<span data-ttu-id="c5e49-133">Wenn ein Stream gestartet wird, werden keine Verzögerungs Daten generiert, bis die Verzögerungszeit verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="c5e49-133">When a stream starts, no delay data is generated until the delay time has elapsed.</span></span> <span data-ttu-id="c5e49-134">Daher ist es wichtig, dass der Verzögerungs Puffer anfänglich den Ruhe Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="c5e49-134">Therefore, it is important that the delay buffer initially contains silence.</span></span> <span data-ttu-id="c5e49-135">Wenn der Verzögerungs Puffer zufällige Daten enthält, hört der Benutzer das weiß Rauschen, bis das Plug-in genügend Verzögerungs Daten generiert, um den gesamten Verzögerungs Puffer zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c5e49-135">If the delay buffer contains random data, the user will hear white noise until the plug-in generates enough delay data to overwrite the entire delay buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5e49-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5e49-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5e49-137">**Übersicht über das Echo Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c5e49-137">**Echo Sample Overview**</span></span>](echo-sample-overview.md)
</dt> </dl>

 

 




