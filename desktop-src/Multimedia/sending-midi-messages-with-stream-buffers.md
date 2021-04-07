---
title: Senden von MIDI-Nachrichten mit streampuffern
description: Senden von MIDI-Nachrichten mit streampuffern
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- Digital Instrumentation Digital Interface (MIDI), Streampuffer
- MIDI (Digital Instrumentation Digital Interface), Streampuffer
- Abspielen von MIDI-Dateien, Streampuffer
- Streampuffer, Senden von MIDI-Nachrichten
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725360"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>Senden von MIDI-Nachrichten mit streampuffern

Wenn Ihre Anwendung mit streampuffern arbeitet, wird die [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) -Funktion verwendet, um alle (kurzen und langen) MIDI-Nachrichten an das Gerät zu senden. Um streamdatenblöcke anzugeben, verwenden Sie die [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -und [**MidiEvent**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) -Strukturen. Die **midihdr** -Struktur enthält die Adresse eines gesperrten Datenblocks, die datenblocklänge und einige sortierte Flags. Die Daten werden in Form von **MidiEvent** -Strukturen gespeichert. Das System erzwingt eine Größenbeschränkung von 64 KB für Streampuffer.

Nachdem Sie **mithilfe von midistreamout** einen Streampuffer mit Daten gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn freigeben. Wenn Sie mehrere Datenblöcke senden, müssen Sie den Abschluss der einzelnen Datenblöcke überwachen, damit Sie wissen, wann zusätzliche Blöcke gesendet werden sollen. Informationen zu den verschiedenen Techniken zum Überwachen der Datenblock Vervollständigung finden Sie unter [Verwalten von MIDI-Datenblöcken](managing-midi-data-blocks.md).

 

 