---
title: Verwalten der MIDI-Aufzeichnung
description: Verwalten der MIDI-Aufzeichnung
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Digital Instrumentation Digital Interface (MIDI), aufzeichnen
- MIDI (Digital Interface Digital Interface), aufzeichnen
- Aufzeichnen von MIDI-Audiodaten, verwalten
- MIDI-Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472773"
---
# <a name="managing-midi-recording"></a>Verwalten der MIDI-Aufzeichnung

Nachdem Sie ein MIDI-Gerät geöffnet haben, können Sie damit beginnen, die Daten von MIDI aufzuzeichnen. Windows stellt die folgenden Funktionen zum Verwalten der MIDI-Aufzeichnung bereit.



| Wert                                      | Bedeutung                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Sendet einen Puffer an den Gerätetreiber, damit er mit aufgezeichneten System exklusiven MIDI-Daten gefüllt werden kann. |
| [**midiinreset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Beendet die Aufzeichnung von MIDI und markiert alle ausstehenden Puffer als abgeschlossen.                                       |
| [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Startet die MIDI-Aufzeichnung und setzt den Zeitstempel auf NULL zurück.                                          |
| [**midiinstop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Beendet die Aufzeichnung von MIDI.                                                                             |



 

Verwenden Sie [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), um Puffer an den Gerätetreiber zum Aufzeichnen von System exklusiven Nachrichten zu senden. Die Anwendung wird benachrichtigt, wenn die Puffer mit System exklusiven aufgezeichneten Daten gefüllt werden. Weitere Informationen zu den Benachrichtigungs Techniken finden Sie unter [Verwalten von MIDI-Datenblöcken](managing-midi-data-blocks.md).

Die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion beginnt den Aufzeichnungsprozess. Wenn Sie System exklusive Nachrichten aufzeichnen, senden Sie mindestens einen Puffer an den Treiber, bevor Sie die Aufzeichnung starten. Verwenden Sie zum Anhalten der Aufzeichnung [**midiinstop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop). Markieren Sie vor dem Schließen des Geräts mithilfe der [**midiinclose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) -Funktion alle ausstehenden Datenblöcke als durch den Aufruf von [**midiinreset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Anwendungen, die Zeitstempel Daten benötigen, verwenden eine Rückruffunktion, um die Daten von MIDI zu empfangen. Wenn Ihre Zeit Steuerungsanforderungen nicht strikt sind, können Sie einen Fenster-oder Thread Rückruf verwenden. Es ist jedoch nicht möglich, einen Ereignis Rückruf zum Empfangen von MIDI-Daten zu verwenden.

Zum Aufzeichnen von System exklusiven Nachrichten mit Anwendungen, die keine Streampuffer verwenden, müssen Sie den Gerätetreiber mit Puffern bereitstellen. Diese Puffer werden mithilfe einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von MIDI-Audiodateien](recording-midi-audio.md)
</dt> </dl>

 

 