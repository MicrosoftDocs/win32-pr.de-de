---
description: Erweiterte Farbinformationen
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Erweiterte Farbinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ba43180a0f1e5253540088c1638f59d52380c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749241"
---
# <a name="extended-color-information"></a>Erweiterte Farbinformationen

Wenn Sie mit der RGB-Farbe vertraut sind, wissen Sie, dass (255, 255, 255) der 8-Bit-RGB-Wert für die Farbe *weiß* ist. Aber wie ist die tatsächliche *Farbe* , die von diesem Dreieck definiert wird?

Die Antwort ist möglicherweise überraschend: ohne zusätzliche Informationen definiert dieses Dreieck keine bestimmte Farbe. Die Bedeutung von RGB-Werten hängt vom *Farbraum* ab. Wenn der Farbraum nicht bekannt ist, wissen wir genau, dass die Farbe nicht bekannt ist.

Ein Farbraum definiert, wie die numerische Darstellung eines angegebenen Farbwerts als physisches Licht reproduziert werden soll. Wenn Videos in einem Farbraum codiert, aber in einem anderen angezeigt werden, führt dies zu verzerrten Farben, es sei denn, das Video wird farblich korrigiert. Um eine exakte Farb Treue zu erzielen, ist es wichtig, den Farbraum des Quellvideos zu kennen. Bisher enthielt die Video Pipeline in Windows keine Informationen über den vorgesehenen Farbraum. Ab Windows Vista unterstützen sowohl DirectShow als auch Media Foundation erweiterte Farbinformationen im Medientyp. Diese Informationen sind auch für die DirectX-Video Beschleunigung (DXVA) verfügbar.

Der standardmäßige Weg, einen Farbraum zu beschreiben, besteht darin, den von der International Commission on Illumination (CIE) definierten Cie XYZ-Farbraum zu verwenden. Die Verwendung von Cie XYZ-Werten in Videos ist nicht praktikabel, aber der Cie XYZ-Farbraum kann als zwischen Darstellung bei der Umstellung zwischen Farbräumen verwendet werden.

Zum exakten reproduzieren von Farben sind folgende Informationen erforderlich:

-   Farb Replikate. Die Farb-Primärwerte definieren, wie die Werte von Cie XYZ-drei Werten als RGB-Komponenten dargestellt werden. Tatsächlich definieren die Farb Replikate die Bedeutung von einem gegebenen RGB-Wert.
-   Übertragungsfunktion. Bei der Übertragungsfunktion handelt es sich um eine Funktion, mit der lineare RGB-Werte in nichtlineare RAS B-Werte konvertiert werden. Diese Funktion wird auch als *Gammakorrektur* bezeichnet.
-   Matrix übertragen. Die Übertragungs Matrix definiert, wie r' g ' B ' in ' pbpr ' konvertiert wird.
-   Chroma-Stichprobenentnahme. Das größte YUV-Video wird mit weniger Auflösung in den Chroma-Komponenten als der "Luma" übertragen. Die Chroma-Stichprobenentnahme wird durch den fourcc des Video Formats angegeben. Beispielsweise ist im YUY2 ein 4:2:2-Format, d. h., die Chroma-Beispiele werden horizontal mit dem Faktor 2 entnommen.
-   Chroma-siting. Wenn der Chroma-Stichprobe Wert ist, bestimmt die Position der Chroma-Beispiele in Relation zu den Luma-Beispielen, wie die fehlenden Stichproben interpoliert werden sollen.
-   Der nominale Bereich. Der nominale Bereich definiert, wie ' pbpr '-Werte auf ' y' CbCr skaliert werden.

## <a name="color-space-in-media-types"></a>Farbraum in Medientypen

DirectShow-, Media Foundation-und DirectX-Videobeschleunigung (DXVA) haben unterschiedliche Möglichkeiten zum Darstellen von Videoformaten. Glücklicherweise ist es einfach, die Farb Rauminformationen von einem in einen anderen zu übersetzen, da die relevanten Enumerationen identisch sind.

