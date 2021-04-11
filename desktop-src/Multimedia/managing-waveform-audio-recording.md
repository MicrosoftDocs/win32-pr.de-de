---
title: Verwalten von Waveform-Audio Aufzeichnung
description: Verwalten von Waveform-Audio Aufzeichnung
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- Wellenform-Audiodaten, aufzeichnen
- Waveform-Audioschnittstelle, aufzeichnen
- Aufzeichnen von Wellenform-Audiodaten, Info
- Wavehdr-Struktur
- waveinaddbuffer-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314774"
---
# <a name="managing-waveform-audio-recording"></a>Verwalten von Waveform-Audio Aufzeichnung

Nachdem Sie ein Waveform-Audioeingabegerät geöffnet haben, können Sie mit dem Aufzeichnen von Waveform-Audiodaten beginnen. Waveform-Audiodaten werden in von der Anwendung bereitgestellten Puffern aufgezeichnet, die durch eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur angegeben werden. Diese Datenblöcke müssen vorbereitet werden, bevor Sie verwendet werden. Weitere Informationen finden Sie unter [Audiodatenblöcke](audio-data-blocks.md).

Windows stellt die folgenden Funktionen zum Verwalten der Waveform-Audioaufzeichnung bereit.



| Funktion                                   | BESCHREIBUNG                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Sendet einen Puffer an den Gerätetreiber, damit er mit aufgezeichneten Wellenform-Audiodaten gefüllt werden kann. |
| [**waveingereset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Hält die Wellenform-Audioaufzeichnung an und markiert alle ausstehenden Puffer als abgeschlossen.                      |
| [**wavanstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Startet die Waveform-Audioaufzeichnung.                                                           |
| [**WaveIn-Ende**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Beendet die Wellenform-Audioaufzeichnung.                                                            |



 

Verwenden Sie die Funktion [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) , um Puffer an den Gerätetreiber zu senden. Wenn die Puffer mit aufgezeichneten Wellenform-Audiodaten gefüllt sind, wird die Anwendung in Abhängigkeit von dem Flag, das beim Öffnen des Geräts angegeben wurde, mit einer Fenster Meldung, einer Rückruf Meldung, einer Thread Nachricht oder einem Ereignis benachrichtigt.

Bevor Sie mit der Aufzeichnung mit [**waveinstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)beginnen, sollten Sie mindestens einen Puffer an den Treiber senden, oder es können eingehende Daten verloren gehen.

Bevor Sie das Gerät mithilfe von [**waveinclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)schließen, wenden Sie [**waveinreset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) an, um alle ausstehenden Datenblöcke als abgeschlossen zu markieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audiodaten](recording-waveform-audio.md)
</dt> </dl>

 

 