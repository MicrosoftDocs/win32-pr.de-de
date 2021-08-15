---
title: Empfangen Time-Stamped-NACHRICHTEN
description: Empfangen Time-Stamped-NACHRICHTEN
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Instruments Instrument Digital Interface (KEYBOARD), Nachrichten mit Zeitstempel
- SOLLEN (Digital Interface für Instrumentieren), Nachrichten mit Zeitstempel
- Aufzeichnung von audio,time-stamped messages
- ZEITStempel-ZEITSTEMP-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec36628a417c19824e25c7ad013da9c539fe88cb6e58fd829a32205bce35679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371290"
---
# <a name="receiving-time-stamped-midi-messages"></a>Empfangen Time-Stamped-NACHRICHTEN

Aufgrund der Verzögerung zwischen dem Zeitpunkt, zu dem der Gerätetreiber eine MESSAGE-Nachricht empfängt, und dem Zeitpunkt, zu dem die Anwendung die Nachricht empfängt, stempelt DER EINGABE-Gerätetreiber den Zeitstempel der MESSAGE-Nachricht mit dem Zeitpunkt, zu dem die Nachricht empfangen wurde. ZEIT-Zeitstempel, die als der Zeitpunkt definiert sind, zu dem das erste Byte der Nachricht empfangen wurde, werden in Millisekunden angegeben. Die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) setzt die Zeitstempel für ein Gerät auf 0 (null) zurück.

Wie bereits erwähnt, müssen Sie eine Rückruffunktion verwenden, um Zeitstempel mit EINER EINGABE-Eingabe zu empfangen. Der *dwParam2-Parameter* der Rückruffunktion gibt den Zeitstempel für die Daten an, die den Daten MIM [**\_ DATA-**](mim-data.md) und MIM [**\_ LONGDATA-Nachrichten zugeordnet**](mim-longdata.md) sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von TONS-Audio](recording-midi-audio.md)
</dt> </dl>

 

 