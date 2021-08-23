---
title: Medienplattform
description: Media Foundation und DirectShow bilden die Grundlage für die Medienunterstützung in Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a4db7d84745f64f3fe80faed267e58d1f5ddbce4ab82ed75b38453f82b0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964579"
---
# <a name="media-platform"></a>Medienplattform

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) und [DirectShow](/windows/desktop/DirectShow/directshow) bilden die Grundlage für die Medienunterstützung in Windows. Media Foundation wurde in Windows Vista als Ersatz für DirectShow eingeführt. In Windows 7 wurde Media Foundation verbessert, um eine bessere Formatunterstützung, einschließlich *MPEG-4,* sowie Unterstützung für Videoaufnahmegeräte und Hardwarecodecs zu bieten.

## <a name="format-support"></a>Formatunterstützung

In Windows 7 [bietet Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) umfangreiche Formatunterstützung, die Codecs für *H.264-Video,* *MJPEG* und *MP3 enthält.* neue Quellen für *MP4,* *3GP,* *AAC-Audio* und *AVI;* und neue Dateisenken für *MP4,* *3GP* und *MP3*. (Siehe [Unterstützte Medienformate in Media Foundation](../medfound/supported-media-formats-in-media-foundation.md).)

## <a name="hardware-devices"></a>Hardwaregeräte

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) unterstützt jetzt die folgenden Arten von Hardwaregeräten in der Audio-/Videopipeline:

-   *UVC 1.1-Videoaufnahmegeräte,* z. B. Webcams
-   Audioaufnahmegeräte
-   Hardwareencoder und Decoder
-   Hardwarevideoprozessoren, z. B. Farbraumkonverter

Hardwarecodecs können eine sehr schnelle Videotranscodierung durchführen. Angenommen, Sie möchten eine *WMV-Datei (Windows Media Video)* auf ein Mobiltelefon übertragen, das nur *3GP-Dateien* unterstützt. Mit einem Hardwareencoder kann die Datei "nach Bedarf" transcodiert werden, unmittelbar bevor sie an das Gerät übertragen wird.

Hardwaregeräte werden [in](/windows/desktop/medfound/microsoft-media-foundation-sdk) Media Foundation proxy-Objekt dargestellt und wie softwarebasierte Komponenten in der Pipeline verwendet. (Weitere [Informationen finden Sie unter What es New for Media Foundation](../medfound/whats-new-for-media-foundation.md).)

## <a name="simplified-programming-model"></a>Vereinfachtes Programmiermodell

In Windows Vista [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) eine relativ niedrige Gruppe von APIs verfügbar. Diese APIs sind flexibel, aber möglicherweise nicht zum Ausführen von Aufgaben geeignet. Windows 7 fügt neue apIs auf hoher Ebene hinzu, die das Schreiben von Medienanwendungen in *C++ vereinfachen.* Zu diesen neuen apIs auf hoher Ebene gehören:

-   **MFPlay**. Diese APIs sind für die Audio- und Videowiedergabe konzipiert. Sie unterstützen die typischen Wiedergabevorgänge (Beenden, Anhalten, Wiedergeben, Suchen, Ratensteuerung, Audiovolumen usw.), während die Details der Low-Level-APIs (die Sitzungs- und Topologieebenen) verborgen werden.
-   **Quellleser**. Sie können diese APIs verwenden, um rohe oder decodierte Daten aus einer Mediendatei zu pullen, ohne etwas über das zugrunde liegende Format zu wissen. Beispielsweise können Sie eine Miniaturbildbitmap aus einer Videodatei oder Livevideoframes von einer Webcam erhalten.
-   **Sink Writer**. Sie können diese APIs verwenden, um Mediendateien zu erstellen, indem Sie unkomprimierte oder codierte Daten übergeben. Beispielsweise können Sie eine Videodatei neu codieren oder neu kombinieren.
-   **Transcodieren von**. Diese APIs sind für die gängigsten Audio- und Videocodierungsszenarien.

## <a name="platform-improvements"></a>Plattformverbesserungen

Windows 7 enthält zahlreiche Verbesserungen an [](/windows/desktop/medfound/microsoft-media-foundation-sdk) den zugrunde liegenden Media Foundation-APIs. Erweiterte Anwendungen können diese APIs direkt verwenden. andere Anwendungen profitieren indirekt von den Vorteilen. Zu diesen Vorteilen zählen:

-   Verbesserungen an der Videopipeline, um den Energieverbrauch und die Nutzung des Videospeichers zu reduzieren.
-   Neue  DVXA-Videoverarbeitungs-APIs, die ein flexibleres Compositing-Modell verwenden und besser für *HD-Videoformate* geeignet sind.
-   Verbesserungen der Art und Weise, wie Plug-Ins (Quellen und Decoder) aufzählt und verwaltet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neues bei Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 