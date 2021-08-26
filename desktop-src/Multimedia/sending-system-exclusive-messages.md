---
title: Senden System-Exclusive Nachrichten
description: Senden System-Exclusive Nachrichten
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Instruments Instrument Digital Interface (KEYBOARD), Senden von Nachrichten
- KEYBOARD (Instruments Instrument Digital Interface), Senden von Nachrichten
- Wiedergeben von DANN-Dateien, Senden von Nachrichten
- Senden von SIGNAL-Nachrichten
- Instruments Instrument Digital Interface (LUS), system-exklusive Nachrichten
- LUS (Instrument Digital Interface), ausschließliche Systemnachrichten
- Wiedergeben von DANN-Dateien, exklusive Systemmeldungen
- system-exclusive-SYSTEMS-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad97371f56c042e5acd230aba6144f5f9734a594b370a791422b2e8f8148861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037260"
---
# <a name="sending-system-exclusive-messages"></a>Senden System-Exclusive Nachrichten

DIE system-exklusiven Nachrichten sind die einzigen VOMT-Nachrichten, die nicht in einen einzelnen Doublewordwert passen. System-exklusive Nachrichten können eine beliebige Länge haben. Windows stellt die [**funktion "sollenOutLongMsg"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) zum Senden von system-exklusiven Nachrichten an DIE-Ausgabegeräte zur Verfügung. Verwenden Sie zum Angeben von exklusiven SYSTEM-EXKLUSIVEn [**Datenblöcken die BLOCKHDR-Struktur.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

Nachdem Sie einen system-exklusiven Datenblock **mithilfe von "blocksOutLongMsg"** gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn wieder frei geben. Wenn Sie mehrere Datenblöcke senden, müssen Sie die Vervollständigung jedes Datenblocks überwachen, damit Sie wissen, wann zusätzliche Blöcke gesendet werden sollen. Informationen zu verschiedenen Techniken zum Überwachen der Datenblockvervollständigung finden Sie unter [Verwalten von BLOCK-Datenblöcken.](managing-midi-data-blocks.md)

> [!Note]  
> Jedes andere STATUS-Byte als eine System-Echtzeitmeldung beendet eine system-exklusive Nachricht. Wenn Sie mehrere Datenblöcke verwenden, um eine einzelne system-exklusive Nachricht zu senden, senden Sie keine ANDEREN NACHRICHTEN als System-Echtzeitnachrichten zwischen Datenblöcken.

 

 

 