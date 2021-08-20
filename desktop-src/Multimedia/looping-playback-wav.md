---
title: Looping Playback (Waveform Audio)
description: Looping Playback (Waveform Audio)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- Waveform-Audio, Looping-Sounds
- Waveform-Audio-Schnittstelle, Looping-Sounds
- Waveform-Audio, Loopingwiedergabe
- waveform-audio interface,looping playback
- Looping waveform-audio sounds
- Looping der Wiedergabe von Waveform-Audio
- waveOutWrite-Funktion
- waveOutBreakLoop-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d98732ccc0a1d75ad13a10dc881b66a3bb634beab03a95a86a9db5689890979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139311"
---
# <a name="looping-playback"></a>Schleifenwiedergabe

Die Schleife eines Sounds wird von den **dwLoops-** und **dwFlags-Membern** in den [**WAVEHDR-Strukturen**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) gesteuert, die mit der [**waveOutWrite-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) an das Gerät übergeben werden. Verwenden Sie **die Flags WHDR \_ BEGINLOOP** und **WHDR \_ ENDLOOP** im **dwFlags-Member,** um die Anfangs- und Enddatenblöcke für Schleifen anzugeben.

Um eine Schleife für einen einzelnen Datenblock zu verwenden, geben Sie beide Flags für denselben Block an. Um die Anzahl der Schleifen anzugeben, verwenden Sie den **dwLoops-Member** in der [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) für den ersten Block in der Schleife.

Sie können die [**waveOutBreakLoop-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) aufrufen, um einen Schleifenklang zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergabe Waveform-Audio Dateien](playing-waveform-audio-files.md)
</dt> </dl>

 

 
