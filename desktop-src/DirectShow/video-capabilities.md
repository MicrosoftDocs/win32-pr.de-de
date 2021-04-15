---
description: Video Funktionen
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Video Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6287839b75bd5044644480c3abcc8248cc46dc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556226"
---
# <a name="video-capabilities"></a>Video Funktionen

Die [**iamstreamconfig:: getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode stellt Videofunktionen in einem Array von Paaren von " [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) " und " [**Video \_ Stream \_ config \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) "-Strukturen dar. Sie können dies verwenden, um alle Formate und Auflösungen verfügbar zu machen, die für eine PIN unterstützt werden, wie unten erläutert.

Audiobezogene Beispiele für **getstreamcaps** finden Sie unter [Audiofunktionen](audio-capabilities.md).

Angenommen, die aufzeichnungskarte unterstützt das JPEG-Format bei allen Auflösungen zwischen 160 x 120 Pixel und 320 x 240 Pixel (einschließlich). Der Unterschied zwischen unterstützten Auflösungen besteht in diesem Fall darin, dass Sie ein Pixel aus jeder unterstützten Auflösung hinzufügen oder subtrahieren, um die nächste unterstützte Auflösung zu erhalten. Dieser Unterschied in unterstützten Auflösungen wird als Granularität bezeichnet.

Angenommen, die Karte unterstützt auch die Größe 640 x 480. Das folgende Beispiel veranschaulicht diese einzelne Auflösung und den oben genannten Bereich von Auflösungen (alle Größen zwischen 160 x 120 Pixel und 320 x 240 Pixel).

![Auflösung zwischen 160 x 120 und 320 x 240 Pixel Plus 640 x 480](images/strmcap1.png)

Außerdem wird angenommen, dass Sie ein 24-Bit-Farb-RGB-Format bei Auflösungen zwischen 160 x 120 und 320 x 240, aber mit einer Granularität von 8 unterstützt. Die folgende Abbildung zeigt einige der gültigen Größen in diesem Fall.

![Auflösung zwischen 160 x 120 und 320 bis 240 mit Granularität = 8](images/strmcap3.png)

Um eine andere Möglichkeit zu finden und weitere Auflösungen aufzulisten, finden Sie die folgenden Informationen in der Liste der gültigen Lösungen.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... Weitere Auflösungen...
-   312 x 232
-   320 x 240

Verwenden Sie **getstreamcaps** , um diese Farb Format-und Dimensions Funktionen verfügbar zu machen, indem Sie den Medientyp 320 x 240 JPEG (wenn dies die standardmäßige oder bevorzugte Größe hat) gekoppelt mit den minimalen Funktionen von 160 x 120, den maximalen Funktionen von 320 x 240 und der Granularität 1 bietet. Das nächste Paar, das Sie mithilfe von **getstreamcaps** verfügbar machen, ist ein Medientyp von 640 x 480 JPEG gekoppelt mit mindestens 640 x 480 und maximal 640 x 480 und einer Granularität von 0. Das dritte Paar umfasst einen Medientyp von 320 x 240, 24-Bit-RGB mit minimalen Funktionen von 160 x 120, maximale Kapazität von 320 x 240 und eine Granularität von 8. Auf diese Weise können Sie nahezu jedes Format und jede Funktion veröffentlichen, die von Ihrer Karte unterstützt werden. Eine Anwendung, die wissen muss, welche Komprimierungs Formate Sie angeben, kann alle Paare erhalten und eine Liste aller eindeutigen Untertypen der Medientypen erstellen.

Ein Filter Ruft die Quell-und Ziel Rechtecke des Medientyps aus den **rcSource** -und **rctarget** -Membern der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur ab. Filter müssen keine Quell-und Ziel Rechtecke unterstützen.

Das Zuschneiderechteck, das in der [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Dokumentation beschrieben wird, ist identisch mit dem **rcSource** -Rechteck der **videinfoheader** -Struktur für die Ausgabepin.

Das in der **iamstreamconfig** -Dokumentation beschriebene Ausgabe Rechteck ist identisch mit den Membern **biwidth** und **biheight** der **BITMAPINFOHEADER** -Struktur der Ausgabe-PIN (siehe [DV-Daten im AVI-Datei Format](dv-data-in-the-avi-file-format.md)).

Wenn die Ausgabepin eines Filters mit einem Medientyp verbunden ist, der nicht leere Quell-und Ziel Rechtecke ist, muss der Filter das Quell subrechteck des Eingabe Formats in das Ziel-unter Rechteck des Ausgabeformats ausdehnen. Das Quell subrechteck wird im **inputsize** -Member der [**\_ videolstream- \_ Konfigurations \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) Ober Struktur gespeichert.

Sehen Sie sich beispielsweise das folgende Video-Kompressor-Szenario an: das Eingabebild hat das RGB-Format und eine Größe von 160 x 120 Pixel. Die linke obere Ecke des Quell Rechtecks liegt bei Koordinate (20, 20), und die untere rechte Ecke liegt bei (30, 30). Das Ausgabe Bild hat das MPEG-Format mit einer Größe von 320 x 240. Die linke obere Ecke des Ziel Rechtecks liegt bei (0,0), und die untere rechte Ecke liegt bei (100.100). In diesem Fall sollte der Filter einen 10 × 10-Bit der 160 x 120 RGB-Quell Bitmap annehmen und den oberen 100 x 100-Bereich einer 320 x 240-Bitmap ausfüllen, sodass der Rest der 320 x 240-Bitmap unverändert bleibt. In der folgenden Abbildung ist dieses Szenario dargestellt.

![unter Rechteck Streckung](images/strmcap4.png)

Ein Filter unterstützt dies möglicherweise nicht, und es kann keine Verbindung mit einem Medientyp hergestellt werden, bei dem **rcSource** und **rctarget** nicht leer sind.

Die **videoinfoheader** -Struktur macht Informationen zu den Datenraten Funktionen eines Filters verfügbar. Angenommen, Sie haben die Ausgabe-PIN mit dem nächsten Filter mit einem bestimmten Medientyp verbunden (entweder direkt oder mithilfe des Medientyps, der von der [**cmediatype:: SetFormat**](cmediatype-setformat.md) -Funktion übergeben wird). Sehen Sie sich den **dwbitrate** -Member der **videoinfoheader** -Format Struktur dieses Medientyps an, um zu sehen, in welcher Datenrate Sie das Video komprimieren sollten. Wenn Sie die Anzahl der Zeiteinheiten pro Frame im **avgtimeperframe** -Member der **videoinfoheader** -Struktur anhand der Datenrate im **dwbitrate** -Element und dividieren durch 10 Millionen (Anzahl der Einheiten pro Sekunde) multiplizieren, können Sie ermitteln, wie viele Bytes jeder Frame sein sollte. Sie können einen Frame mit geringerer Größe, aber nie einen größeren Frame schaffen. Verwenden Sie zum Bestimmen der Framerate für einen Video-Kompressor oder einen Erfassungs Filter **avgtimeperframe** aus dem Medientyp ihrer Ausgabe-PIN.

 

 



