---
description: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482270"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien

Beim Erstellen von Windows Media – basierten Inhalten verwenden Anwendungen in der Regel eines der folgenden Szenarien:

-   Umwandeln oder transcodieren von Inhalten aus einem anderen Format in das Windows Media-Format.
-   Einfügen von Inhalten, bei denen es sich nicht um Windows Media-basierte (Native Streamformate) handelt, in ASF-Dateien
-   Die Erfassung von Livedaten und die direkte Codierung im Windows Media-Format.

Transcodierung von ASF-Dateien

Sie können ein Datei-transcodierungsfilterdiagramm mit dem [WM-ASF-Writer](wm-asf-writer-filter.md) auf verschiedene Weise erstellen. Die einfachste Möglichkeit besteht darin, den WM-ASF-Writer dem Filter Diagramm hinzuzufügen und dann mit der igraphbuilder:: RenderFile-Methode automatisch das Diagramm zu erstellen.

Eine alternative Möglichkeit besteht darin, jeden Filter manuell dem Diagramm hinzuzufügen und die Pins zu verbinden. Nachdem Sie den WM-ASF-Writer hinzugefügt haben, konfigurieren Sie ihn mithilfe der iconfigasfwriter-Methoden, wenn das Standardprofil nicht geeignet ist, und verbinden Sie die WM-ASF-Eingabe Pins mit den entsprechenden Ausgabe Pins in den upstreamfiltern.

Die folgende Abbildung zeigt die typischen Konfigurationen von "WM-ASF-Writer-Transcodierungs Filter"

![Transcodierungs Filter Diagramm](images/asf-transcode.png)

Einfügen von nativen streamformaten in ASF-Dateien

Standardmäßig erwartet der WM-ASF-Writer-Filter unkomprimierte Audiodaten und Videostreams auf den Eingabe Pins und verwendet die Windows Media Audio und Windows Media Video Codecs, um die Streams zu komprimieren. Allerdings kann der ASF-Datei Container für beliebige Datentypen verwendet werden. Durch das Platzieren digitaler Mediendaten in einem ASF-Datei Container können Sie Features hinzufügen, die von ASF bereitgestellt werden, wie z. b. Metadaten und Digital Rights Management (DRM), ohne dass Sie Ihre Inhalte transcodieren müssen.

Zum Erstellen einer ASF-Datei, die Inhalte enthält, die nicht auf Windows Media – basieren, muss die Anwendung den Datenstrom im Filter Diagramm Upstream des WM-ASF-Writers komprimieren und den Komprimierungs Mechanismus des WM-ASF-Writers durch Aufrufen von [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) wie folgt umgehen:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Konfigurieren Sie dann den Filter mit dem gewünschten Profil. Es ist von entscheidender Bedeutung, dass der Medientyp des Eingabestreams genau mit dem Format im Profil übereinstimmt. In einigen Fällen kann es erforderlich sein, das Format des Eingabestreams zu untersuchen und ein benutzerdefiniertes Profil zu erstellen, um es abzugleichen.

Wenn Sie den WM-ASF-Writer mit dem upstreamfilter verbinden, verwenden Sie die igraphbuilder:: connectdirect-Methode. Verwenden Sie keine "Intelligent Connect"-Methoden wie z. b. igraphbuilder:: Connect oder igraphbuilder:: RenderFile, um den Filter zu verbinden, da dadurch der Modus "Umgehung der Umgehungs Komprimierung" deaktiviert wird.

Direkte Erfassung von einem Gerät in einer ASF-Datei

Wenn Sie Audiodaten oder Videos direkt in einer ASF-Datei erfassen, sieht das Filter Diagramm in etwa wie folgt aus, je nach Art des verwendeten Erfassungs Geräts.

![Windows Media Video Capture Graph](images/asf-webcam.png)

Weitere Informationen zum Erstellen von Video-und audioerfassungs Diagrammen finden Sie in den folgenden Themen:

-   [Audioerfassung](audio-capture.md)
-   [Video Erfassung](video-capture.md)

Der WM-ASF-Writer wird nicht ausgeführt, es sei denn, alle seine Pins sind verbunden. Wenn Sie den WM-ASF-Writer mit dem Standardsystem Profil (nicht empfohlen) oder einem beliebigen Profil mit Audio-und Videostreams konfigurieren, wird eine Eingabe-PIN für jeden Stream erstellt, und jeder dieser Pins muss verbunden sein. Wenn Sie z. b. keine Audiodaten erfassen möchten, stellen Sie sicher, dass Sie den Filter mit einem nur-Video-Profil konfigurieren, sodass keine audiopin erstellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



