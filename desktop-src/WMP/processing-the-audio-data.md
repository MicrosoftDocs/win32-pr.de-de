---
title: Verarbeiten der Audiodaten
description: Verarbeiten der Audiodaten
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337596"
---
# <a name="processing-the-audio-data"></a><span data-ttu-id="56b90-109">Verarbeiten der Audiodaten</span><span class="sxs-lookup"><span data-stu-id="56b90-109">Processing the Audio Data</span></span>

<span data-ttu-id="56b90-110">Die Standard Implementierung von " **DoProcess Output** " beginnt mit dem Abrufen eines Zeigers auf eine gültige **WaveFormatEx** -Struktur, wie dies in "" von "" in "" von "" **zugeordnet** wurde.</span><span class="sxs-lookup"><span data-stu-id="56b90-110">The default implementation of **DoProcessOutput** begins by retrieving a pointer to a valid **WAVEFORMATEX** structure, exactly like was done in **AllocateStreamingResources**.</span></span> <span data-ttu-id="56b90-111">Anschließend werden die Informationen in dieser Struktur verwendet, um die Anzahl der Stichproben im Eingabepuffer zu berechnen, die auf die Verarbeitung warten.</span><span class="sxs-lookup"><span data-stu-id="56b90-111">It then uses the information in that structure to calculate the number of samples in the input buffer waiting to be processed.</span></span> <span data-ttu-id="56b90-112">Der folgende Code ist aus der Standard Implementierung:</span><span class="sxs-lookup"><span data-stu-id="56b90-112">The following code is from the default implementation:</span></span>


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



<span data-ttu-id="56b90-113">Anschließend überprüft der Code den **wbitspersample** -Member, um die Bittiefe der Audiodatei zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="56b90-113">Then, the code inspects the **wBitsPerSample** member to determine the bit depth of the audio.</span></span> <span data-ttu-id="56b90-114">Dieser Wert wird in einer Switch-Anweisung verwendet, um eine separate Verarbeitung für 8-Bit-und 16-Bit-Audiodaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="56b90-114">This value is used in a switch statement to provide separate processing for 8-bit and 16-bit audio.</span></span>

## <a name="differences-between-8-bit-and-16-bit-audio"></a><span data-ttu-id="56b90-115">Unterschiede zwischen 8-Bit-und 16-Bit-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="56b90-115">Differences Between 8-bit and 16-bit Audio</span></span>

<span data-ttu-id="56b90-116">Es gibt wichtige Unterschiede zwischen 8-Bit-und 16-Bit-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="56b90-116">There are important differences between 8-bit and 16-bit audio.</span></span> <span data-ttu-id="56b90-117">Daher unterscheiden sich die Verarbeitungs Routinen zum Erstellen des Echo Effekts.</span><span class="sxs-lookup"><span data-stu-id="56b90-117">Therefore, the processing routines to create the echo effect are different.</span></span> <span data-ttu-id="56b90-118">Die beiden Formate unterscheiden sich wie folgt:</span><span class="sxs-lookup"><span data-stu-id="56b90-118">The two formats differ in the following ways:</span></span>

-   <span data-ttu-id="56b90-119">Jedes Format hat eine andere Stichprobengröße: 8-Bit-Samplings belegen jeweils ein Byte Arbeitsspeicher, während 16-Bit-Stichproben jeweils zwei Bytes belegen.</span><span class="sxs-lookup"><span data-stu-id="56b90-119">Each format has a different sample size: 8-bit samples each occupy one byte of memory, while 16-bit samples each occupy two bytes.</span></span>
-   <span data-ttu-id="56b90-120">Jedes Format repräsentiert die Audioamplitude anders.</span><span class="sxs-lookup"><span data-stu-id="56b90-120">Each format represents the audio amplitude differently.</span></span> <span data-ttu-id="56b90-121">8-Bit-Audiodaten werden durch eine Ganzzahl ohne Vorzeichen mit einem Bereich von 0 bis 255 dargestellt. der Wert 128 stellt den Ruhe Wert dar.</span><span class="sxs-lookup"><span data-stu-id="56b90-121">8-bit audio is represented by an unsigned integer with a range from 0 to 255; a value of 128 represents silence.</span></span> <span data-ttu-id="56b90-122">die 16-Bit-Audiodaten werden durch eine ganze Zahl mit Vorzeichen und einen Bereich von-32768 bis 32767 dargestellt. der Wert 0 (null) stellt den Ruhe Wert dar.</span><span class="sxs-lookup"><span data-stu-id="56b90-122">16-bit audio is represented by a signed integer with a range from -32768 to 32767; a value of zero represents silence.</span></span>

<span data-ttu-id="56b90-123">Während der Vorgang zum Erstellen des Echo Effekts für jedes Format grundsätzlich identisch ist, müssen sich die Details leicht unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="56b90-123">While the process of creating the echo effect is fundamentally identical for each format, the details must differ slightly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56b90-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56b90-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b90-125">**Implementieren von Cecho::D oprocess Output**</span><span class="sxs-lookup"><span data-stu-id="56b90-125">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




