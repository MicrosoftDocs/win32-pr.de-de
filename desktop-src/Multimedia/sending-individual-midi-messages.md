---
title: Senden einzelner MIDI-Nachrichten
description: Senden einzelner MIDI-Nachrichten
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
- Digital Instrumentation Digital Interface (MIDI), individuelle Nachrichten
- MIDI (Digital Instrumentation Digital Interface), individuelle Nachrichten
- Abspielen von MIDI-Dateien, einzelnen Nachrichten
- einzelne MIDI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339875"
---
# <a name="sending-individual-midi-messages"></a>Senden einzelner MIDI-Nachrichten

Sie können mit den folgenden Funktionen mit einzelnen MIDI-Nachrichten arbeiten.



| Wert                                      | Bedeutung                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Sendet einen Puffer von MIDI-Daten an das angegebene MIDI-Ausgabegerät. Verwenden Sie diese Funktion, um System exklusive Nachrichten an ein MIDI-Gerät zu senden.                                              |
| [**falsch einwählsatz**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Deaktiviert alle Notizen für ein angegebenes MIDI-Ausgabegerät in allen Kanälen. Alle ausstehenden System exklusiven Puffer und Streampuffer werden als abgeschlossen markiert und an die Anwendung zurückgegeben. |
| [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Sendet eine MIDI-Nachricht an ein angegebenes MIDI-Ausgabegerät.                                                                                                                             |



 

Verwenden Sie [**midioutshortmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg), um eine beliebige MIDI-Nachricht (mit Ausnahme von System exklusiven Nachrichten) zu senden.

 

 