---
title: Erzielen von guten Ergebnissen mit dem Windows Media Video 9-Bildschirm Codec
description: Erzielen von guten Ergebnissen mit dem Windows Media Video 9-Bildschirm Codec
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media-Format-SDK, Windows Media Video 9-Bildschirm Codec
- Advanced Systems Format (ASF), Windows Media Video 9-Bildschirm Codec
- ASF (Advanced Systems Format), Windows Media Video 9-Bildschirm Codec
- Codecs, Windows Media Video 9-Bildschirm
- Windows Media Video 9-Bildschirm Codec, Ergebnisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948450"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Erzielen von guten Ergebnissen mit dem Windows Media Video 9-Bildschirm Codec

Der Windows Media Video 9-Bildschirm Codec ist darauf ausgelegt, hochkomprimierte Videos für die Bildschirmaufnahme zu erstellen. Da der größte Teil der Bildschirm Erfassung relativ einfache und statische Bilder umfasst, bedeutet die hohe Komprimierungs Ebene in der Regel nicht, dass die Qualität des Images groß ist. Allerdings ist jede Bildschirmaufnahme anders, und die resultierende Bildqualität kann je nach Situation erheblich variieren.

Die beste Möglichkeit, die Profileinstellungen für eine Bildschirm Codec-Sitzung zu ermitteln, besteht darin, eine Testdatei mit einem Qualitäts basierten variablenbitrate-Datenstrom zu codieren. Legen Sie die Qualität auf den gewünschten Wert fest, und codieren Sie eine Bildschirmaufnahme, als wäre Sie die endgültige Datei aufzuzeichnen. Wenn die Datei geschrieben ist, geben Sie Sie mithilfe des asynchronen Reader-Objekts wieder, und führen Sie dabei reguläre Aufrufe von [**iwmreaderadvanced:: getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)aus. Indem Sie den Wert des **dwbandwidth** -Members der [**WM- \_ Reader- \_ Statistik**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) Struktur für jeden-Befehl überwachen, können Sie die ungefähre Bitrate ermitteln, die zum Erreichen der gewünschten Qualität erforderlich ist. Anschließend können Sie diese Bitrate für die Konstante Bitrate-Codierung verwenden.

Wenn Sie feststellen, dass die gewünschte Qualität eine höhere Bitrate erfordert, als Sie für Ihr Bereitstellungs Szenario verwenden können, können Sie die folgenden Techniken ausprobieren, um eine höhere Effizienz vom Codec zu erzielen.

-   Verwenden Sie eine kleinere Auflösung für die Bildschirmaufnahme. Wenn Sie eine größere Bildschirmauflösung erfassen, als Sie benötigen, können Sie auch Verwirrung für den Viewer erzielen, indem Sie mehr Informationen als benötigt darstellen.
-   Verwenden Sie weniger Grafiken in der Bildschirmaufnahme. Der Windows Media Video 9-Bildschirm Codec ist so optimiert, dass Windows-primitive und Text mit hoher Qualität codiert werden. In der Regel treten Probleme aufgrund von Bitmapgrafiken auf, die häufig Tausende von einzelnen Farben enthalten. Je weniger Bitmaps bei der Erfassung auf dem Bildschirm angezeigt werden, desto besser sind die Ergebnisse. Wenn Sie keine Grafiken aus der Bildschirmaufnahme ausschließen können, gibt es mehrere Möglichkeiten, die Auswirkungen einer Bitmap auf die Bildqualität zu minimieren:
    -   Verringern Sie die Größe der Grafik.
    -   Reduzieren Sie die Anzahl der einzelnen Grafiken, die gleichzeitig auf dem Bildschirm angezeigt werden.
    -   Reduzieren Sie die Menge der Bewegung der Grafik. Wenn sich die Grafik beispielsweise in einem Fenster befindet, lassen Sie das Fenster so stationär wie möglich.
    -   Bewegen Sie den Mauszeiger nicht über die Grafik, oder ziehen Sie Fenster oder andere Elemente auf die Grafik.
-   Verwenden Sie eine langsamere [*Framerate*](wmformat-glossary.md). Bildschirmaufnahmen können häufig zu sehr niedrigen Frameraten (manchmal nur 4 oder 5 Frames pro Sekunde) wirksam werden.
-   Reduzieren Sie die Bitrate der zugehörigen Audiodaten.

Außerdem unterstützt der Codec die Größe des Video Rechtecks nicht. Anders ausgedrückt: Wenn Sie versuchen, den Codec zu verwenden, um einen 800 x 600-Bildschirm in ein 640 x 480-Video Rechteck zu codieren, weist das resultierende Video bedeutende Artefakte auf, die möglicherweise einen Großteil des Texts auf dem Bildschirm enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Bildschirm Aufzeichnungsdaten strömen**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




