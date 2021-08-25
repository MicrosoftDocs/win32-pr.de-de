---
title: Zuordnen und Vorbereiten von DATENQUELLEN-Datenblöcken
description: Zuordnen und Vorbereiten von DATENQUELLEN-Datenblöcken
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Music Instrument Digital Interface (OPC), Zuordnen von Datenblöcken
- DATENQUELLEN (Digitale Schnittstelle für Musikinstrument),Zuordnen von Datenblöcken
- DATENQUELLENDIENSTE,Zuordnen von Datenblöcken
- Zuordnen von DATENQUELLEN-Datenblöcken
- Instruments Digital Interface (INSTRUMENT Digital Interface), Vorbereiten von Datenblöcken
- INSTRUMENTS (Music Instrument Digital Interface),Vorbereiten von Datenblöcken
- DATENQUELLENDIENSTE,Vorbereiten von Datenblöcken
- Vorbereiten von BLOCKS-Datenblöcken
- Music Instrument Digital Interface (OPC), Datenblöcke
- INSTRUMENTS (Music Instrument Digital Interface), Datenblöcke
- DIENSTEN,DATENBLÖCKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137556c1344e6f2e8db8557d45a70c5981fa7bab99e7452cc1f756b4a8ee159b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808490"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Zuordnen und Vorbereiten von DATENQUELLEN-Datenblöcken

Die Funktionen [**"bedOutLongMsg",**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) [**"turboInAddBuffer"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)und [**"streamingStreamOut"**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) erfordern, dass Anwendungen Datenblöcke zuordnen müssen, die zur Wiedergabe oder Aufzeichnung an die Gerätetreiber übergeben werden. Jede dieser Funktionen verwendet eine [**CSVHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) um ihren Datenblock zu beschreiben.

Bevor Sie eine dieser Funktionen verwenden, um einen Datenblock an einen Gerätetreiber zu übergeben, müssen Sie Speicher für den Puffer und die Headerstruktur zuordnen, die den Datenblock beschreibt.

Windows stellt die folgenden Funktionen zum Vorbereiten und Bereinigen von CSV-Datenblöcken bereit.



| Wert                                                    | Bedeutung                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**partsInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Bereitet einen INPUT-Datenblock vor.                      |
| [**partsInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Bereinigt die Vorbereitung eines INPUT-Eingabedatenblocks.  |
| [**partsOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Bereitet einen OUTPUT-Ausgabedatenblock vor.                     |
| [**partsOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Bereinigt die Vorbereitung eines CSV-Ausgabedatenblocks. |



 

Bevor Sie einen BLOCKS-Datenblock an einen Gerätetreiber übergeben, müssen Sie den Puffer vorbereiten, indem Sie ihn an die [**Funktion "sysInPrepareHeader"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) oder [**"pubOutPrepareHeader"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) übergeben. Wenn der Gerätetreiber mit dem Puffer fertig ist und ihn zurückgibt, müssen Sie diese Vorbereitung bereinigen, indem Sie den Puffer an die [**Funktion "sysInUnprepareHeader"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) oder [**"outUnprepareHeader"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) übergeben, bevor der zugeordnete Arbeitsspeicher freigegeben werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PARTS-Dienste](midi-services.md)
</dt> </dl>

 

 