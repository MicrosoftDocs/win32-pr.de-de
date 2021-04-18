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
# <a name="looping-playback"></a>Schleifen Wiedergabe

Das Schleifen eines Sounds wird durch die **dwloops** -und **dwFlags** -Elemente in den [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Strukturen gesteuert, die mit der [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) -Funktion an das Gerät übermittelt werden. Verwenden Sie die Flags **whdr \_ BeginLoop** und **whdr \_ ENDLOOP** im **dwFlags** -Member, um die Anfangs-und Enddaten Blöcke für Schleifen anzugeben.

Wenn Sie einen einzelnen Datenblock Schleifen möchten, geben Sie beide Flags für denselben Block an. Um die Anzahl der Schleifen anzugeben, verwenden Sie den **dwloops** -Member in der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur für den ersten Block in der Schleife.

Sie können die [**waveoutbreakloop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) -Funktion zum Anhalten eines audiosounds aufruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergabe Waveform-Audio Dateien](playing-waveform-audio-files.md)
</dt> </dl>

 

 