-   DXVA 1,0: in der DXVA-Struktur " [**\_ extendedformat**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) " werden Farb Rauminformationen angegeben.
-   DXVA 2,0: die Farbraum-Informationen werden in der [**DXVA2 \_ extendedformat**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) -Struktur Struktur angegeben. Diese Struktur ist identisch mit der DXVA 1,0-Struktur, und die Bedeutung der Felder ist identisch.
-   DirectShow: Farb Rauminformationen werden in der [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur angegeben. Die Informationen werden in den oberen 24 Bits des Felds " **dwcontrolflags** " gespeichert. Wenn Farb Rauminformationen vorhanden sind, legen Sie das " **amcontrol \_ colorinfo \_ Present** "-Flag in " **dwcontrolflags**" fest. Wenn dieses Flag festgelegt ist, sollte das Feld **dwcontrolflags** als [**DXVA \_ extendedformat**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) -Struktur interpretiert werden, mit dem Unterschied, dass die unteren 8 Bits der Struktur für **amcontrol \_ xxx** -Flags reserviert sind.
-   Video Erfassungs Treiber: in der Struktur der Struktur " [**\_ VIDEOINFOHEADER2**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) " werden Farb Rauminformationen angegeben. Diese Struktur ist identisch mit der [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur, und die Bedeutung der Felder ist identisch.
-   Media Foundation: Farb Rauminformationen werden als Attribute im Medientyp gespeichert:

    

    | Farbinformationen  | Attribut                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Farb-Primärwerte    | [**MF- \_ MT- \_ Video- \_ primär**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Übertragungsfunktion  | [**MF- \_ MT- \_ Übertragungs \_ Funktion**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Übertragungs Matrix    | [**MF \_ MT \_ YUV \_ Matrix**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Chroma-Unterstichprobe | [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)<br/> (Angegeben durch den FourCC, der im ersten **DWORD** -Wert der Untertyp-GUID gespeichert ist.)<br/> |
    | Chroma-Positionierung      | [**MF- \_ MT- \_ Video- \_ Chroma- \_ siting**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Nominaler Bereich      | [**\_ \_ \_ nominaler Bereich von MF MT-Video \_**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Farb Raum Konvertierung

Die Konvertierung von einem ' CbCr '-Raum in einen anderen erfordert die folgenden Schritte.

1.  Umgekehrte Quantisierung: konvertieren Sie die ' y' CbCr-Darstellung in eine ' ' ' pbpr '-Darstellung, indem Sie den Quell nominalen Bereich verwenden.
2.  Upsampling: Konvertieren der erfassten Chroma-Werte in 4:4:4 durch Interpolation von Chroma-Werten.
3.  YUV-zu-RGB-Konvertierung: Konvertieren von "y' pbpr" in "nonlineare r' g' B '" mithilfe der Quell Übertragungs Matrix.
4.  Umgekehrte Übertragungsfunktion: konvertiert die nichtlineare r' g' B ' mit der Umkehrung der Übertragungsfunktion in lineare RGB.
5.  RGB-Farb Raum Konvertierung: Verwenden Sie die Farb-primär Zeichen, um den RGB-Quell Raum in den RGB-Zielbereich zu konvertieren.
6.  Übertragungsfunktion: Konvertieren von Linear RGB in nichtlineare RG ' g' B ' mithilfe der Ziel Übertragungsfunktion.

7.  Konvertierung von RGB in YUV: Konvertieren von r' g' B ' in ' pbpr ' mithilfe der Ziel Übertragungs Matrix.
8.  Downsampling: konvertieren Sie 4:4:4 in 4:2:2, 4:2:0 oder 4:1:1, indem Sie die Chroma-Werte filtern.
9.  Quantisierung: Konvertieren von "y' pbpr" in "y' CbCr" mit dem nominalen Zielbereich.

Die Schritte 1 – 4 treten im Quell Farbraum auf, und die Schritte 6 – 9 erfolgen im Ziel Farbraum. In der eigentlichen Implementierung können Zwischenschritte angeglichen und angrenzende Schritte kombiniert werden. Im Allgemeinen gibt es einen Kompromiss zwischen Genauigkeits-und berechnungskosten.

Zum Konvertieren von RT. 601 in RT. 709 sind z. b. die folgenden Phasen erforderlich:

-   Inverse Quantisierung: y' CbCr (601) to y' pbpr (601)
-   Upsampling: y' pbpr (601)
-   YUV zu RGB: "pbpr (601)" in "g ' B ' (601)
-   Umgekehrte Übertragungsfunktion: r' B ' (601) zu RGB (601)
-   RGB-Farb Raum Konvertierung: RGB (601) nach RGB (709)
-   Übertragungsfunktion: RGB (709) an r' B ' (709)
-   RGB zu YUV: r' B ' (709) in ' pbpr (709) '
-   Downsampling: y' pbpr (709)

-   Quantisierung: ' pbpr (709) ' in ' y' CbCr (709)

## <a name="using-extended-color-information"></a>Verwenden von erweiterten Farbinformationen

Um die Farbtreue in der Pipeline beizubehalten, müssen die Farbraum-Informationen in der Quelle oder im Decoder eingefügt und alle über die Pipeline an die Senke übermittelt werden.

### <a name="video-capture-devices"></a>Video Erfassungsgeräte

Die meisten analogen Erfassungsgeräte verwenden beim Aufzeichnen von Videos einen klar definierten Farbraum. Erfassungs Treiber sollten ein Format mit einem **\_ VIDEOINFOHEADER2** -Format Block bieten, der die Farbinformationen enthält. Aus Gründen der Abwärtskompatibilität sollte der Treiber Formate akzeptieren, die die Farbinformationen nicht enthalten. Dadurch kann der Treiber mit Komponenten arbeiten, die die erweiterten Farbinformationen nicht akzeptieren.

### <a name="file-based-sources"></a>Dateibasierte Quellen

Beim Parsen einer Videodatei kann die Medienquelle (oder der Parserfilter in DirectShow) möglicherweise einige der Farbinformationen bereitstellen. Beispielsweise kann der DVD-Navigator den Farb Raum basierend auf dem DVD-Inhalt bestimmen. Weitere Farbinformationen sind möglicherweise für den Decoder verfügbar. Beispielsweise gibt ein MPEG-2-Videodaten Strom die Farbinformationen im Feld Sequenz \_ Anzeige \_ Erweiterung. Wenn die Farbinformationen nicht explizit in der Quelle beschrieben werden, kann Sie implizit vom Inhaltstyp definiert werden. Beispielsweise verwenden die NTSC-und PAL-Varianten des DV-Videos jeweils unterschiedliche Farbraum. Schließlich kann der Decoder alle Farbinformationen verwenden, die er aus dem Medientyp der Quelle abruft.

### <a name="other-components"></a>Andere Komponenten

Andere Komponenten müssen möglicherweise die Farb Rauminformationen in einem Medientyp verwenden:

-   Bei der Auswahl eines Konvertierungs Algorithmus sollten bei der Auswahl von Farb Raum Konvertern Farb Rauminformationen verwendet werden.
-   Video-Mixer, wie z. b. der "Enhanced Video Renderer" (EVR), sollten die Farbinformationen beim Mischen von Videostreams aus verschiedenen Inhaltstypen verwenden.
-   Die DXVA-Videoverarbeitungs-APIs und DDIs ermöglichen dem Aufrufer das Angeben von Informationen über den Farbraum. Die GPU sollte diese Informationen verwenden, wenn Sie eine Video Mischung mit hardward ausführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
