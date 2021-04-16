---
title: Medienplattform
description: Media Foundation und DirectShow bilden die Grundlage für die Unterstützung von Medien in Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f756112384451ac3f5b4055d73a60a170b2e29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517057"
---
# <a name="media-platform"></a>Medienplattform

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) und [DirectShow](/windows/desktop/DirectShow/directshow) bilden die Grundlage für die Unterstützung von Medien in Windows. Media Foundation wurde in Windows Vista als Ersatz für DirectShow eingeführt. In Windows 7 wurde Media Foundation verbessert, um eine bessere Formatunterstützung, einschließlich *MPEG-4*, sowie Unterstützung für Video Erfassungsgeräte und Hardware Codecs bereitzustellen.

## <a name="format-support"></a>Format Unterstützung

In Windows 7 bietet [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) eine umfangreiche Formatunterstützung, die Codecs für *H. 264* -Video, *MJPEG* und *MP3* umfasst. neue Quellen für *MP4*, *3GP*, *AAC* -Audiodaten und *AVI*; und neue dateisenken für *MP4*, *3GP* und *MP3*. (Informationen hierzu finden Sie [unter Unterstützte Medienformate in Media Foundation](../medfound/supported-media-formats-in-media-foundation.md).)

## <a name="hardware-devices"></a>Hardware Geräte

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) unterstützt jetzt die folgenden Typen von Hardware Geräten in der Audio-/Video-Pipeline:

-   *UVC 1,1* -Video Erfassungsgeräte, z. b. Webcams
-   Audioerfassungs Geräte
-   Hardware Codierern und Decoder
-   Hardware-Video Prozessoren, z. b. Farb Raum Konverter

Hardware-Codecs können eine sehr schnelle Video-Transcodierung durchführen. Angenommen, Sie möchten eine Windows Media Video-Datei *(WMV)* an ein Mobiltelefon übertragen, das nur *3GP-* Dateien unterstützt. Bei einem Hardware Encoder kann die Datei nach Bedarf nach der Übertragung auf das Gerät transcodiert werden.

Hardware Geräte werden in [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) durch ein Proxy Objekt dargestellt und wie softwarebasierte Komponenten in der Pipeline verwendet. (Weitere Informationen finden Sie unter [What es New for Media Foundation](../medfound/whats-new-for-media-foundation.md).)

## <a name="simplified-programming-model"></a>Vereinfachtes Programmiermodell

In Windows Vista wurde [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) einen relativ niedrigen Satz von APIs verfügbar gemacht. Diese APIs sind flexibel, sind aber möglicherweise nicht für die Ausführung von Aufgaben geeignet. Windows 7 fügt neue APIs auf hoher Ebene hinzu, die das Schreiben von Medienanwendungen in *C++* vereinfachen. Diese neuen High-Level-APIs umfassen Folgendes:

-   **MF Play**. Diese APIs sind für die Audiowiedergabe und Videowiedergabe konzipiert. Sie unterstützen die normalen Wiedergabe Vorgänge ("anhalten", "anhalten", "spielen", "suchen", "Raten Kontrolle", "audiovolume" usw.) und verbergen die Details der Low-Level-APIs (die Sitzungs-und Topologieschichten).
-   Der **Quell Reader**. Mit diesen APIs können Sie Rohdaten oder decodierte Daten aus einer Mediendatei abrufen, ohne etwas über das zugrunde liegende Format zu wissen. Beispielsweise können Sie eine Miniaturansicht aus einer Videodatei oder Live Video Frames von einer Webcam erhalten.
-   **Senke-Writer**. Sie können diese APIs verwenden, um Mediendateien zu erstellen, indem Sie unkomprimierte oder codierte Daten übergeben. Beispielsweise können Sie eine Videodatei erneut codieren oder reaktivieren.
-   **Transcode**. Diese APIs Zielen auf die gängigsten Audio-und Video Codierungs Szenarios ab.

## <a name="platform-improvements"></a>Platt Form Verbesserungen

Windows 7 umfasst zahlreiche Verbesserungen an den zugrunde liegenden [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) Plattform-APIs. Erweiterte Anwendungen können diese APIs direkt verwenden. andere Anwendungen erhalten die Vorteile indirekt. Zu diesen Vorteilen zählen:

-   Verbesserungen an der Video Pipeline, um den Energieverbrauch und die Verwendung des Video Speichers zu reduzieren
-   Neue *dvxa* -Videoverarbeitungs-APIs, die ein flexibleres Zusammensetzung-Modell verwenden und besser für *HD* -Videoformate geeignet sind.
-   Verbesserungen an der Art und Weise, in der Plug-ins (Quellen und Decoders) aufgelistet und verwaltet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neuerungen bei Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 