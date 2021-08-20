---
title: Zeitsteuerungsinformationen
description: Zeitsteuerungsinformationen
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- Music Instrument Digital Interface (OPC), Zeitsteuerungsinformationen
- INSTRUMENTS (Music Instrument Digital Interface),Zeitsteuerungsinformationen
- Streampuffer, Zeitsteuerungsinformationen
- STRUKTURENEVENT-Struktur
- Streampuffer, SMPTE-Format
- Streampuffer, Quartalsnotizzeit
- Streampuffer, Ticks
- SMPTE-Format
- Uhrzeit der Quartalsnotiz
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a75be9964457c64c7c1da59cb93aab2e423f72e861ba496494a5007025461c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804740"
---
# <a name="timing-information"></a>Zeitsteuerungsinformationen

Zeitsteuerungsinformationen für ein CSV-Ereignis werden im **dwDeltaTime-Member** der [**ELEMENTSEVENT-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) gespeichert. Die Zeit wird in Ticks angegeben, wie in der *STANDARD-SPEZIFIKATION FÜR DATEIEN 1.0* definiert. Die Länge eines Ticks wird durch das Zeitformat und möglicherweise durch das dem Stream zugeordnete Tempo definiert. Weitere Informationen zu Streams finden Sie unter [CSV Streams](midi-streams.md).

Ein Tick wird entweder als Mikrosekunden pro Quartalsnotiz oder als Ticks der Zeit von SMPTE (Society of Motion Picture and Tv Engineers) ausgedrückt. Anwendungen, die CSV-Nachrichten einzeln senden oder unverarbeitete CAB-Nachrichten verwenden, verwenden Zeit- und Geschwindigkeitsinformationen für Quartalsnotizen, um die Dauer eines Ticks zu bestimmen. Anwendungen, die MELDUNGEN vorverarbeiten, können die verstrichene Zeit als Anzahl der verwendeten SMPTE-Einheiten speichern.

Die Quartalsnotizzeit wird mit einer Null im hohen Wortbit (Bit 15) des Zeitteilungsworts angegeben. Der Rest des Worts enthält die Ticks pro Quartalsnotiz. Ein Tempo, das einem Stream von CSV-Daten zugeordnet ist, wird in Einheiten (Mikrosekunden pro Quartalshinweis) beibehalten, die mit der *STANDARD-SPEZIFIKATION VON CAB Files 1.0* konsistent sind. Beispielsweise wird ein Quartalshinweis in 4/4-Zeit mit einem Tempo von 500.000 Mikrosekunden pro Quartal mit einer Rate von 120 Schlägen pro Minute wiedergegeben.

SMPTE-Zeitteilungsformate geben die Länge eines Ticks vollständig an, ohne dass Geschwindigkeitsinformationen erforderlich sind. Bei Verwendung von SMPTE-Zeitformaten können DIE SEQUENZEN mit anderen SMPTE-Ereignissen synchronisiert werden, z. B. Mit Video oder Stripesetaudio. Die SMPTE-Zeit wird mit einem 1 im hohen Bit (Bit 15) des Zeitteilungsworts angegeben. Der Rest des wichtigsten Byte gibt das SMPTE-Format an, das als negative Werte verwendet wird. Die unterstützten SMPTE-Formate und die entsprechenden Werte (in Klammern) sind 24 (-24), 25 (-25), 30 (-30) und 30 Drop (-29). Das niedrige Byte des Zeitteilungsworts gibt die Anzahl der Ticks pro SMPTE-Frame an.

 

 