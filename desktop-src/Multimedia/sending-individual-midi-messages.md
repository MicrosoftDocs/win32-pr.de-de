---
title: Senden einzelner SIGNAL-Nachrichten
description: Senden einzelner SIGNAL-Nachrichten
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Instruments Instrument Digital Interface (KEYBOARD), Senden von Nachrichten
- KEYBOARD (Instruments Instrument Digital Interface), Senden von Nachrichten
- Wiedergeben von DANN-Dateien, Senden von Nachrichten
- Senden von SIGNAL-Nachrichten
- Instruments Instrument Digital Interface (KEYBOARD), einzelne Nachrichten
- KEYBOARD (Instrument Digital Interface), einzelne Nachrichten
- Wiedergeben von DANN-Dateien,einzelne Nachrichten
- einzelneR DANN-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1f73d0956004f90644ce2e8b0e41b368137a7b61fd04e6d17302619980336d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037450"
---
# <a name="sending-individual-midi-messages"></a>Senden einzelner SIGNAL-Nachrichten

Sie können mit den folgenden Funktionen mit einzelnen DANN-Nachrichten arbeiten.



| Wert                                      | Bedeutung                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ohneLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Sendet einen Puffer vonBENACHRICHTIGUNG-Daten an das angegebene OUTPUT-Gerät. Verwenden Sie diese Funktion, um system-exklusive Nachrichten an einBENACHRICHTIGUNG-Gerät zu senden.                                              |
| [**ohne Rücksendung**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Deaktiviert alle Notizen auf allen Kanälen für ein angegebenes SENDER-Ausgabegerät. Alle ausstehenden system-exklusiven Puffer und Streampuffer werden als abgeschlossen markiert und an die Anwendung zurückgegeben. |
| [**ohne ShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Sendet eine SIGNAL-Nachricht an ein angegebenes OUTPUT-Gerät.                                                                                                                             |



 

Verwenden Sie zum Senden einer beliebigen DANN-Nachricht (mit Ausnahme von system-exklusiven [**Nachrichten) die BenachrichtigungsdateiOutShortMsg.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)

 

 