---
title: Verwalten der TONS-Aufzeichnung
description: Verwalten der TONS-Aufzeichnung
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Instrument Digital Interface (KEYBOARD), Aufzeichnung
- KEYBOARD (Keyboard Instrument Digital Interface), Aufzeichnung
- Aufzeichnen von AUDIOdateien mit DER TON,Verwalten
- RECORDING-Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bf4ac85ad0cc9735a08bab3ee07d744eecb0d75308ee323ec93c1c69b1a9e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139061"
---
# <a name="managing-midi-recording"></a>Verwalten der TONS-Aufzeichnung

Nachdem Sie ein DANN-Gerät geöffnet haben, können Sie mit der Aufzeichnung von SOLLTEN-Daten beginnen. Windows stellt die folgenden Funktionen für die Verwaltung der TONT-Aufzeichnung zur Verfügung.



| Wert                                      | Bedeutung                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**bluInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Sendet einen Puffer an den Gerätetreiber, damit er mit aufgezeichneten system-exklusiven DABEI-Daten gefüllt werden kann. |
| [**keyboardInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Beendet die RECORDING-Aufzeichnung und markiert alle ausstehenden Puffer wie abgeschlossen.                                       |
| [**durchstartenInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Startet die RECORDING-Aufzeichnung und setzt den Zeitstempel auf 0 (null) zurück.                                          |
| [**keyboardInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Beendet die STOPP-Aufzeichnung.                                                                             |



 

Verwenden Sie zum Senden von Puffern an den Gerätetreiber zum Aufzeichnen von system-exklusiven Nachrichten [**die Datei "bluInAddBuffer".**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) Die Anwendung wird benachrichtigt, wenn die Puffer mit vom System exklusiven aufgezeichneten Daten gefüllt werden. Weitere Informationen zu den Benachrichtigungstechniken finden Sie unter [Verwalten von NOTIFICATION-Datenblöcken.](managing-midi-data-blocks.md)

Die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) startet den Aufzeichnungsprozess. Senden Sie beim Aufzeichnen von system exklusiven Nachrichten mindestens einen Puffer an den Treiber, bevor Sie mit der Aufzeichnung beginnen. Um die Aufzeichnung zu beenden, [**verwenden Sie "sollInStop".**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop) Markieren Sie alle ausstehenden Datenblöcke vor dem Schließen des Geräts mithilfe der [**funktion "sollInClose"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) als abgeschlossen, indem Sie [**"mussInReset" aufrufen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)

Anwendungen, die Zeitstempeldaten benötigen, verwenden eine Rückruffunktion, um DIE Daten zu empfangen. Wenn Ihre zeitlichen Anforderungen nicht streng sind, können Sie einen Fenster- oder Threadrückruf verwenden. Sie können jedoch keinen Ereignisrückruf verwenden, um DIE Daten zu empfangen.

Zum Aufzeichnen von system-exklusiven Nachrichten mit Anwendungen, die keine Streampuffer verwenden, müssen Sie den Gerätetreiber mit Puffern versorgen. Diese Puffer werden mithilfe einer [**FORMATHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von TONS-Audio](recording-midi-audio.md)
</dt> </dl>

 

 