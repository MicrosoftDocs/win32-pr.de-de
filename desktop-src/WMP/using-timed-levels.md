---
title: Verwenden von zeitgesteuerten Ebenen
description: Verwenden von zeitgesteuerten Ebenen
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- Visualisierungen, zeitgesteuerte Ereignisse
- benutzerdefinierte Visualisierungen, zeitgesteuerte Ereignisse
- Visualisierungen, Häufigkeits Array
- benutzerdefinierte Visualisierungen, Häufigkeits Array
- Visualisierungen, Wellenform Array
- benutzerdefinierte Visualisierungen, Wellenform Array
- Visualisierungen, Zustands Variable
- benutzerdefinierte Visualisierungen, Zustands Variable
- Visualisierungen, timestamp-Variable
- benutzerdefinierte Visualisierungen, timestamp-Variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036987"
---
# <a name="using-timed-levels"></a><span data-ttu-id="8e504-113">Verwenden von zeitgesteuerten Ebenen</span><span class="sxs-lookup"><span data-stu-id="8e504-113">Using Timed Levels</span></span>

<span data-ttu-id="8e504-114">Die **timedlevel** -Struktur besteht aus 2 2-dimensionalen Arrays, einem Zustandswert und einem Zeitstempelwert.</span><span class="sxs-lookup"><span data-stu-id="8e504-114">The **TimedLevel** structure is composed of two two-dimensional arrays, a state value, and a time stamp value.</span></span>

## <a name="frequency-array"></a><span data-ttu-id="8e504-115">Frequency-Array</span><span class="sxs-lookup"><span data-stu-id="8e504-115">Frequency Array</span></span>

<span data-ttu-id="8e504-116">Das Frequency-Array ist ein zweidimensionales Array.</span><span class="sxs-lookup"><span data-stu-id="8e504-116">The frequency array is a two-dimensional array.</span></span> <span data-ttu-id="8e504-117">Die erste Dimension jedes Arrays entspricht dem Stereo Audiokanal (links oder rechts), und der zweite entspricht den Frequenz Ebenen (in Bytes) der Momentaufnahme, in der das Audiospektrum in 1024 Regionen aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="8e504-117">The first dimension of each array corresponds to the stereo audio channel (left or right), and the second corresponds to the frequency levels (in bytes) of the snapshot, where the audio spectrum is divided up into 1024 regions.</span></span>

<span data-ttu-id="8e504-118">Die vom Windows-Media Player bereitgestellten Häufigkeits Array Daten können wie folgt angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="8e504-118">You can get the frequency array data supplied from the Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



<span data-ttu-id="8e504-119">Der Wert von Snapshot ist für den linken Kanal und enthält den Wert des untersten Teils des Häufigkeits Spektrums.</span><span class="sxs-lookup"><span data-stu-id="8e504-119">The value of snapshot is for the left channel and contains the value of the lowest part of the frequency spectrum.</span></span> <span data-ttu-id="8e504-120">Wenn die Momentaufnahme beispielsweise einen großen Wert aufweist, gibt Sie an, dass der niedrigste 1024-Teil des Häufigkeits Spektrums sehr umfangreich ist.</span><span class="sxs-lookup"><span data-stu-id="8e504-120">For example, if snapshot has a large value, it indicates that the lowest 1024th part of the frequency spectrum is rich in frequency.</span></span> <span data-ttu-id="8e504-121">Der Wert 0 (null) gibt an, dass in diesem Teil des Spektrums für den linken Kanal keine niedrigen Häufigkeits Werte vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8e504-121">A value of zero indicates no low frequency values in that part of the spectrum for the left channel.</span></span> <span data-ttu-id="8e504-122">Wenn Sie über ein Monophonic-Signal verfügen, hat nur die erste Dimension gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="8e504-122">If you have a monophonic signal, only the first dimension has valid values.</span></span>

<span data-ttu-id="8e504-123">Wenn das Signal nicht Stereo ist, enthält das zweite Array eine Kopie des Mono-Signals.</span><span class="sxs-lookup"><span data-stu-id="8e504-123">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="8e504-124">Das heißt, \[ die Häufigkeit 0 \] \[ *n* \] und \[ die Häufigkeit 1 \] \[ *n* \] enthalten die gleichen Daten, wobei *n* der Index in einer bestimmten Zelle ist.</span><span class="sxs-lookup"><span data-stu-id="8e504-124">That is, frequency\[0\]\[*n*\] and frequency\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="waveform-array"></a><span data-ttu-id="8e504-125">Waveform-Array</span><span class="sxs-lookup"><span data-stu-id="8e504-125">Waveform Array</span></span>

<span data-ttu-id="8e504-126">Das Wellenform-Array ist auch ein zweidimensionales Array.</span><span class="sxs-lookup"><span data-stu-id="8e504-126">The waveform array is also a two-dimensional array.</span></span> <span data-ttu-id="8e504-127">Die erste Dimension des Arrays entspricht dem Kanal (links oder rechts), und der zweite entspricht den Leistungsebenen (in Bytes) der Momentaufnahme, in der die audiopotenz in 1024 aufeinander folgende Zeit Segmente aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="8e504-127">The first dimension of the array corresponds to the channel (left or right), and the second corresponds to the power levels (in bytes) of the snapshot, where the audio power is broken up into 1024 contiguous time segments.</span></span>

