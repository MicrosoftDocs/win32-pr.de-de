---
title: Variablen zum Durchführen der Verarbeitung
description: Variablen zum Durchführen der Verarbeitung
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, Verarbeiten von Variablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711106"
---
# <a name="variables-to-perform-processing"></a><span data-ttu-id="40ce1-109">Variablen zum Durchführen der Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="40ce1-109">Variables to Perform Processing</span></span>

<span data-ttu-id="40ce1-110">Die Element Variablen zur Behandlung des Verzögerungs Puffers mit **Byte** Mengen. Dabei handelt es sich um **Byte** Zeiger und eine ganze Zahl, die die Anzahl von Bytes speichert.</span><span class="sxs-lookup"><span data-stu-id="40ce1-110">The member variables for handling the delay buffer deal with **BYTE** quantities; they are **BYTE** pointers and an integer that stores a count of bytes.</span></span> <span data-ttu-id="40ce1-111">Dies eignet sich ideal für die Verarbeitung von 8-Bit-Audiodaten, da eine 8-Bit-Stichprobe problemlos in ein Byte Arbeitsspeicher passt.</span><span class="sxs-lookup"><span data-stu-id="40ce1-111">This is ideal for processing 8-bit audio, since an 8-bit sample fits nicely into one byte of memory.</span></span> <span data-ttu-id="40ce1-112">Bei der Verarbeitung von 16-Bit-Audiodaten ist es jedoch bequemer, diese in **kurze** Zeiger zu konvertieren, sodass die Verarbeitung zwei Bytes gleichzeitig durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="40ce1-112">When processing 16-bit audio, though, it is more convenient to convert these to **short** pointers, so the processing can occur two bytes at a time.</span></span>

<span data-ttu-id="40ce1-113">Im folgenden Beispielcode werden die neuen 16-Bit-Zeiger zugeordnet und eine Zeiger Variable hinzugefügt, in der die Adresse des Endes des Verzögerungs Puffers gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="40ce1-113">The following example code allocates the new 16-bit pointers, and adds a pointer variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="40ce1-114">Fügen Sie Sie direkt vor dem Einstiegspunkt der Schleife in den Abschnitt "Case 16" ein:</span><span class="sxs-lookup"><span data-stu-id="40ce1-114">Insert it in the "case 16" section just before the loop entry point:</span></span>


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



<span data-ttu-id="40ce1-115">Der Code für die 8-Bit-Verarbeitung weist auch eine Variable zu, in der die Adresse des Endes des Verzögerungs Puffers gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="40ce1-115">The code for 8-bit processing also allocates a variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="40ce1-116">Durch das Speichern dieses Werts können Sie leicht testen, ob der Puffer Zeiger für verschiebbare Verzögerung das Ende des Verzögerungs Puffers erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="40ce1-116">Storing this value makes it easy to test whether the movable delay buffer pointer has reached the end of the delay buffer.</span></span> <span data-ttu-id="40ce1-117">Der folgende Beispielcode berechnet den-Wert:</span><span class="sxs-lookup"><span data-stu-id="40ce1-117">The following example code calculates the value:</span></span>


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a><span data-ttu-id="40ce1-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40ce1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ce1-119">**Implementieren von Cecho::D oprocess Output**</span><span class="sxs-lookup"><span data-stu-id="40ce1-119">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




