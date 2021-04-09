---
description: H. 264-Video Typen
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: H. 264-Video Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957704"
---
# <a name="h264-video-types"></a>H. 264-Video Typen

Die folgenden Medien Untertypen sind für das H. 264-Video definiert.



| Subtype                | FOURCC | BESCHREIBUNG                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **Mediasubtype \_ AVC1** | 'AVC1' | H. 264-Bitstrom ohne Start Codes.                           |
| **Mediasubtype \_ H264** | H264 | H. 264-Bitstrom mit Start Codes.                              |
| **Mediasubtype \_ H264** | H264 | Äquivalent zu **mediasubtype \_ H264** mit einem anderen FourCC. |
| **Mediasubtype \_ X264** | X264 | Äquivalent zu **mediasubtype \_ H264** mit einem anderen FourCC. |
| **Mediasubtype \_ x264** | x264 | Äquivalent zu **mediasubtype \_ H264** mit einem anderen FourCC. |



 

Diese Untertyp-GUIDs werden in wmcodecdsp. h deklariert.

Der Hauptunterschied zwischen diesen Medientypen besteht darin, dass Start Codes im Bitstream vorhanden sind. Wenn der Untertyp **mediasubtype \_ AVC1** ist, enthält der Bitstrom keine Start Codes.

### <a name="h264-bitstream-with-start-codes"></a>H. 264-Bitstream mit Start Codes

H. 264-Bitstreams, die per Funk übertragen oder in MPEG-2-oder Transportdaten Strömen enthalten oder auf HD-DVD aufgezeichnet werden, werden wie in Anhang B von ITU-T Rec. H. 264 beschrieben formatiert. Gemäß dieser Spezifikation besteht der Bitstrom aus einer Sequenz von Einheiten für die Netzwerk Abstraktionsschicht (nalus), denen jeweils ein Startcode vorangestellt ist, der 0x000001 oder 0x00000001 entspricht.

Wenn im Bitstream Start Codes vorhanden sind, wird der folgende Medientyp verwendet:



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| Haupttyp  | **MediaType- \_ Video**                                                                              |
| Untertypen    | **Mediasubtype \_ H264**, **mediasubtype \_ H264**, **mediasubtype \_ x264** oder **mediasubtype \_ x264** |
| Formattyp | **Format \_ Videoinfo**, **Format \_ VideoInfo2**, **Format \_ MPEG2Video** oder **GUID \_ null**          |



 

Wenn der Formattyp " **GUID \_ null**" ist, ist keine Format Struktur vorhanden.

Wenn der Bitstrom Start Codes enthält, sind die hier aufgeführten Format Typen ausreichend, da der Decoder keine zusätzlichen Informationen zum Analysieren des Streams benötigt. Der Bitstrom enthält bereits alle Informationen, die vom Decoder benötigt werden, und die Start Codes ermöglichen es dem Decoder, den Start der einzelnen Nalu zu finden.

Die folgenden Untertypen sind äquivalent:

### <a name="h264-bitstream-without-start-codes"></a>H. 264-Bitstream ohne Start Codes

Das MP4-Containerformat speichert H. 264-Daten ohne Start Codes. Stattdessen wird jedem Nalu ein Längenfeld vorangestellt, das die Länge der Nalu in Bytes angibt. Die Größe des Längen Felds kann variieren, ist jedoch in der Regel 1, 2 oder 4 Bytes.

Wenn keine Start Codes im Bitstream vorhanden sind, wird der folgende Medientyp verwendet.



|             |                        |
|-------------|------------------------|
| Haupttyp  | **MediaType- \_ Video**   |
| Subtype     | **Mediasubtype \_ AVC1** |
| Formattyp | **MPEG2Video formatieren \_** |



 

Der Format Block ist eine [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur. Diese Struktur sollte wie folgt ausgefüllt werden:

-   **HDR**: eine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur, die den Bitstream beschreibt. Nach dem [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Teil der Struktur ist keine Farbtabelle vorhanden, und **biclrused** muss NULL sein.
-   **dwstarttimecode**: wird nicht verwendet. Auf NULL festlegen.
-   **cbsequenceheader**: die Länge des **dwsequenceheader** -Arrays in Bytes.
-   **dwprofile**: gibt das H. 264-Profil an.
-   **dwlevel**: gibt die H. 264-Ebene an.
-   **dwFlags**: die Anzahl von Bytes, die für das Längenfeld verwendet wird, das vor jedem **Nalu** angezeigt wird. Das Längenfeld gibt die Größe der folgenden Nalu in Bytes an. Wenn **dwFlags** z. b. 4 ist, wird jedem Nalu ein 4-Byte-Längenfeld vorangestellt. Gültige Werte sind 1, 2 und 4.
-   **dwsequenceheader**: ein Bytearray, das Sequence Parameter Set (SPS) und Picture Parameter Set (PPS) nalus enthalten kann.

Der MP4-Container enthält möglicherweise Sequenz Parametersätze (SPS) oder Bildparameter Sätze (PPS) als spezielle nal-Einheiten in Datei Headern oder in einem separaten Stream (unterscheidet sich vom Videostream). Wenn das Format festgelegt wird, kann der Medientyp SPS und PPS-nal-Einheiten im **dwsequenceheader** -Array angeben. Wenn **cbsequenceheader** größer als 0 (null) ist, handelt es sich bei **dwsequenceheader** um den Anfang eines Bytearrays, das SPS und PPS nalus enthält, getrennt durch 2-Byte-Längenfelder (Big-Endian). Es ist möglich, sowohl SPS als auch PPS, nur einen dieser Typen oder None zu haben. Der tatsächliche Typ der einzelnen Nalu kann ermittelt werden, indem das Feld " **nal \_ Unit \_ Type** " des Nalu selbst überprüft wird.

Wenn dieser Medientyp verwendet wird, beginnt jedes Medien Beispiel am Anfang eines Nalu, und NAL-Einheiten umfassen keine Stichproben. Dadurch kann der Decoder nach Daten Beschädigungen oder gelöschten Beispielen wieder hergestellt werden.

 

 



