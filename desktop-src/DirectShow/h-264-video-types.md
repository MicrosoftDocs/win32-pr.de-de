---
description: H.264-Videotypen
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: H.264-Videotypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973df2825b0824256e2eb7a1a7f580c5f13bf5cdbb390602175e1319305756b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102762"
---
# <a name="h264-video-types"></a>H.264-Videotypen

Die folgenden Medienuntertypen sind für H.264-Video definiert.



| Subtype                | FOURCC | BESCHREIBUNG                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **MEDIASUBTYPE \_ AVC1** | "AVC1" | H.264-Bitstream ohne Startcodes.                           |
| **MEDIASUBTYPE \_ H264** | 'H264' | H.264-Bitstream mit Startcodes.                              |
| **MEDIASUBTYPE \_ h264** | 'h264' | Entspricht **MEDIASUBTYPE \_ H264** mit einem anderen FOURCC. |
| **MEDIASUBTYPE \_ X264** | 'X264' | Entspricht **MEDIASUBTYPE \_ H264** mit einem anderen FOURCC. |
| **MEDIASUBTYPE \_ x264** | 'x264' | Entspricht **MEDIASUBTYPE \_ H264** mit einem anderen FOURCC. |



 

Diese Untertyp-GUIDs werden in wmcodecdsp.h deklariert.

Der Hauptunterschied zwischen diesen Medientypen ist das Vorhandensein von Startcodes im Bitstream. Wenn der Untertyp **MEDIASUBTYPE \_ AVC1** ist, enthält der Bitstream keine Startcodes.

### <a name="h264-bitstream-with-start-codes"></a>H.264 Bitstream mit Startcodes

H.264-Bitstreams, die über die Luft übertragen oder in MPEG-2-Programm- oder Transportstreams enthalten oder auf HD-DVD aufgezeichnet werden, werden wie in Anhang B von ITU-T Rec. H.264 beschrieben formatiert. Gemäß dieser Spezifikation besteht der Bitstream aus einer Sequenz von Netzwerkabstraktionsschichteinheiten (Network Abstraction Layer Units, NALUs), denen jeweils ein Startcode vorangestellt ist, der 0x000001 oder 0x00000001 entspricht.

Wenn Startcodes im Bitstream vorhanden sind, wird der folgende Medientyp verwendet:



| Bezeichnung | Wert |
|-------------|---------------------------------------------------------------------------------------------------|
| Haupttyp  | **\_MEDIATYPE-Video**                                                                              |
| Untertypen    | **MEDIASUBTYPE \_ H264,** **MEDIASUBTYPE \_ h264,** **MEDIASUBTYPE \_ X264** oder **MEDIASUBTYPE \_ x264** |
| Formattyp | **FORMATIEREN \_ VideoInfo,** **FORMAT \_ VideoInfo2,** **FORMAT \_ MPEG2Video** oder **GUID \_ NULL**          |



 

Wenn der Formattyp **GUID \_ NULL** ist, ist keine Formatstruktur vorhanden.

Wenn der Bitstream Startcodes enthält, ist jeder der hier aufgeführten Formattypen ausreichend, da der Decoder keine zusätzlichen Informationen zum Analysieren des Streams benötigt. Der Bitstream enthält bereits alle vom Decoder benötigten Informationen, und die Startcodes ermöglichen es dem Decoder, den Anfang jeder NALU zu finden.

Die folgenden Untertypen sind gleichwertig:

### <a name="h264-bitstream-without-start-codes"></a>H.264 Bitstream ohne Startcodes

Im MP4-Containerformat werden H.264-Daten ohne Startcodes gespeichert. Stattdessen wird jeder NALU ein Längenfeld vorangestellt, das die Länge der NALU in Bytes angibt. Die Größe des Längenfelds kann variieren, beträgt aber in der Regel 1, 2 oder 4 Bytes.

Wenn Startcodes nicht im Bitstream vorhanden sind, wird der folgende Medientyp verwendet.



| Bezeichnung | Wert |
|-------------|------------------------|
| Haupttyp  | **\_MEDIATYPE-Video**   |
| Subtype     | **MEDIASUBTYPE \_ AVC1** |
| Formattyp | **FORMAT \_ MPEG2Video** |



 

Der Formatblock ist eine [**MPEG2VIDEOINFO-Struktur.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) Diese Struktur sollte wie folgt ausgefüllt werden:

-   **hdr:** Eine [**VIDEOINFOHEADER2-Struktur,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) die den Bitstream beschreibt. Nach dem [**BITMAPINFOHEADER-Teil**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) der Struktur ist keine Farbtabelle vorhanden, und **biClrUsed** muss 0 (null) sein.
-   **dwStartTimeCode:** Nicht verwendet. Auf NULL festlegen.
-   **cbSequenceHeader:** Die Länge des **dwSequenceHeader-Arrays** in Bytes.
-   **dwProfile:** Gibt das H.264-Profil an.
-   **dwLevel:** Gibt die H.264-Ebene an.
-   **dwFlags:** Die Anzahl der Bytes, die für das Längenfeld verwendet werden, das vor jeder **NALU** angezeigt wird. Das Feld length gibt die Größe der folgenden NALU in Bytes an. Wenn **dwFlags** beispielsweise 4 ist, wird jeder NALU ein Feld mit einer Länge von 4 Byte vorangestellt. Die gültigen Werte sind 1, 2 und 4.
-   **dwSequenceHeader:** Ein Bytearray, das NALUs von Sequence Parameter Set (SPS) und Picture Parameter Set (PPS) enthalten kann.

Der MP4-Container kann Sequenzparametersätze (Sequence Parameter Sets, SPS) oder Bildparametersätze (Picture Parameter Sets, PPS) als spezielle NAL-Einheiten in Dateiheadern oder in einem separaten Stream (getrennt vom Videostream) enthalten. Wenn das Format festgelegt ist, kann der Medientyp SPS- und PPS-NAL-Einheiten im **dwSequenceHeader-Array** angeben. Wenn **cbSequenceHeader** größer als 0 (null) ist, ist **dwSequenceHeader** der Anfang eines Bytearrays mit SPS- und PPS-NALUs, getrennt durch Felder mit einer Länge von 2 Byte, alle in Netzwerk-Bytereihenfolge (Big-Endian). Es ist möglich, sowohl SPS als auch PPS zu verwenden, nur einen dieser Typen oder keinen. Der tatsächliche Typ jeder NALU kann durch Untersuchen des Felds des **\_ nalen \_ Einheitentyps** der NALU selbst bestimmt werden.

Wenn dieser Medientyp verwendet wird, beginnt jedes Medienbeispiel am Anfang einer NALU, und NAL-Einheiten umfassen keine Stichproben. Dadurch kann der Decoder nach Datenbeschädigung oder gelöschten Stichproben wiederhergestellt werden.

 

 