<span data-ttu-id="8e504-128">Sie können die Wellenform-Array Daten von Windows Media Player auf folgende Weise erhalten:</span><span class="sxs-lookup"><span data-stu-id="8e504-128">You can get the waveform array data from Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



<span data-ttu-id="8e504-129">Der Wert von Snapshot ist für den linken Kanal und enthält den ersten Wert der quantifizierten Momentaufnahme der Stromwerte.</span><span class="sxs-lookup"><span data-stu-id="8e504-129">The value of snapshot is for the left channel and contains the first value of the quantized snapshot of the power values.</span></span> <span data-ttu-id="8e504-130">Wenn eine Momentaufnahme erstellt wird, besteht aus 1024 winzigen inkrementellen Messungen der audiopotenz.</span><span class="sxs-lookup"><span data-stu-id="8e504-130">When a snapshot is taken, it consists of 1024 tiny incremental measurements of the audio power.</span></span> <span data-ttu-id="8e504-131">Der niedrigste Wert des Arrays wird durch das erste inkrementelle Maß an audiopotenz generiert.</span><span class="sxs-lookup"><span data-stu-id="8e504-131">The lowest value of the array is generated by the first incremental measurement of audio power.</span></span> <span data-ttu-id="8e504-132">Beachten Sie, dass die Werte der Potenz von-128 bis + 127 gemessen werden, die Werte im Array jedoch zwischen 0 und 255 liegen.</span><span class="sxs-lookup"><span data-stu-id="8e504-132">Note that the values of the power are measured from -128 to +127 but the values in the array range from 0 to 255.</span></span> <span data-ttu-id="8e504-133">Wenn Sie über eine Mono-Welle verfügen, hat nur die erste Dimension gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="8e504-133">If you have a monophonic wave, only the first dimension will have valid values.</span></span>

<span data-ttu-id="8e504-134">Wenn das Signal nicht Stereo ist, enthält das zweite Array eine Kopie des Mono-Signals.</span><span class="sxs-lookup"><span data-stu-id="8e504-134">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="8e504-135">Das heißt, Wellenform \[ 0 \] \[ *n* \] und Wellenform \[ 1 \] \[ *n* \] enthalten dieselben Daten, wobei *n* der Index in einer bestimmten Zelle ist.</span><span class="sxs-lookup"><span data-stu-id="8e504-135">That is, waveform\[0\]\[*n*\] and waveform\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="state"></a><span data-ttu-id="8e504-136">State</span><span class="sxs-lookup"><span data-stu-id="8e504-136">State</span></span>

<span data-ttu-id="8e504-137">Die Zustands Variable gibt den Audiowiedergabe Status von Windows-Media Player wieder.</span><span class="sxs-lookup"><span data-stu-id="8e504-137">The state variable reflects the audio playback state of Windows Media Player.</span></span> <span data-ttu-id="8e504-138">Die playerstate-Enumerationswerte lauten.</span><span class="sxs-lookup"><span data-stu-id="8e504-138">The PlayerState enumeration values are</span></span>


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



<span data-ttu-id="8e504-139">Sie können diese Variable verwenden, um je nach Audiowiedergabe Status verschiedene Aktionen durchführen.</span><span class="sxs-lookup"><span data-stu-id="8e504-139">You can use this variable to take different actions depending on the audio playback state.</span></span> <span data-ttu-id="8e504-140">Sie können z. b. eine Art von Visualisierung wiedergeben, wenn die Audiodatei abgespielt wird, und eine andere, wenn Sie angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="8e504-140">For example, you can play one kind of visualization when the audio is playing and another when it is stopped.</span></span>

## <a name="time-stamp"></a><span data-ttu-id="8e504-141">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="8e504-141">Time Stamp</span></span>

<span data-ttu-id="8e504-142">Die timestamp-Variable gibt die aktuelle Zeit an, zu der die Momentaufnahme erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8e504-142">The timeStamp variable reflects the current time when the snapshot is taken.</span></span> <span data-ttu-id="8e504-143">Dies kann verwendet werden, um zu messen, wie häufig die Momentaufnahmen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8e504-143">This can be used to measure how frequently the snapshots are taken.</span></span>

<span data-ttu-id="8e504-144">Sie können diese Variable verwenden, um Ihre Animationen zu Zeit zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e504-144">You can use this variable to time your animations.</span></span> <span data-ttu-id="8e504-145">Wenn die Momentaufnahmen zu häufig vorkommen, können Sie das Abbild ordnungsgemäß herabstufen, sodass es auf die von Ihnen gewählte Weise angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8e504-145">If the snapshots are too frequent, you can gracefully degrade your image to display in the manner you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e504-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e504-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e504-147">**Implementieren von Rendering**</span><span class="sxs-lookup"><span data-stu-id="8e504-147">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




