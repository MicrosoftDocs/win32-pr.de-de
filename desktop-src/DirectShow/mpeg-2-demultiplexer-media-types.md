---
description: MPEG-2-Demultiplexer-Medientypen
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MPEG-2-Demultiplexer-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dfba52378813b8b96920a44c593e9c7d4b45a0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476276"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>MPEG-2-Demultiplexer-Medientypen

Der [MPEG-2-Demultiplexer-Filter](mpeg-2-demultiplexer.md) erkennt die folgenden Medientypen.

### <a name="input-types"></a>Eingabetypen

Der Haupttyp ist immer **MEDIATYPE \_ Stream.** Der Untertyp kann einer der folgenden sein.



| GUID                                             | Beschreibung                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_KSDATAFORMAT-UNTERTYP \_ BDA \_ \_ MPEG2-TRANSPORT** | Transportstream aus einem BDA-Gerätefilter (Broadcast Driver Architecture). Der MPEG-2-Demultiplexer behandelt diesen Untertyp identisch mit **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**.                                |
| **MEDIASUBTYPE \_ \_ MPEG2-PROGRAMM**                 | Programmstream                                                                                                                                                                                            |
| **MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT**               | Transportstream (TS) mit 188-Byte-Paketen                                                                                                                                                              |
| **MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT-STRIDE \_**       | Transportstream mit "strided"-Paketen. Dieser Untertyp gibt an, dass die TS-Pakete möglicherweise mit zusätzlichen Bytes aufschlossen werden. Weitere Informationen finden Sie unter [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). |



 

Bei Transportpaketen mit Striding **(MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE)** muss jedes Medienbeispiel eine ganzzahlige Anzahl von Transportpaketen enthalten, wie in [**MPEG2 \_ TRANSPORT \_ STRIDE beschrieben.**](mpeg2-transport-stride.md) Für alle anderen Eingabetypen gelten keine Einschränkungen für Beispielgrenzen. Einzelne Pakete können Beispielgrenzen umfassen.

### <a name="output-types"></a>Ausgabetypen

Der MPEG-2-Demultiplexer überprüft keine Ausgabetypen. Der Downstreamfilter ist für die Analyse der Vom Demultiplexer empfangenen Daten verantwortlich. Die folgenden Typen werden jedoch häufig von Downstreamfiltern als Ausgabe des Demultiplexers akzeptiert.

### <a name="mpeg-2-sections"></a>MPEG-2-Abschnitte




| | | Haupttyp | <strong>MEDIATYPE_MPEG2_SECTIONS</strong> | | Untertyp | Eine der folgenden Bedingungen:<br /><ul><li><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC-Dienstinformationen.</li><li><strong>MEDIASUBTYPE_DVB_SI</strong>: DIENSTINFORMATIONEN FÜR DEN DIENST .</li><li><strong>MEDIASUBTYPE_ISDB_SI</strong>: IsDB-Dienstinformationen (Integrated Services Digital Broadcasting).</li><li><strong>MEDIASUBTYPE_MPEG2DATA:</strong>MPEG-2-Abschnittsdaten.</li></ul> | | Formattyp-| Keine | 




 

### <a name="mpeg-2-video"></a>MPEG-2-Video



| Bezeichnung | Wert |
|------------------|------------------------------------------|
| Haupttyp       | **\_MEDIATYPE-Video**                     |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**           |
| Formattyp      | **FORMAT \_ MPEG2Video**                   |
| Formatstruktur | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>MPEG-2-Audio



| Bezeichnung | Wert |
|------------------|--------------------------------------|
| Haupttyp       | **MEDIATYPE \_ Audio**                 |
| Subtype          | **MEDIASUBTYPE \_ \_ MPEG2-AUDIO**       |
| Formattyp      | **FORMAT \_ WaveFormatEx**             |
| Formatstruktur | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 
