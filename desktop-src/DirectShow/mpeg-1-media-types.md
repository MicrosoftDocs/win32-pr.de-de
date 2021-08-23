---
description: In diesem Abschnitt werden die Medientypen aufgelistet, die für MPEG-1-Daten verwendet werden.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: MPEG-1-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f6486b455fc2045ceb0256f6b6344f06a8923ef767c397068022acec052627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684930"
---
# <a name="mpeg-1-media-types"></a>MPEG-1-Medientypen

In diesem Abschnitt werden die Medientypen aufgelistet, die für MPEG-1-Daten verwendet werden.

## <a name="mpeg-1-system-stream"></a>MPEG-1-Systemdatenstrom



| Bezeichnung | Wert |
|-----------------------|-------------------------------------------------|
| Haupttyp            | \_MEDIATYPE-Stream                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1System                       |
| Formattyp           | FORMAT \_ MPEGStreams                             |
| Formatstruktur      | [**AM \_ MPEGSYSTEMTYPE**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Medienbeispielinhalt | Bytestream; Keine Ausrichtung                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>MPEG-1-Systemstream aus Video-CD



| Bezeichnung | Wert |
|-----------------------|----------------------------|
| Haupttyp            | \_MEDIATYPE-Stream          |
| Subtype               | MEDIASUBTYPE \_ MPEG1VideoCD |
| Formattyp           | GUID \_ NULL                 |
| Formatstruktur      | Keine                       |
| Medienbeispielinhalt | Bytestream; keine Ausrichtung. |



 

## <a name="mpeg-1-audio-packet"></a>MPEG-1-Audiopaket



| Bezeichnung | Wert |
|-----------------------|------------------------------------------------|
| Haupttyp            | MEDIATYPE \_ Audio                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Formattyp           | FORMAT \_ WaveFormatEx                           |
| Formatstruktur      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Medienbeispielinhalt | Einzelnes MPEG-1-Paket, einschließlich Paketheader. |



 

## <a name="mpeg-1-audio-payload"></a>MPEG-1-Audionutzlast



| Bezeichnung | Wert |
|-----------------------|--------------------------------------------|
| Haupttyp            | MEDIATYPE \_ Audio                           |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload                 |
| Formattyp           | FORMAT \_ WaveFormatEx                       |
| Formatstruktur      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Medienbeispielinhalt | Bytebündig ausgerichtete MPEG-1-Audiodaten.            |



 

## <a name="mpeg-1-video-packet"></a>MPEG-1-Videopaket



| Bezeichnung | Wert |
|-----------------------|------------------------------------------------|
| Haupttyp            | \_MEDIATYPE-Video                               |
| Subtype               | MEDIASUBTYPE \_ MPEG1Packet                      |
| Formattyp           | FORMAT \_ MPEGVideo                              |
| Formatstruktur      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Medienbeispielinhalt | Einzelnes MPEG-1-Paket, einschließlich Paketheader. |



 

## <a name="mpeg-1-video-payload"></a>MPEG-1-Videonutzlast



| Bezeichnung | Wert |
|-----------------------|------------------------------------------|
| Haupttyp            | \_MEDIATYPE-Video                         |
| Subtype               | MEDIASUBTYPE \_ MPEG1Payload               |
| Formattyp           | FORMAT \_ MPEGVideo                        |
| Formatstruktur      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Medienbeispielinhalt | Bytebündige MPEG-1-Videodaten.          |



 

## <a name="mpeg-1-native-video-stream"></a>MPEG-1 Nativer Videostream



| Bezeichnung | Wert |
|-----------------------|------------------------------------------------|
| Haupttyp            | \_MEDIATYPE-Stream                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Video                      |
| Formattyp           | GUID \_ NULL                                     |
| Formatstruktur      | Keine                                           |
| Medienbeispielinhalt | Array von Videostreambytes (keine Systemebene). |



 

## <a name="mpeg-1-native-audio-stream"></a>MPEG-1 Nativer Audiostream



| Bezeichnung | Wert |
|-----------------------|------------------------------------------------|
| Haupttyp            | \_MEDIATYPE-Stream                              |
| Subtype               | MEDIASUBTYPE \_ MPEG1Audio                      |
| Formattyp           | GUID \_ NULL                                     |
| Formatstruktur      | Keine                                           |
| Medienbeispielinhalt | Array von Audiostreambytes (keine Systemebene). |



 

## <a name="remarks"></a>Hinweise

Die DirectShow MPEG-1-Filter unterstützen diese Typen wie folgt.



| Filtern               | Richtung | Unterstützte Medientypen                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| MPEG-1-Splitter      | Eingabe     | MPEG-1-SystemstreamMPEG-1-Systemstream aus Video-CD<br/>                                                 |
| MPEG-1-Splitter      | Ausgabe    | MPEG-1-AudiopaketMPEG-1 Audionutzlast<br/> MPEG-1-Videopaket<br/> MPEG-1-Videonutzlast<br/> |
| Softwareaudiocodec | Eingabe     | MPEG-1-AudiopaketMPEG-1 Audionutzlast<br/>                                                                |
| Softwarevideocodec | Eingabe     | MPEG-1-VideopaketMPEG-1 Videonutzlast<br/>                                                                |
| Softwareaudiocodec | Ausgabe    | PCM-Audio                                                                                                         |
| Softwarevideocodec | Ausgabe    | Nicht komprimiertes Video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

MPEG-1 Videopaket- und Nutzlastmedientypen enthalten einen vollständigen Sequenzheader, sodass Daten aus der Mitte einer Datei wiedergegeben werden können, ohne dass ein Sequenzheader zum Initialisieren der Videowiedergabe erforderlich ist.

Der Videosequenzheader wird an den Videodatentyp für MPEG-Videos angefügt, damit die Wiedergabe von der Mitte eines Streams aus beginnen kann. Die Länge dieses Felds beträgt bis zu 140 Bytes. sie enthält den Startcode des Sequenzheaders (0x000001B3) am Anfang sowie alle Quantisierungsmatrizen, die im ersten gefundenen Sequenzheader gefunden wurden.

 

 




