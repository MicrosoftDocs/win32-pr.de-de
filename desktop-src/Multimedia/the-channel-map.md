---
title: Die Kanalzuordnung
description: Die Kanalzuordnung
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Instruments Instrument Digital Interface (INSTRUMENTS), MAPPer
- INSTRUMENTS (Digitale Schnittstelle des Instrumentierers), MAPPER
- MAPPer, Kanalzuordnung
- Kanalzuordnung
- MAPPer, Kanalmeldungen
- MELDUNGEN DES KANALS
- Kanalnachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d514b5af6df6426db7cc5a313d1c6a52070a49c22a8a04e8cd2a9c34f49d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688285"
---
# <a name="the-channel-map"></a>Die Kanalzuordnung

Die Kanalzuordnung wirkt sich auf alle MELDUNGEN des CHANNELS aus. ZU DEN CHANNEL-Nachrichten gehören Meldungen zu Note-On, Note Off, polyphoneic-key-aftertouch, control-change, program-change, channel-aftertouch und pitch-itch-change. Der MAPPER verwendet eine einzelne Kanalzuordnung mit einem Eintrag für jeden der 16 CHANNELS-Kanäle. Jeder Kanalzuordnungseintrag gibt Folgendes an:

-   Ein Zielkanal für die FEHLERMELDUNG
-   Ein Zielausgabegerät für die FEHLERMELDUNG
-   Eine optionale Patch map, die andere mögliche Änderungen für die FEHLERMELDUNG angibt

Der Zielkanal ist auf einen der 16CHANNEL-Kanäle festgelegt. DIE MELDUNGEN werden geändert, um jede neue Kanalzuweisung widerzuspiegeln. Wenn z. B. der Zielkanaleintrag für DEN KANAL 4 auf 6 festgelegt ist, werden alle an Kanal 4 gesendeten SENDENACHRICHTEN dem Kanal 6 zugeordnet, wie in der folgenden Abbildung dargestellt.

![zugeordnetes Bild](images/mmap-a05.gif)

In diesem Beispiel wird der STATUS byte 0x93 0x95 zugeordnet. Die niedrige Reihenfolge eines STATUS-Byte gibt die Kanalnummer an. Quellkanäle werden entweder auf aktiv oder inaktiv festgelegt. Nachrichten, die an inaktive Quellkanäle gesendet werden, werden ignoriert, sodass ein inaktiver Kanal stummgeschaltet oder deaktiviert ist.

Das Zielausgabegerät ist auf eines der verfügbaren OUTPUT-Ausgabegeräte festgelegt. Ein OUTPUT-Ausgabegerät kann ein interner Synthesizer oder ein physischer ZIP-Ausgabeport sein.

BEI DEN SYSTEMMELDUNGEN handelt es sich um MELDUNGEN (mit Statusbytes) von 0xF0 bis 0xFF. ES ist kein Kanal zugeordnet, der DEN SYSTEMMELDUNGEN zugeordnet ist, sodass sie nicht zugeordnet werden können. WARNMELDUNG-Systemmeldungen werden an alle in einer Kanalzuordnung aufgeführten OUTPUT-Ausgabegeräte gesendet.

 

 




