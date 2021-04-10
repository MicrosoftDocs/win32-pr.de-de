---
title: Senden von System-Exclusive Nachrichten
description: Senden von System-Exclusive Nachrichten
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
- Digital Instrumentation Digital Interface (MIDI), System exklusive Meldungen
- MIDI (Digital Instrumentation Digital Interface), System exklusive Nachrichten
- Abspielen von MIDI-Dateien, System exklusive Nachrichten
- System exklusive MIDI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858167"
---
# <a name="sending-system-exclusive-messages"></a>Senden von System-Exclusive Nachrichten

System exklusive System-Nachrichten sind die einzigen MIDI-Nachrichten, die nicht in einen einzelnen Double Word-Wert passen. System exklusive Nachrichten können eine beliebige Länge aufweisen. Windows stellt die [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) -Funktion zum Senden von System exklusiven Nachrichten an die MIDI-Ausgabegeräte bereit. Verwenden Sie die [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, um System exklusive Systemdaten Blöcke anzugeben.

Nachdem Sie einen System exklusiven Datenblock mithilfe von **midioutlongmsg** gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn freigeben. Wenn Sie mehrere Datenblöcke senden, müssen Sie den Abschluss der einzelnen Datenblöcke überwachen, damit Sie wissen, wann zusätzliche Blöcke gesendet werden sollen. Informationen zu den verschiedenen Techniken zum Überwachen der Datenblock Vervollständigung finden Sie unter [Verwalten von MIDI-Datenblöcken](managing-midi-data-blocks.md).

> [!Note]  
> Alle anderen Bytes als eine System-Real-Time-Nachricht beenden eine System exklusive Nachricht. Wenn Sie mehrere Datenblöcke verwenden, um eine einzelne System exklusive Nachricht zu senden, senden Sie keine anderen als System-Real-Time-Meldungen zwischen den Datenblöcken.

 

 

 