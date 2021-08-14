---
description: Erstellen von Filterdiagrammen zum Schreiben von ASF-Dateien
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Erstellen von Filterdiagrammen zum Schreiben von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe53dcee310be34c321dfc2e988807184735a24b0793d68e3ca7dea10d0b29e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662748"
---
# <a name="building-filter-graphs-to-write-asf-files"></a>Erstellen von Filterdiagrammen zum Schreiben von ASF-Dateien

Beim Erstellen Windows medienbasierten Inhalts verwenden Anwendungen in der Regel eines der folgenden Szenarien:

-   Konvertieren oder Transcodieren von Inhalten aus einem anderen Format in Windows Medienformat.
-   Einfügen von Inhalten, die nicht Windows Medienbasiert (native Streamformate) in ASF-Dateien sind.
-   Erfassen von Livedaten und sofortiges Codieren in Windows Medienformat.

Transcodierung von ASF-Dateien

Sie können mit dem [WM ASF Writer](wm-asf-writer-filter.md) auf verschiedene Weise einen Dateitranscodierungsfiltergraphen erstellen. Die einfachste Möglichkeit besteht darin, den WM ASF Writer dem Filterdiagramm hinzuzufügen und dann die IGraphBuilder::RenderFile-Methode zu verwenden, um das Diagramm automatisch zu erstellen.

Eine alternative Möglichkeit besteht darin, jeden Filter manuell zum Diagramm hinzuzufügen und die Stecknadeln zu verbinden. Nachdem Sie den WM ASF Writer hinzugefügt haben, konfigurieren Sie ihn mithilfe der IConfigAsfWriter-Methoden, wenn das Standardprofil nicht geeignet ist, und verbinden Sie die WM ASF Writer-Eingabepins mit den entsprechenden Ausgabepins in den Upstreamfiltern.

Die folgende Abbildung zeigt typische Konfigurationen von WM ASF Writer-Transcodierungsfilterdiagrammen.

![Transcodierungsfilterdiagramm](images/asf-transcode.png)

Einfügen nativer Streamformate in ASF-Dateien

Standardmäßig erwartet der WM ASF Writer-Filter unkomprimierte Audio- und Videostreams auf den Eingabepins und verwendet die Windows Medienaudio- und Windows Media Video-Codecs, um die Datenströme zu komprimieren. Der ASF-Dateicontainer kann jedoch für jeden Datentyp verwendet werden. Indem Sie digitale Mediendaten in einem ASF-Dateicontainer platzieren, können Sie von ASF bereitgestellte Features wie Metadaten und DRM (Digital Rights Management) hinzufügen, ohne Ihre Inhalte transcodieren zu müssen.

Um eine ASF-Datei zu erstellen, die Inhalte enthält, die nicht Windows Medienbasiert sind, muss die Anwendung den Datenstrom im Filterdiagramm vor dem WM ASF Writer komprimieren und den Komprimierungsmechanismus des WM ASF Writer umgehen, indem [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) wie folgt aufgerufen wird:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Konfigurieren Sie dann den Filter mit dem gewünschten Profil. Es ist wichtig, dass der Medientyp des Eingabestreams genau mit dem Format im Profil übereinstimmt. In einigen Fällen kann es erforderlich sein, das Format des Eingabestreams zu untersuchen und ein benutzerdefiniertes Profil zu erstellen, um es abzugleichen.

Wenn Sie den WM ASF Writer mit dem Upstreamfilter verbinden, verwenden Sie die IGraphBuilder::ConnectDirect-Methode. Verwenden Sie keine "intelligent connect"-Methoden wie IGraphBuilder::Verbinden oder IGraphBuilder::RenderFile, um den Filter zu verbinden, da dadurch der Modus "Bypass compression" des Filters deaktiviert wird.

Direkte Erfassung von einem Gerät in eine ASF-Datei

Wenn Audio- oder Videodaten direkt in einer ASF-Datei erfasst werden, sieht das Filterdiagramm je nach verwendeter Art des Erfassungsgeräts in etwa wie folgt aus.

![Windows Media Video Capture Graph](images/asf-webcam.png)

Weitere Informationen zum Erstellen von Video- und Audioaufzeichnungsdiagrammen finden Sie in den folgenden Themen:

-   [Audioaufnahme](audio-capture.md)
-   [Videoaufnahme](video-capture.md)

Der WM ASF Writer wird nur ausgeführt, wenn alle pins verbunden sind. Wenn Sie WM ASF Writer mit dem Standardsystemprofil (nicht empfohlen) oder einem profil mit Audio- und Videostreams konfigurieren, wird ein Eingabepin für jeden Datenstrom erstellt, und jeder dieser Pins muss verbunden sein. Wenn Sie z. B. keine Audiodaten erfassen möchten, müssen Sie den Filter mit einem profil nur für Videos konfigurieren, sodass kein Audiopin erstellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



