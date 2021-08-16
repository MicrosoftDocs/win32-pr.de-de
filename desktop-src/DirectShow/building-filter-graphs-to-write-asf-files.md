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
-   Einfügen von Inhalten, die nicht Windows medienbasierten (nativen Streamformaten) in ASF-Dateien.
-   Erfassen sie Livedaten, und codieren Sie sie Windows Medienformat.

Transcodieren von ASF-Dateien

Sie können mithilfe des [WM ASF Writer](wm-asf-writer-filter.md) auf verschiedene Weise ein Filterdiagramm für die Dateitranscodierung erstellen. Am einfachsten fügen Sie den WM ASF Writer dem Filterdiagramm hinzu und verwenden dann die IGraphBuilder::RenderFile-Methode, um das Diagramm automatisch zu erstellen.

Eine alternative Möglichkeit besteht in der manuellen Hinzufügeweise jedes Filters zum Diagramm und zum Verbinden der Stecknadeln. Nachdem Sie den WM ASF Writer hinzugefügt haben, konfigurieren Sie ihn mithilfe der IConfigAsfWriter-Methoden, wenn das Standardprofil nicht geeignet ist, und verbinden Sie die WM ASF Writer-Eingabepins mit den entsprechenden Ausgabepins in den Upstreamfiltern.

Die folgende Abbildung zeigt typische WM ASF Writer-Transcodierungsfilterdiagrammkonfigurationen.

![Transcoding-Filterdiagramm](images/asf-transcode.png)

Einfügen nativer Streamformate in ASF-Dateien

Standardmäßig erwartet der WM ASF Writer-Filter unkomprimierte Audio- und Videostreams auf seinen Eingabepins und verwendet die Codecs Windows Media Audio und Windows Media Video, um die Streams zu komprimieren. Der ASF-Dateicontainer kann jedoch für jeden Datentyp verwendet werden. Indem Sie digitale Mediendaten in einem ASF-Dateicontainer platzieren, können Sie von ASF bereitgestellte Features hinzufügen, z. B. Metadaten und Digital Rights Management (DRM), ohne Ihre Inhalte transcodieren zu müssen.

Um eine ASF-Datei zu erstellen, die Inhalte enthält, die nicht Windows Media-basiert sind, muss die Anwendung den Stream im Filterdiagramm vor dem WM ASF Writer komprimieren und den Komprimierungsmechanismus des WM ASF Writer umgehen, indem [**sie IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) wie folgt aufruft:


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



Konfigurieren Sie dann den Filter mit dem gewünschten Profil. Es ist wichtig, dass der Medientyp des Eingabestreams genau dem Format im Profil entspricht. In einigen Fällen kann es erforderlich sein, das Format des Eingabestreams zu untersuchen und ein benutzerdefiniertes Profil zu erstellen, um es zu finden.

Wenn Sie den WM ASF Writer mit dem Upstreamfilter verbinden, verwenden Sie die IGraphBuilder::ConnectDirect-Methode. Verwenden Sie keine Intelligent Connect-Methoden wie IGraphBuilder::Verbinden oder IGraphBuilder::RenderFile, um den Filter zu verbinden, da dadurch der Modus "Umgehungskomprimierung" des Filters deaktiviert wird.

Direktes Erfassen von einem Gerät in einer ASF-Datei

Wenn Audio- oder Videodaten direkt in einer ASF-Datei erfasst werden, sieht das Filterdiagramm ähnlich wie folgt aus, je nachdem, welche Art von Erfassungsgerät verwendet wird.

![Diagramm zur Videoaufnahme von Windows-Medien](images/asf-webcam.png)

Weitere Informationen zum Erstellen von Video- und Audioaufnahmediagrammen finden Sie in den folgenden Themen:

-   [Audioaufnahme](audio-capture.md)
-   [Videoaufnahme](video-capture.md)

Der WM ASF Writer wird nur ausgeführt, wenn alle seine Pins verbunden sind. Wenn Sie WM ASF Writer mit dem Standardsystemprofil (nicht empfohlen) oder einem Profil mit Audio- und Videostreams konfigurieren, wird ein Eingabepin für jeden Stream erstellt, und jeder dieser Pins muss verbunden sein. Wenn Sie z. B. keine Audiodaten erfassen möchten, müssen Sie den Filter mit einem profilbasierten Video konfigurieren, damit kein Audiopin erstellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



