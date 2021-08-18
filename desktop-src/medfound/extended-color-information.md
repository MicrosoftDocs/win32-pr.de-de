---
description: Erweiterte Farbinformationen
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Erweiterte Farbinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ffce83acccd2004156d55c0711836271d9ad5cfe7a6ac395e0d9fcbb418142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466370"
---
# <a name="extended-color-information"></a>Erweiterte Farbinformationen

Wenn Sie etwas über RGB-Farbe wissen, wissen Sie, dass (255, 255, 255) das 8-Bit-RGB-Triplet für die Farbe *Weiß ist.* Aber was ist die tatsächliche *Farbe, die* von diesem Triplet definiert wird?

Die Antwort mag überraschend sein: Ohne zusätzliche Informationen definiert dieses Triplet keine bestimmte Farbe! Die Bedeutung eines RGB-Werts hängt vom *Farbraum ab.* Wenn wir den Farbraum nicht kennen, kennen wir streng genommen die Farbe nicht.

Ein Farbraum definiert, wie die numerische Darstellung eines bestimmten Farbwerts als physisches Licht reproduziert werden soll. Wenn Video in einem Farbraum codiert, aber in einem anderen angezeigt wird, führt dies zu verzerrten Farben, es sei denn, das Video wurde farblich korrigiert. Um eine genaue Farbgenauigkeit zu erzielen, ist es daher wichtig, den Farbraum des Quellvideos zu kennen. Zuvor hatte die Videopipeline in Windows keine Informationen über den vorgesehenen Farbraum. Ab Windows Vista unterstützen Sowohl DirectShow als auch Media Foundation erweiterte Farbinformationen im Medientyp. Diese Informationen sind auch für die DirectX-Videobeschleunigung (DXVA) verfügbar.

Die Standardmäßige Möglichkeit, einen Farbraum mathematisch zu beschreiben, ist die Verwendung des CIE XYZ-Farbraums, der von der International Commission on Commission on Commission (CIE) definiert wurde. Es ist nicht praktisch, CIE XYZ-Werte direkt im Video zu verwenden, aber der CIE XYZ-Farbraum kann beim Konvertieren zwischen Farbräumen als Zwischendarstellung verwendet werden.

Um Farben genau zu reproduzieren, sind die folgenden Informationen erforderlich:

-   Farbprimprimries. Die Farbprimries definieren, wie CIE XYZ-Tristimuluswerte als RGB-Komponenten dargestellt werden. Tatsächlich definieren die Farbprim primär die "Bedeutung" eines bestimmten RGB-Werts.
-   Übertragungsfunktion. Die Übertragungsfunktion ist eine Funktion, die lineare RGB-Werte in nicht lineare R'G'B'-Werte konvertiert. Diese Funktion wird auch als *Gammakorrektur bezeichnet.*
-   Übertragungsmatrix. Die Übertragungsmatrix definiert, wie R'G'B' in Y'PbPr konvertiert wird.
-   Sampling von Mustern. Die meisten YUV-Videos werden mit weniger Auflösung in den Komponenten von "Luma" übertragen. Die Stichprobenentnahme wird durch den FOURCC des Videoformats angegeben. Beispielsweise ist YUY2 ein 4:2:2-Format, was bedeutet, dass die Stichprobenentnahmen horizontal um den Faktor 2 durchgeführt werden.
-   Besennung. Wenn die Brille entnommen wird, bestimmt die Position der Musterbeispiele relativ zu den Luma-Stichproben, wie die fehlenden Stichproben interpoliert werden sollen.
-   Nominaler Bereich. Der nominale Bereich definiert, wie Y'PbPr-Werte auf Y'CbCr skaliert werden.

## <a name="color-space-in-media-types"></a>Farbraum in Medientypen

DirectShow, Media Foundation und DirectX Video Acceleration (DXVA) haben unterschiedliche Möglichkeiten, Videoformate zu darstellen. Glücklicherweise ist es einfach, die Farbrauminformationen von einer in eine andere zu übersetzen, da die relevanten Enumerationen identisch sind.

