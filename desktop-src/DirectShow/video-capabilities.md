---
description: Videofunktionen
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Videofunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4841f5f33b39adc6bd12775e07085e14886d250cd59c988884ae7ca8a6a21b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290845"
---
# <a name="video-capabilities"></a>Videofunktionen

Die [**IAMStreamConfig::GetStreamCaps-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) stellt Videofunktionen in einem Array von Paaren von [**AM MEDIA \_ \_ TYPE-**](/windows/win32/api/strmif/ns-strmif-am_media_type) und [**VIDEO STREAM \_ \_ CONFIG \_ CAPS-Strukturen**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) dar. Sie können dies verwenden, um alle Formate und Auflösungen verfügbar zu machen, die auf einem Pin unterstützt werden, wie unten beschrieben.

Audiobezogene Beispiele für **GetStreamCaps** finden Sie unter [Audiofunktionen.](audio-capabilities.md)

Angenommen, Ihre Erfassungskarte unterstützt das JPEG-Format in allen Auflösungen zwischen 160 x 120 Pixel und 320 x 240 Pixel (einschließlich). Der Unterschied zwischen unterstützten Auflösungen ist in diesem Fall eine, da Sie jeder unterstützten Auflösung ein Pixel hinzufügen oder subtrahieren, um die nächste unterstützte Auflösung zu erhalten. Dieser Unterschied in den unterstützten Auflösungen wird als Granularität bezeichnet.

Angenommen, Ihre Karte unterstützt auch die Größe 640 x 480. Das folgende Beispiel veranschaulicht diese einzelne Auflösung und den oben genannten Auflösungsbereich (alle Größen zwischen 160 x 120 Pixel und 320 x 240 Pixel).

![Auflösung von 160 x 120 bis 320 x 240 Pixel plus 640 x 480](images/strmcap1.png)

Angenommen, es unterstützt das RGB-Format der 24-Bit-Farbe mit Auflösungen zwischen 160 x 120 und 320 x 240, jedoch mit einer Granularität von 8. Die folgende Abbildung zeigt einige der gültigen Größen in diesem Fall.

![Auflösung von 160 x 120 bis 320 bis 240, mit Granularität = 8](images/strmcap3.png)

Anders ausgedrückt: Die folgenden Lösungen sind in der Liste der gültigen Auflösungen aufgeführt und enthalten weitere Lösungen.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... zusätzliche Lösungen ...
-   312 x 232
-   320 x 240

Verwenden Sie **GetStreamCaps,** um diese Farbformat- und Dimensionsfunktionen verfügbar zu machen, indem Sie einen Medientyp von 320 x 240 JPEG (wenn dies Ihre Standardgröße oder bevorzugte Größe ist) in Kombination mit minimalen Funktionen von 160 x 120, einer maximalen Funktionalität von 320 x 240 und einer Granularität von 1 anbieten. Das nächste Paar, das Sie mit **GetStreamCaps** verfügbar machen, ist ein Medientyp von 640 x 480 JPEG, gekoppelt mit einem Minimum von 640 x 480 und einem Maximum von 640 x 480 und einer Granularität von 0. Das dritte Paar enthält einen Medientyp von 320 x 240, 24-Bit RGB mit minimalen Funktionen von 160 x 120, einer maximalen Funktionalität von 320 x 240 und einer Granularität von 8. Auf diese Weise können Sie fast jedes Format und jede Funktion veröffentlichen, die Ihre Karte möglicherweise unterstützt. Eine Anwendung, die wissen muss, welche Komprimierungsformate Sie bereitstellen, kann alle Paare abrufen und eine Liste aller eindeutigen Untertypen der Medientypen erstellen.

Ein Filter ruft die Quell- und Zielrechtecke des Medientyps aus den **rcSource-** bzw. **rcTarget-Membern** der [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ab. Filter müssen quell- und zielrechteckige Rechtecke nicht unterstützen.

Das in der [**IAMStreamConfig-Dokumentation**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) beschriebene Zuschneiderechteck entspricht dem **rcSource-Rechteck** der **VIDEOINFOHEADER-Struktur** für den Ausgabepin.

Das in der **IAMStreamConfig-Dokumentation** beschriebene Ausgaberechteck entspricht den **Membern biWidth** und **biHeight** der **BITMAPINFOHEADER-Struktur** des Ausgabepins (siehe [DV-Daten im AVI-Dateiformat](dv-data-in-the-avi-file-format.md).).

Wenn der Ausgabepin eines Filters mit einem Medientyp mit nichtmpy Quell- und Zielrechtecken verbunden ist, ist Ihr Filter erforderlich, um das Quellunterrectangle des Eingabeformats in das Zielunterrectangle des Ausgabeformats zu strecken. Das Quellunterrectangle wird im **InputSize-Member** der [**VIDEO STREAM \_ \_ CONFIG \_ CAPS-Struktur**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) gespeichert.

Betrachten Sie beispielsweise das folgende Videoszenario: Das Eingabebild hat das RGB-Format und eine Größe von 160 x 120 Pixel. Die obere linke Ecke des Quellrechtecks befindet sich an der Koordinate (20,20), und die untere rechte Ecke befindet sich bei (30,30). Das Ausgabebild ist im MPEG-Format mit einer Größe von 320 x 240. Die obere linke Ecke des Zielrechtecks befindet sich bei (0,0) und die untere rechte Ecke bei (100.100). In diesem Fall sollte der Filter ein 10 x 10-Teil der 160 x 120 RGB-Quellbitmap annehmen und den oberen 100 x 100-Bereich einer 320 x 240-Bitmap füllen, sodass der Rest der 320 x 240 Bitmap unverändert bleibt. Die folgende Abbildung zeigt dieses Szenario.

![subrectangle stretching](images/strmcap4.png)

Ein Filter unterstützt dies möglicherweise nicht und kann keine Verbindung mit einem Medientyp herstellen, bei dem **rcSource** und **rcTarget** nicht leer sind.

Die **VIDEOINFOHEADER-Struktur** macht Informationen über die Datenratenfunktionen eines Filters verfügbar. Angenommen, Sie haben Ihren Ausgabepin mit dem nächsten Filter mit einem bestimmten Medientyp verbunden (entweder direkt oder mithilfe des Medientyps, der von der [**CMediaType::SetFormat-Funktion**](cmediatype-setformat.md) übergeben wird). Sehen Sie sich den **dwBitRate-Member** der **VIDEOINFOHEADER-Formatstruktur** dieses Medientyps an, um zu sehen, auf welche Datenrate Sie das Video komprimieren sollten. Wenn Sie die Anzahl der Zeiteinheiten pro Frame im **AvgTimePerFrame-Element** der **VIDEOINFOHEADER-Struktur** mit der Datenrate im **dwBitRate-Element** multiplizieren und durch 10.000.000 dividieren (die Anzahl der Einheiten pro Sekunde), können Sie die Anzahl der Bytes pro Frame herausfinden. Sie können einen kleineren Rahmen erstellen, aber nie einen größeren. Verwenden Sie **AvgTimePerFrame** aus dem Medientyp Ihres Ausgabepins, um die Bildfrequenz für eine Videoentität oder einen Erfassungsfilter zu bestimmen.

 

 



