---
description: In diesem Abschnitt sind die Medientypen aufgeführt, die für MPEG-1-Daten verwendet werden.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: MPEG-1-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354270"
---
# <a name="mpeg-1-media-types"></a>MPEG-1-Medientypen

In diesem Abschnitt sind die Medientypen aufgeführt, die für MPEG-1-Daten verwendet werden.

## <a name="mpeg-1-system-stream"></a>MPEG-1-Systemdatenstrom



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| Haupttyp            | MediaType- \_ Stream                               |
| Subtype               | Mediasubtype \_ MPEG1System                       |
| Formattyp           | Formatieren von \_ mpegstreams                             |
| Format Struktur      | [**AM \_ mpegsystemtype**](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| Medien Beispiel Inhalt | Bytestream; keine Ausrichtung                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a>MPEG-1-System Datenstrom von Video-CD



|                       |                            |
|-----------------------|----------------------------|
| Haupttyp            | MediaType- \_ Stream          |
| Subtype               | Mediasubtype \_ MPEG1VideoCD |
| Formattyp           | GUID \_ null                 |
| Format Struktur      | Keine                       |
| Medien Beispiel Inhalt | Bytestream; keine Ausrichtung. |



 

## <a name="mpeg-1-audio-packet"></a>MPEG-1-audiopaket



|                       |                                                |
|-----------------------|------------------------------------------------|
| Haupttyp            | MediaType \_ -Audiodatei                               |
| Subtype               | Mediasubtype \_ MPEG1Packet                      |
| Formattyp           | Formatieren von \_ WaveFormatEx                           |
| Format Struktur      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| Medien Beispiel Inhalt | Einzelnes MPEG-1-Paket, einschließlich Paket Header. |



 

## <a name="mpeg-1-audio-payload"></a>MPEG-1-audionutzlast



|                       |                                            |
|-----------------------|--------------------------------------------|
| Haupttyp            | MediaType \_ -Audiodatei                           |
| Subtype               | Mediasubtype \_ MPEG1Payload                 |
| Formattyp           | Formatieren von \_ WaveFormatEx                       |
| Format Struktur      | [**MPEG1WAVEFORMAT**](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| Medien Beispiel Inhalt | Byte ausgerichtete MPEG-1-Audiodaten.            |



 

## <a name="mpeg-1-video-packet"></a>MPEG-1-Video Paket



|                       |                                                |
|-----------------------|------------------------------------------------|
| Haupttyp            | MediaType- \_ Video                               |
| Subtype               | Mediasubtype \_ MPEG1Packet                      |
| Formattyp           | Formatieren von \_ MPEGVideo                              |
| Format Struktur      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| Medien Beispiel Inhalt | Einzelnes MPEG-1-Paket, einschließlich Paket Header. |



 

## <a name="mpeg-1-video-payload"></a>MPEG-1-Video Nutzlast



|                       |                                          |
|-----------------------|------------------------------------------|
| Haupttyp            | MediaType- \_ Video                         |
| Subtype               | Mediasubtype \_ MPEG1Payload               |
| Formattyp           | Formatieren von \_ MPEGVideo                        |
| Format Struktur      | [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| Medien Beispiel Inhalt | Byte ausgerichtete MPEG-1-Videodaten.          |



 

## <a name="mpeg-1-native-video-stream"></a>Nativer MPEG-1-Videostream



|                       |                                                |
|-----------------------|------------------------------------------------|
| Haupttyp            | MediaType- \_ Stream                              |
| Subtype               | Mediasubtype \_ MPEG1Video                      |
| Formattyp           | GUID \_ null                                     |
| Format Struktur      | Keine                                           |
| Medien Beispiel Inhalt | Array von Videodaten Strom bytes (keine Systemebene). |



 

## <a name="mpeg-1-native-audio-stream"></a>MPEG-1 nativer Audiodatenstrom



|                       |                                                |
|-----------------------|------------------------------------------------|
| Haupttyp            | MediaType- \_ Stream                              |
| Subtype               | Mediasubtype \_ MPEG1Audio                      |
| Formattyp           | GUID \_ null                                     |
| Format Struktur      | Keine                                           |
| Medien Beispiel Inhalt | Array von Audiodatenstrom-bytes (keine Systemebene). |



 

## <a name="remarks"></a>Bemerkungen

Die DirectShow-MPEG-1-Filter unterstützen diese Typen wie folgt.



| Filter               | Richtung | Unterstützte Medientypen                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| MPEG-1-Splitter      | Eingabe     | MPEG-1-System-streammpeg-1-Systemdaten Strom von Video-CD<br/>                                                 |
| MPEG-1-Splitter      | Ausgabe    | MPEG-1-audiopacketmpeg-1-audionutzlast<br/> MPEG-1-Video Paket<br/> MPEG-1-Video Nutzlast<br/> |
| Software-Audiocodec | Eingabe     | MPEG-1-audiopacketmpeg-1-audionutzlast<br/>                                                                |
| Software Videocodec | Eingabe     | MPEG-1 Video packetmpeg-1 Video Nutzlast<br/>                                                                |
| Software-Audiocodec | Ausgabe    | PCM-Audiodatei                                                                                                         |
| Software Videocodec | Ausgabe    | Unkomprimiertes Video (im y41p, im YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)                                    |



 

MPEG-1 Video Packet-und Payload-Medientypen enthalten einen Complete Sequence-Header, damit Daten von der Mitte einer Datei wiedergegeben werden können, ohne dass ein Sequenz Header erforderlich ist, um die Video Wiedergabe zu initialisieren.

Der Videosequenz Header wird an den Video Datentyp für MPEG-Video angehängt, sodass die Wiedergabe von der Mitte eines Streams beginnen kann. Die Länge dieses Felds beträgt 140 bytes. Sie enthält den Sequenz Header-Startcode (0x000001b3) am Anfang, zusammen mit allen quantifisierungsmatrizen, die im ersten gefundenen Sequenz Header gefunden wurden.

 

 




