---
title: Referenz zum Video Komprimierungs-Manager
description: Referenz zum Video Komprimierungs-Manager
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video für Windows (Vfw), Video Komprimierungs-Manager (VCM)
- VFW (Video für Windows), Video Komprimierungs-Manager (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206451"
---
# <a name="video-compression-manager-reference"></a>Referenz zum Video Komprimierungs-Manager

In diesem Abschnitt werden die Funktionen, Strukturen, Meldungen und Makros beschrieben, die mit VCM verknüpft sind. Diese Elemente werden wie folgt gruppiert.

## <a name="compressor-installation-and-removal"></a>Installation und Entfernung von Kompressors

-   [**Icinstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**Iclocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**Icopen**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**Icclose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**Ikremove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**Icopenfunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Suchen und Öffnen eines Kompressors

-   [**Iclocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**Icopen**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**Icdebug**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**Icdrawopen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**Icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**Icclose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Auswählen von Kompressoren

-   [**Iccompressorchoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**Iccompressorfree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**Compvaren**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Konfigurieren von Kompressoren

-   [**ICM- \_ Konfiguration**](icm-configure.md)
-   [**ICM \_ GetState**](icm-getstate.md)
-   [**ICM \_ SetState**](icm-setstate.md)
-   [**Icsendmessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informationen zum Kompressor

-   [**Icgetinfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**Icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICM \_ getdefaultkeyframerate**](icm-getdefaultkeyframerate.md)
-   [**Icgetdisplayformat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**ICM \_ getdefaultquality**](icm-getdefaultquality.md)
-   [**ICM \_ Info**](icm-about.md)

## <a name="single-image-compression"></a>Komprimierung mit einem Bild

-   [**Icimagecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Sequenz Komprimierung

-   [**Icabqcompressframe**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**Icabqcompressframestart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**Icabqcompressframeend**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>Compvaren

-   [**Iccompressorchoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Bild Datenkomprimierung

-   [**Iccompress**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**ICM \_ - \_ komprimierungsget- \_ Format**](icm-compress-get-format.md)
-   [**ICM- \_ Komprimierungs \_ Abfrage**](icm-compress-query.md)
-   [**ICM- \_ Komprimierung \_ get \_ size**](icm-compress-get-size.md)
-   [**ICM- \_ Komprimierung \_ starten**](icm-compress-begin.md)
-   [**ICM- \_ Komprimierung \_ Beenden**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Überwachung des Kompressors

-   [**Icsetstatusproc**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Komprimieren von einzelnen Bildern

-   [**Icimagedebug**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Abbild Daten werden komprimiert.

-   [**ICDE CompressEx**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDE compressexbegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**ICM- \_ \_ decoderende**](icm-decompressex-end.md)
-   [**ICM \_ Decompress \_ get- \_ Format**](icm-decompress-get-format.md)
-   [**ICM- \_ aufgeschbe \_ get- \_ Palette**](icm-decompress-get-palette.md)
-   [**Icabcompressexquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**Icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**ICM-Start \_ \_ Anfang**](icm-decompress-begin.md)
-   [**ICM-Debug- \_ \_ Ende**](icm-decompress-end.md)
-   [**ICM-Abfrage "Debug" \_ \_**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Verwenden von Hardware-Drawing Funktionen

-   [**Icgetinfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**Icdrawbegin**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**ICM- \_ Zeichnungs \_ Ende**](icm-draw-end.md)
-   [**ICM-Zeichnungs Leerung \_ \_**](icm-draw-flush.md)
-   [**ICM- \_ Draw- \_ Abfrage**](icm-draw-query.md)
-   [**Icdrawvorschlags Format**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**ICM- \_ Zeichnen \_ starten**](icm-draw-start.md)
-   [**ICM- \_ Zeichnungs \_ Ende**](icm-draw-stop.md)
-   [**ICM \_ getbufferswanted**](icm-getbufferswanted.md)
-   [**ICM- \_ Zeichnen \_**](icm-draw-realize.md)
-   [**Icdrawopen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**Icdraw**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**ICM \_ Zeichnen \_ GetTime**](icm-draw-gettime.md)
-   [**ICM \_ Draw \_ setTime**](icm-draw-settime.md)
-   [**ICM- \_ Zeichnungs \_ Fenster**](icm-draw-window.md)
-   [**ICM- \_ Zeichnen \_**](icm-draw-realize.md)
-   [**ICM \_ Zeichnen von \_ changepalette**](icm-draw-changepalette.md)
-   [**ICM \_ Draw \_ renderbuffer**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> </dl>

 

 




