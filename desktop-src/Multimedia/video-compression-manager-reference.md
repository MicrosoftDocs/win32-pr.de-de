---
title: Referenz zum Videokomprimierungs-Manager
description: Referenz zum Videokomprimierungs-Manager
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video für Windows (VFW), Videokomprimierungs-Manager (VCM)
- VFW (Video für Windows),Videokomprimierungs-Manager (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adffe57bd731736ed434dfdfa3c4ded4e643c66a0b5f9ea1c6085a71285e45c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804270"
---
# <a name="video-compression-manager-reference"></a>Referenz zum Videokomprimierungs-Manager

In diesem Abschnitt werden die Funktionen, Strukturen, Meldungen und Makros beschrieben, die VCM zugeordnet sind. Diese Elemente sind wie folgt gruppiert.

## <a name="compressor-installation-and-removal"></a>Installations- und Entfernungsschritte

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Suchen und Öffnen eines 19-

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Auswählen von "Aussteller"

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Konfigurieren von Ausstellern

-   [**\_ICM Konfigurieren**](icm-configure.md)
-   [**\_ICM GETSTATE**](icm-getstate.md)
-   [**\_ICM Setstate**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informationen zum Rauschen

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**\_ICM GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**\_ICM GETDEFAULTQUALITY**](icm-getdefaultquality.md)
-   [**\_ICM Über**](icm-about.md)

## <a name="single-image-compression"></a>Komprimierung einzelner Images

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Sequenzkomprimierung

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Bilddatenkomprimierung

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**\_ICM KOMPRIMIEREN \_ DES \_ GET-FORMATS**](icm-compress-get-format.md)
-   [**\_ICM COMPRESS \_ QUERY**](icm-compress-query.md)
-   [**\_ICM KOMPRIMIEREN DER \_ \_ GET-GRÖßE**](icm-compress-get-size.md)
-   [**\_ICM COMPRESS \_ BEGIN**](icm-compress-begin.md)
-   [**\_ICM COMPRESS \_ END**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Überwachung der Überwachungsdaten

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Dekomprimieren einzelner Images

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Dekomprimieren von Bilddaten

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**\_ICM DECOMPRESSEX \_ END**](icm-decompressex-end.md)
-   [**\_ICM DECOMPRESS \_ GET \_ FORMAT**](icm-decompress-get-format.md)
-   [**\_ICM DECOMPRESS \_ GET \_ PALETTE**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**\_ICM DECOMPRESS \_ BEGIN**](icm-decompress-begin.md)
-   [**\_ICM DECOMPRESS \_ END**](icm-decompress-end.md)
-   [**\_ICM DECOMPRESS \_ QUERY**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Verwenden von Hardware-Drawing Funktionen

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**\_ICM DRAW \_ END**](icm-draw-end.md)
-   [**\_ICM DRAW \_ FLUSH**](icm-draw-flush.md)
-   [**\_ICM DRAW \_ QUERY**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**\_ICM DRAW \_ START**](icm-draw-start.md)
-   [**\_ICM DRAW \_ STOP**](icm-draw-stop.md)
-   [**\_ICM GETBUFFERSWANTED**](icm-getbufferswanted.md)
-   [**\_ICM DRAW \_ REALIZE**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**\_ICM DRAW \_ GETTIME**](icm-draw-gettime.md)
-   [**\_ICM DRAW \_ SETTIME**](icm-draw-settime.md)
-   [**\_ICM ZEICHNEN \_ DES FENSTERS**](icm-draw-window.md)
-   [**\_ICM DRAW \_ REALIZE**](icm-draw-realize.md)
-   [**\_ICM DRAW \_ CHANGEPALETTE**](icm-draw-changepalette.md)
-   [**\_ICM DRAW \_ RENDERBUFFER**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> </dl>

 

 




