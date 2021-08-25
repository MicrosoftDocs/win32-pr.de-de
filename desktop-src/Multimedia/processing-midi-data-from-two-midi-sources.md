---
title: Verarbeiten von DATENQUELLEN aus zwei DATENQUELLEN
description: Verarbeiten von DATENQUELLEN aus zwei DATENQUELLEN
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows Multimedia, Verarbeiten von DATENQUELLEN aus zwei Quellen
- Multimedia, Verarbeiten von DATENQUELLEN aus zwei Quellen
- Multimediaaudio, Verarbeiten von AUDIO-Daten aus zwei Quellen
- Audio, Verarbeiten von AUDIO-Daten aus zwei Quellen
- Music Instrument Digital Interface (OPC), Verarbeiten von Daten aus zwei Quellen
- INSTRUMENTS (Music Instrument Digital Interface),Verarbeiten von Daten aus zwei Quellen
- Verarbeiten von DATENQUELLEN aus zwei Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5eb31c4c6b4b965321b7458d058a3547426b95236d6e0b52d6eb0f55b3e74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805790"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Verarbeiten von DATENQUELLEN aus zwei DATENQUELLEN

Das SUBSYSTEM FÜR DAS SUBSYSTEM kann MELDUNGEN aus zwei Datenquellen an ein einzelnes OUTPUT-Ausgabegerät für die gleichzeitige Wiedergabe weiterleiten. Eine Quelle kann z. B. Hintergrund-Musik oder eine Blasenlinie sein, die vorab aufgezeichnet und in einer Datei gespeichert wurde. Die zweite Quelle kann Livedaten von einem INSTRUMENT sein, z. B. einer Tastatur oder einem Messgerät.

Beide Datenquellen senden DIE DATEN an ein einzelnes DATENQUELLEN-Gerät, das mit einem Handle identifiziert wird. Senden Sie einen Datenstrom mithilfe der [**funktion "streamsStreamOut"**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) und mindestens einem Streampuffer. Dieser Datenstrom enthält in der Regel vorab aufgezeichnete Daten, die in den Puffer gepackt werden.

Senden Sie den zweiten Datenstrom (in der Regel von einem INSTRUMENT)) asynchron mithilfe der [**funktionoutShortMsg.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) Der Ausführungsstatus eines Streampuffers wird durch die asynchronen Aufrufe des zweiten Datenstroms nicht beeinträchtigt.

Jede kurze Nachricht, die mit **dem Befehl "grubOutShortMsg"** gesendet wird, muss eine vollständige MSI-Nachricht mit einem Statusbyte und der entsprechenden Anzahl von Datenbytes sein. Wenn das Status-Byte ausgelassen wird, gibt **die dateioutShortMsg** einen Fehler zurück. (Es gibt jedoch keinen Ausführungsstatus mit Streamausgabe.)

 

 