-   DXVA 1.0: Farbrauminformationen werden in der [**DXVA \_ ExtendedFormat-Struktur**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) angegeben.
-   DXVA 2.0: Farbrauminformationen werden in der [**DXVA2 \_ ExtendedFormat-Strukturstruktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) angegeben. Diese Struktur ist mit der DXVA 1.0-Struktur identisch, und die Bedeutung der Felder ist identisch.
-   DirectShow: Farbrauminformationen werden in der [**VIDEOINFOHEADER2-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) angegeben. Die Informationen werden in den oberen 24 Bits des **Felds dwControlFlags** gespeichert. Wenn Farbrauminformationen vorhanden sind, legen Sie das **FLAG AMCONTROL \_ COLORINFO \_ PRESENT** in **dwControlFlags fest.** Wenn dieses Flag festgelegt ist, sollte das **feld dwControlFlags** als [**DXVA \_ ExtendedFormat-Struktur**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) interpretiert werden, mit der Ausnahme, dass die unteren 8 Bits der Struktur für **AMCONTROL \_ xxx-Flags reserviert** sind.
-   Videoaufnahmetreiber: Farbrauminformationen werden in der [**KS \_ VIDEOINFOHEADER2-Struktur**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) angegeben. Diese Struktur ist mit der [**VIDEOINFOHEADER2-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) identisch, und die Bedeutung der Felder ist identisch.
-   Media Foundation: Farbrauminformationen werden als Attribute im Medientyp gespeichert:

    

    | Farbinformationen  | attribute                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Farbprimprimries    | [**MF \_ \_ MT-VIDEO \_ – PRIMÄRER**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Übertragungsfunktion  | [**MF \_ MT \_ \_ TRANSFER-FUNKTION**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Übertragungsmatrix    | [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Subsampling von Subsampling in Einem -Subsampling | [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)<br/> (Angegeben durch den FOURCC, der im ersten **DWORD** der Untertyp-GUID gespeichert wird.)<br/> |
    | Besennung      | [**MF \_ MT VIDEO MOUNT \_ \_ \_ SITING**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Nominaler Bereich      | [**NOMINALER MF \_ \_ \_ MT-VIDEOBEREICH \_**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Farbraumkonvertierung

Für die Konvertierung von einem Y'CbCr-Bereich in einen anderen sind die folgenden Schritte erforderlich.

1.  Inverse Quantisierung: Konvertieren Sie die Y'CbCr-Darstellung unter Verwendung des nominalen Quellbereichs in eine Y'PbPr-Darstellung.
2.  Upsampling: Konvertieren Sie die stichprobenierten Werte in 4:4:4, indem Sie Werte interpolieren.
3.  KONVERTIERUNG VON YUV in RGB: Konvertieren von Y'PbPr in nicht lineares R'G'B' mithilfe der Quellübertragungsmatrix.
4.  Inverse Übertragungsfunktion: Konvertieren Sie nicht lineare R'G'B' in lineares RGB, indem Sie die Umkehrung der Übertragungsfunktion verwenden.
5.  RGB-Farbraumkonvertierung: Verwenden Sie die Farbprimiten, um aus dem RGB-Quellraum in den RGB-Zielraum zu konvertieren.
6.  Übertragungsfunktion: Konvertieren Sie lineares RGB mithilfe der Zielübertragungsfunktion in nicht lineares R'G'B.

7.  KONVERTIERUNG VON RGB in YUV: Konvertieren Sie R'G'B' mithilfe der Zielübertragungsmatrix in Y'PbPr.
8.  Downsampling: Konvertieren Sie 4:4:4 in 4:2:2, 4:2:0 oder 4:1:1, indem Sie die Werte filtern.
9.  Quantisierung: Konvertieren Sie Y'PbPr mithilfe des nominalen Zielbereichs in Y'CbCr.

Die Schritte 1 bis 4 werden im Quellfarbraum und die Schritte 6 bis 9 im Zielfarbraum angezeigt. In der tatsächlichen Implementierung können Zwischenschritte ungefähr und angrenzende Schritte kombiniert werden. Im Allgemeinen besteht ein Vor- und Abkniff zwischen Genauigkeit und Berechnungskosten.

Für die Konvertierung von RT.601 in RT.709 sind beispielsweise die folgenden Phasen erforderlich:

-   Inverse Quantisierung: Y'CbCr(601) to Y'PbPr(601)
-   Upsampling: Y'PbPr(601)
-   YUV to RGB: Y'PbPr(601) to R'G'B'(601)
-   Inverse Übertragungsfunktion: R'G'B'(601) to RGB(601)
-   RGB-Farbraumkonvertierung: RGB(601) in RGB(709)
-   Übertragungsfunktion: RGB(709) nach R'G'B'(709)
-   RGB to YUV: R'G'B'(709) to Y'PbPr(709)
-   Downsampling: Y'PbPr(709)

-   Quantisierung: Y'PbPr(709) bis Y'CbCr(709)

## <a name="using-extended-color-information"></a>Verwenden erweiterter Farbinformationen

Um die Farbtreue in der gesamten Pipeline zu erhalten, müssen Farbrauminformationen an der Quelle oder am Decoder eingeführt und über die Pipeline bis zur Senke übermittelt werden.

### <a name="video-capture-devices"></a>Videoaufnahmegeräte

Die meisten analogen Erfassungsgeräte verwenden beim Erfassen von Videos einen klar definierten Farbraum. Erfassungstreiber sollten ein Format mit einem **KS \_ VIDEOINFOHEADER2-Formatblock** anbieten, der die Farbinformationen enthält. Aus Gründen der Abwärtskompatibilität sollte der Treiber Formate akzeptieren, die keine Farbinformationen enthalten. Dadurch kann der Treiber mit Komponenten arbeiten, die die erweiterten Farbinformationen nicht akzeptieren.

### <a name="file-based-sources"></a>Dateibasierte Quellen

Beim Analysieren einer Videodatei kann die Medienquelle (oder der Parserfilter in DirectShow) möglicherweise einige der Farbinformationen bereitstellen. Beispielsweise kann der DVD-Navigator den Farbraum basierend auf dem DVD-Inhalt bestimmen. Möglicherweise stehen dem Decoder andere Farbinformationen zur Verfügung. Beispielsweise gibt ein elementarer MPEG-2-Videostream die Farbinformationen im Feld für die \_ \_ Sequenzanzeigeerweiterung an. Wenn die Farbinformationen nicht explizit in der Quelle beschrieben werden, können sie implizit durch den Inhaltstyp definiert werden. Beispielsweise verwenden die NTSC- und PAL-Varianten von DV-Videos jeweils unterschiedliche Farbräume. Schließlich kann der Decoder alle Farbinformationen verwenden, die er vom Medientyp der Quelle erhält.

### <a name="other-components"></a>Andere Komponenten

Andere Komponenten müssen möglicherweise die Farbrauminformationen in einem Medientyp verwenden:

-   Softwarefarbraumkonverter sollten bei der Auswahl eines Konvertierungsalgorithmus Farbrauminformationen verwenden.
-   Videomixer, z. B. der EVR-Mixer (Enhanced Video Renderer), sollten die Farbinformationen verwenden, wenn Videostreams aus verschiedenen Inhaltstypen gemischt werden.
-   Mit den DXVA-Videoverarbeitungs-APIs und -DDIs kann der Aufrufer Informationen zum Farbraum angeben. Die GPU sollte diese Informationen verwenden, wenn sie eine hart umkn uhrliche Videomischung ausführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videomedientypen](video-media-types.md)
</dt> <dt>

[DirectX-Videobeschleunigung 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
