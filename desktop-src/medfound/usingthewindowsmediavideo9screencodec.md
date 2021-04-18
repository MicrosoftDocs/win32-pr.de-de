---
description: Verwenden des Windows Media Video 9-Bildschirm Codecs
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Verwenden des Windows Media Video 9-Bildschirm Codecs (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361114"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a>Verwenden des Windows Media Video 9-Bildschirm Codecs (Microsoft Media Foundation)

Der Windows Media Video 9-Bildschirm Codec ist für das Komprimieren von *Anwendungsvideos* optimiert, die aus aufeinander folgenden Bildschirmfotos für die Anzeige eines Computers bestehen. Der Codec nutzt die typische Einfachheit des Bilds (relativ wenige Farben, viele gerade Linien usw.) und eine relative fehlende Bewegung, um ein sehr hohes Komprimierungs Verhältnis zu erzielen. Der Nachteil dieser Optimierung ist, dass Videos, die nicht den erwarteten Merkmalen von Anwendungsvideos entsprechen, möglicherweise nur schwer mit akzeptabler Qualität komprimiert werden.

Der Windows Media Video 9-Bildschirm Encoder wird durch den Klassen Bezeichner CLSID \_ CMSSEncMediaObject2 identifiziert, und der Decoder wird als Klassen Bezeichner CLSID \_ cmssdecmediaobject bezeichnet. Der FourCC-Wert für Medientypen, die diesen Codec verwenden, ist "MSS2".

## <a name="configuring-the-encoder"></a>Konfigurieren des Encoders

Der Encoder des Windows Media Video 9-Bildschirm Codecs wird auf die gleiche Weise konfiguriert wie der Standard Video Decoder.

> [!Note]  
> Der Bildschirm Encoder unterstützt nur One-Pass-Codierung. Sie können die Eigenschaft " [ \_ passesused" für "mfpkey](mfpkey-passesusedproperty.md) " auf 2 festlegen und die Eingaben zweimal ohne Fehler verarbeiten. Dies hat jedoch keinen Vorteil. Dies ist ein bekanntes Problem, das in zukünftigen Versionen möglicherweise korrigiert wird.

 

## <a name="getting-the-best-results"></a>Erzielen der besten Ergebnisse

Wenn Sie feststellen, dass die Qualität, die Sie in Ihrem Bildschirmaufnahme Inhalt wünschen, eine höhere Bitrate erfordert, als Sie für das Liefer Szenario verwenden können, können Sie die folgenden Techniken ausprobieren, um eine höhere Effizienz vom Codec zu erzielen:

-   Verwenden Sie eine kleinere Auflösung für die Bildschirmaufnahme. Die Erfassung einer größeren Bildschirmauflösung als erforderlich kann den Viewer durch die Darstellung unnötiger Informationen verwirren.
-   Verwenden Sie eine langsamere Framerate. Bildschirmaufnahmen können häufig zu sehr niedrigen Frameraten (manchmal nur 4 oder 5 Frames pro Sekunde) wirksam werden.
-   Verwenden Sie weniger Grafiken in der Bildschirmaufnahme. Der Windows Media Video 9-Bildschirm Codec ist so optimiert, dass Windows-primitive und Text mit hoher Qualität codiert werden. In der Regel treten Probleme aufgrund von Bitmapgrafiken auf, die häufig Tausende von einzelnen Farben enthalten. Je weniger Bitmaps bei der Erfassung auf dem Bildschirm angezeigt werden, desto besser sind die Ergebnisse. Wenn Sie keine Grafiken aus der Bildschirmaufnahme ausschließen können, gibt es mehrere Möglichkeiten, die Auswirkungen einer Bitmap auf die Bildqualität zu minimieren:
    -   Verringern Sie die Größe der Grafik.
    -   Reduzieren Sie die Anzahl der einzelnen Grafiken, die gleichzeitig auf dem Bildschirm angezeigt werden.
    -   Reduzieren Sie die Menge der Bewegung der Grafik. Wenn sich die Grafik beispielsweise in einem Fenster befindet, lassen Sie das Fenster so stationär wie möglich.
    -   Bewegen Sie den Mauszeiger nicht über die Grafik, oder ziehen Sie Fenster oder andere Elemente auf die Grafik.

## <a name="decoding"></a>Decodierung

Es gibt keine besonderen Anforderungen für das Decodieren von Bildschirm Erfassungs Videos. Allerdings kann der Bildschirm Aufzeichnungs Decoder den codierten Inhalt ohne die privaten Codec-Daten nicht ordnungsgemäß decodieren, wie bei allen Windows Media Video 9-Codecs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Video Codierung](configuringvideoencoding.md)
</dt> <dt>

[Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md)
</dt> <dt>

[Windows Media Video 9-Bildschirm Encoder](windowsmediavideo9screenencoder.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



