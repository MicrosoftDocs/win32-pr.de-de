---
title: Getting Good Results with the Windows Media Video 9 Screen Codec
description: Getting Good Results with the Windows Media Video 9 Screen Codec
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media Format SDK,Windows Media Video 9 Screen-Codec
- Advanced Systems Format (ASF), Windows Media Video 9 Screen-Codec
- ASF (Advanced Systems Format), Windows Media Video 9 Screen-Codec
- codecs,Windows Media Video 9 Screen
- Windows Media Video 9-Bildschirmcodec,Ergebnisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657cde745f6bfbabe00fe123b493e2eae2afb20ddf40206f781822770a4386f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110430"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Getting Good Results with the Windows Media Video 9 Screen Codec

Der Windows Media Video 9 Screen-Codec ist für die Erstellung stark komprimierter Videos für die Bildschirmaufnahme konzipiert. Da der größte Teil der Notwendigkeit der Bildschirmaufnahme recht einfache und statische Bilder umfasst, bedeuten die hohen Komprimierungsgrade in der Regel keine große Komprimierungsqualität. Allerdings ist jede Bildschirmaufnahme unterschiedlich, und die resultierende Bildqualität kann je nach Den jeweiligen Umständen erheblich variieren.

Die beste Möglichkeit, die Profileinstellungen für eine Bildschirmcodecsitzung zu bestimmen, besteht in der Codierung einer Testdatei mithilfe eines qualitätsbasierten Streams mit variabler Bitrate. Legen Sie die Qualität auf den gewünschten Wert fest, und codieren Sie eine Bildschirmaufnahme so, als ob Sie die endgültige Datei aufzeichnen würden. Wenn die Datei geschrieben wird, geben Sie sie mithilfe des asynchronen Readerobjekts wieder, indem Sie reguläre Aufrufe von [**IWMReaderAdvanced::GetStatistics ausführen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) Indem Sie den Wert des **dwBandwidth-Mitglieds** der [**WM READER \_ \_ STATISTICS-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) für jeden Aufruf überwachen, können Sie die ungefähre Bitrate bestimmen, die erforderlich ist, um die gewünschte Qualität zu erreichen. Sie können diese Bitrate dann für die Codierung mit konstanter Bitrate verwenden.

Wenn Sie feststellen, dass die von Ihnen wünschen Qualität eine höhere Bitrate erfordert, als Sie für Ihr Übermittlungsszenario verwenden können, können Sie die folgenden Techniken ausprobieren, um eine höhere Effizienz des Codecs zu erzielen.

-   Verwenden Sie eine kleinere Auflösung für die Bildschirmaufnahme. Das Erfassen einer größeren Bildschirmauflösung, als Sie benötigen, kann auch verwirrung für den Viewer erzeugen, indem mehr Informationen angezeigt werden, als benötigt werden.
-   Verwenden Sie weniger Grafiken in der Bildschirmaufnahme. Der Windows Media Video 9 Screen-Codec ist für die Codierung Windows Primitiven und Text mit hoher Qualität optimiert. Normalerweise treten Probleme aufgrund von Bitmapgrafiken auf, die häufig Tausende einzelner Farben enthalten. Desto weniger Bitmaps, die beim Erfassen auf dem Bildschirm angezeigt werden, desto besser sind Ihre Ergebnisse. Wenn Sie Grafiken nicht aus der Bildschirmaufnahme eliminieren können, gibt es mehrere Möglichkeiten, die Auswirkungen einer Bitmap auf die Bildqualität zu minimieren:
    -   Reduzieren Sie die Größe der Grafik.
    -   Reduzieren Sie die Anzahl einzelner Grafiken, die gleichzeitig auf dem Bildschirm angezeigt werden.
    -   Reduzieren Sie die Bewegung der Grafik. Wenn sich die Grafik z. B. in einem Fenster befindet, halten Sie das Fenster so still wie möglich.
    -   Vermeiden Sie es, den Mauszeiger über die Grafik zu bewegen oder Fenster oder andere Elemente über die Grafik zu ziehen.
-   Verwenden Sie eine [*langsamere Bildfrequenz.*](wmformat-glossary.md) Bildschirmaufnahme können häufig bei sehr niedrigen Bildraten (manchmal bis zu 4 oder 5 Frames pro Sekunde) effektiv sein.
-   Reduzieren Sie die Bitrate der zugehörigen Audiodaten.

Außerdem unterstützt der Codec keine Größenver ändern des Videorechtecks. Anders ausgedrückt: Wenn Sie versuchen, den Codec zu verwenden, um einen 800 x 600-Bildschirm in ein 640 x 480-Videorechteck zu codieren, enthält das resultierende Video wichtige Artefakte, die einen Großen Teil des Texts auf dem Bildschirm unlesbar machen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Bildschirmaufnahme-Streams**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Konfigurieren Streams**](configuring-streams.md)
</dt> </dl>

 

 




