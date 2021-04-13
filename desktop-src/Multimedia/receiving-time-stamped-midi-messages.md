---
title: Empfangen Time-Stamped von MIDI-Nachrichten
description: Empfangen Time-Stamped von MIDI-Nachrichten
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Digital Instrumentation Digital Interface (MIDI), Nachrichten mit Zeitstempel
- MIDI (Digital Instrumentation Digital Interface), Nachrichten mit Zeitstempel
- Aufzeichnen von MIDI-Audiodaten, Zeitstempel Meldungen
- mit Zeitstempel versehene MIDI-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314864"
---
# <a name="receiving-time-stamped-midi-messages"></a>Empfangen Time-Stamped von MIDI-Nachrichten

Aufgrund der Verzögerung zwischen dem Zeitpunkt, zu dem der Gerätetreiber eine MIDI-Nachricht empfängt, und dem Zeitpunkt, zu dem die Anwendung die Nachricht empfängt, wird die MIDI-Nachricht von den MIDI-Eingabe-Gerätetreibern mit dem Zeitpunkt der Nachrichten Empfangszeit versehen. Die Zeitstempel von MIDI, die als Zeitpunkt definiert werden, zu dem das erste Byte der Nachricht empfangen wurde, werden in Millisekunden angegeben. Die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion setzt die Zeitstempel für ein Gerät auf 0 (null) zurück.

Wie bereits erwähnt, müssen Sie zum Empfangen von Zeitstempeln mit der Verwendung von MIDI eine Rückruffunktion verwenden. Der *dwParam2* -Parameter der Rückruffunktion gibt den Zeitstempel für die Daten an, die den [**MIM- \_ Daten**](mim-data.md) und [**MIM \_ longdata**](mim-longdata.md) -Nachrichten zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von MIDI-Audiodateien](recording-midi-audio.md)
</dt> </dl>

 

 