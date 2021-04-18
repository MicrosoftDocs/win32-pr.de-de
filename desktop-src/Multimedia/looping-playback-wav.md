---
title: Schleifen Wiedergabe (Waveform-Audiodatei)
description: Schleifen Wiedergabe (Waveform-Audiodatei)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- Wellenform-Audio, Schleifen Klänge
- Waveform-Audioschnittstelle, Schleifen Klänge
- Wellenform-Audiodaten, Schleifen Wiedergabe
- Waveform-Audioschnittstelle, Schleifen Wiedergabe
- Schleifen von Waveform-audiosounds
- Schleifen Wellenform-Audiowiedergabe
- waveOutWrite-Funktion
- waveoutbreakloop-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106371381"
---
# <a name="looping-playback"></a><span data-ttu-id="81282-111">Schleifen Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="81282-111">Looping Playback</span></span>

<span data-ttu-id="81282-112">Das Schleifen eines Sounds wird durch die **dwloops** -und **dwFlags** -Elemente in den [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Strukturen gesteuert, die mit der [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) -Funktion an das Gerät übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="81282-112">Looping a sound is controlled by the **dwLoops** and **dwFlags** members in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structures passed to the device with the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> <span data-ttu-id="81282-113">Verwenden Sie die Flags **whdr \_ BeginLoop** und **whdr \_ ENDLOOP** im **dwFlags** -Member, um die Anfangs-und Enddaten Blöcke für Schleifen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="81282-113">Use the **WHDR\_BEGINLOOP** and **WHDR\_ENDLOOP** flags in the **dwFlags** member to specify the beginning and ending data blocks for looping.</span></span>

<span data-ttu-id="81282-114">Wenn Sie einen einzelnen Datenblock Schleifen möchten, geben Sie beide Flags für denselben Block an.</span><span class="sxs-lookup"><span data-stu-id="81282-114">To loop a single data block, specify both flags for the same block.</span></span> <span data-ttu-id="81282-115">Um die Anzahl der Schleifen anzugeben, verwenden Sie den **dwloops** -Member in der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur für den ersten Block in der Schleife.</span><span class="sxs-lookup"><span data-stu-id="81282-115">To specify the number of loops, use the **dwLoops** member in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure for the first block in the loop.</span></span>

<span data-ttu-id="81282-116">Sie können die [**waveoutbreakloop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) -Funktion zum Anhalten eines audiosounds aufruft.</span><span class="sxs-lookup"><span data-stu-id="81282-116">You can call the [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) function to stop a looping sound.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81282-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81282-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81282-118">Wiedergabe Waveform-Audio Dateien</span><span class="sxs-lookup"><span data-stu-id="81282-118">Playing Waveform-Audio Files</span></span>](playing-waveform-audio-files.md)
</dt> </dl>

 

 
