---
title: Verwalten Waveform-Audio Aufzeichnung
description: Verwalten Waveform-Audio Aufzeichnung
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- Waveform-Audio, Aufzeichnung
- Waveform-Audio-Schnittstelle, Aufzeichnung
- Aufzeichnen von Waveform-Audio, Informationen
- WAVEHDR-Struktur
- waveInAddBuffer-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d798cb1b6a8a22f4c695bced89dd669346ad2bb6452179df1d3278af8681aa49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138933"
---
# <a name="managing-waveform-audio-recording"></a>Verwalten Waveform-Audio Aufzeichnung

Nachdem Sie ein Waveform-Audio-Eingabegerät geöffnet haben, können Sie mit der Aufzeichnung von Waveform-Audio-Daten beginnen. Waveform-Audiodaten werden in von der Anwendung bereitgestellten Puffern aufgezeichnet, die durch eine [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) angegeben werden. Diese Datenblöcke müssen vorbereitet werden, bevor sie verwendet werden. Weitere Informationen finden Sie unter [Audiodatenblöcke.](audio-data-blocks.md)

Windows bietet die folgenden Funktionen zum Verwalten der Waveform-Audioaufzeichnung.



| Funktion                                   | Beschreibung                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Sendet einen Puffer an den Gerätetreiber, damit er mit aufgezeichneten Waveform-Audiodaten gefüllt werden kann. |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Beendet die Waveform-Audioaufzeichnung und markiert alle ausstehenden Puffer wie abgeschlossen.                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Startet die Waveform-Audioaufzeichnung.                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Beendet die Waveform-Audioaufzeichnung.                                                            |



 

Verwenden Sie die [**waveInAddBuffer-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) um Puffer an den Gerätetreiber zu senden. Da die Puffer mit aufgezeichneten Waveform-Audiodaten gefüllt werden, wird die Anwendung mit einer Fenstermeldung, Rückrufnachricht, Threadnachricht oder einem Ereignis benachrichtigt, abhängig von dem Flag, das beim Öffnen des Geräts angegeben wurde.

Bevor Sie mit der Aufzeichnung mit [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)beginnen, sollten Sie mindestens einen Puffer an den Treiber senden. Andernfalls könnten eingehende Daten verloren gehen.

Rufen Sie vor dem Schließen des Geräts mit [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) auf, um alle ausstehenden Datenblöcke als erledigt zu markieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audio](recording-waveform-audio.md)
</dt> </dl>

 

 