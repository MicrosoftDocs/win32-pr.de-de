---
description: Microsoft Media Foundation wurde in Windows Vista als Ersatz für DirectShow eingeführt. Natürlich wird DirectShow weiterhin in Windows 7 unterstützt, aber Entwicklern wird empfohlen, Media Foundation in ihren neuen Anwendungen für digitale Medien zu verwenden.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Neuerungen bei Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0270c28e5aca2a1f0fdad893743a1e8fb630fa5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351368"
---
# <a name="whats-new-for-media-foundation"></a>Neuerungen bei Media Foundation

Microsoft Media Foundation wurde in Windows Vista als Ersatz für DirectShow eingeführt. Natürlich wird DirectShow weiterhin in Windows 7 unterstützt, aber Entwicklern wird empfohlen, Media Foundation in ihren neuen Anwendungen für digitale Medien zu verwenden.

Die Verbesserungen an Media Foundation können wie folgt zusammengefasst werden:

-   Bessere Formatunterstützung, einschließlich MPEG-4
-   Unterstützung für Erfassungsgeräte und Hardware Codecs
-   Vereinfachtes Programmiermodell
-   Verbesserungen an der Plattform

## <a name="better-format-support"></a>Bessere Format Unterstützung

Die Media Foundation Audio-/Video-Pipeline wurde in Windows Vista implementiert, aber es wurde ein eingeschränkter Satz von Formaten und Datei Containern unterstützt. Dies bedeutete, dass einige Anwendungen auf ältere Technologien wie DirectShow zurückgreifen mussten. In Windows 7 umfasst Media Foundation die folgenden neuen Codecs, Medienquellen und Medien senken:

-   AAC-Decoder
-   AAC-Encoder
-   AVI/Wave-Datei Quelle
-   DV-Video Decoder
-   H. 264-Video Decoder
-   H. 264-Video Encoder
-   MJPEG-Decoder
-   MP3-Datei Senke\*
-   MP4/3GP-Datei Quelle
-   MP4/3GP-Datei Senke

> [!Note]  
> Die MP3-Datei Senke enthält keinen MP3-Audioencoder.

 

Weitere Informationen finden Sie [unter Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Hardware Geräte Unterstützung

Media Foundation unterstützt jetzt die folgenden Typen von Hardware Geräten in der Audio-/Video-Pipeline:

-   UVC 1,1-Video Erfassungsgeräte, z. b. Webcams
-   Audioerfassungs Geräte
-   Hardware Codierern und Decoder
-   Hardware-Video Prozessoren, z. b. Farb Raum Konverter

Hardware-Codecs können eine sehr schnelle Video-Transcodierung durchführen. Eine Anwendung kann z. b. Windows Media Video (WMV)-Dateien an ein Mobiltelefon übertragen, das nur 3GP-Dateien unterstützt. Mithilfe eines Hardware Encoders kann die Anwendung die Datei im Hintergrund vor der Übertragung auf das Gerät transcodieren.

Hardware Geräte werden in Media Foundation durch ein Proxy Objekt dargestellt und wie softwarebasierte Komponenten in der Pipeline verwendet.

## <a name="simplified-programming-model"></a>Vereinfachtes Programmiermodell

In Windows Vista wurde Media Foundation einen relativ niedrigen Satz von APIs verfügbar gemacht. Diese APIs sind flexibel, aber zu komplex für einfache Aufgaben. Windows 7 fügt neue APIs auf hoher Ebene hinzu, die das Schreiben von Medienanwendungen in C++ vereinfachen. Diese neuen APIs auf hoher Ebene umfassen Folgendes:



| API                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Quell Leser](source-reader.md) | Der Quell Leser ruft Rohdaten oder decodierte Daten aus einer Mediendatei ab. Beispielsweise können Sie den Quell Leser zum Aufrufen von Miniatur Ansichts-Bitmaps aus einer Videodatei oder zum Analysieren der Wellenform-Daten in einer Audiodatei verwenden. Sie können auch den Quell Reader verwenden, um Livedaten von einem Audiogerät oder Video Erfassungsgerät zu erhalten. <br/> |
| [Senke-Writer](sink-writer.md)     | Der Senke Writer ermöglicht das Erstellen von Mediendateien, indem unkomprimierte oder codierte Daten übergeben werden. Beispielsweise können Sie Sie zum erneuten Codieren einer Videodatei oder zum Erfassen von Livevideos von einer Webcam in eine Datei verwenden.                                                                                                         |
| [Transcode-API](transcode-api.md) | Diese Funktion unterstützt die gängigsten Audio-/videocodierungsszenarien.<br/>                                                                                                                                                                                                                               |



 

Die Low-Level-APIs können weiterhin in Media Foundation verwendet werden. Dies ist möglicherweise der Fall, wenn Sie mehr Kontrolle über die Audio-/Video-Pipeline benötigen.

## <a name="platform-improvements"></a>Platt Form Verbesserungen

Windows 7 umfasst zahlreiche Verbesserungen an den zugrunde liegenden Media Foundation Plattform-APIs. Erweiterte Anwendungen können diese APIs direkt verwenden. andere Anwendungen erhalten die Vorteile indirekt. Die Verbesserungen umfassen:

-   Änderungen in der Video Pipeline, um den Energieverbrauch und die Verwendung von Video Arbeitsspeicher zu verringern.
-   [DXVA-HD](dxva-hd.md): Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine neue API für die hardwarebeschleunigte Video Verarbeitung. DXVA-HD bietet ein flexibleres Zusammensetzung-Modell als die vorherige DXVA-Videoverarbeitungs-API und eignet sich besser für Videoformate mit hoher Definition.
-   Ein neuer Mechanismus zum Auflisten von Quellen und Decodern, der Verdienst Werte und eine bevorzugte/blockierte Liste enthält. Diese Funktion verbessert die Gesamtzuverlässigkeit des Systems. Weitere Informationen finden Sie unter den folgenden Themen:
    -   [**MF-Datei**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMF-Steuerelement**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Codec-Verdienst](codec-merit.md)

## <a name="sdk-changes"></a>SDK-Änderungen

-   Neue Header und Bibliotheksdateien: [Media Foundation-Header und-Bibliotheken](media-foundation-headers-and-libraries.md)
-   DLL-und lib-Änderungen: [Bibliotheks Änderungen in Windows 7](media-foundation-headers-and-libraries.md)
-   Neue SDK-Beispiele:
    -   [Beispiel für Audioclip](audio-clip-sample.md)
    -   [DXVA-HD-Beispiel](dxva-hd-sample.md)
    -   [MFCaptureD3D-Beispiel](mfcaptured3d-sample.md)
    -   [MF-Datei Beispiel](mfcapturetofile-sample.md)
    -   [Transcode-Beispiel](transcode-sample.md)
    -   [Videothumbnail-Beispiel](videothumbnail-sample.md)
-   Verbesserungen an [topoedit](topoedit.md):
    -   Unterstützung für die Transcodierung. Weitere Informationen finden Sie unter aufbauen einer [transcode-Topologie mit topoedit](building-a-transcode-topology-with-topoedit.md).
    -   Unterstützung für die Audio-und Video Erfassung. Siehe [Menü Topologie](topology-menu.md).

## <a name="new-in-windows-8"></a>Neu in Windows 8

Einige der neuen Updates für Media Foundation mit Windows 8 lauten:

-   Die [**IMF-Engine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) steuert ein oder mehrere Erfassungsgeräte. Eine Liste der Attribute finden Sie unter [Attribute der Erfassungs-Engine](capture-engine-attributes.md) . Andere neue Medien Erfassungs Schnittstellen sind [**IMF capturephotosink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**IMF capturepreviewsink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**IMF capturerecordsink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**IMF capturesink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)und [**IMF capturesource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).
-   Die folgenden Media Foundation-Klassen Erweiterungen für Windows 8 sind neu:
    -   [**IMF mediaengineex**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**Imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**Imfrealtimecliumtex**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**Imbsinkschreiterex**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMF sourcereaderex**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMF videosamplezuweisungen**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMF workqueueservicesex**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   Die [Video-API von Direct3D 11](direct3d-11-video-apis.md) ist neu für Windows 8. Windows 8-Desktop-Apps können weiterhin die [Direct3D 9-Video-API](direct3d-video-apis.md)verwenden, Windows Store-Apps müssen jedoch die neue Direct3D 11-Video-API verwenden. Weitere Informationen zu Microsoft Direct3D 11 finden Sie [unter Unterstützung von Direct3D 11 Video Decodierung in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Es gab Updates und Verbesserungen an Media Foundation Arbeits Warteschlangen. Weitere Informationen finden Sie unter [Arbeits Warteschlangen und Threading Verbesserungen](media-foundation-work-queue-and-threading-improvements.md) .
-   [H. 264 UVC 1,5-Kamera Encoder](camera-encoder-h264-uvc-1-5.md).
-   Eine Liste der Media Foundation-API, die mit Windows Store-Apps verwendet werden kann, finden Sie unter [Win32 und com für Windows Store-Apps (Multimedia)](media-foundation-headers-and-libraries.md).
-   Media Foundation ist nicht in den N-und KN-Editionen von Windows 8 enthalten. Weitere Informationen finden Sie unter [Microsoft Windows Media Feature Pack für N-und KN-Versionen aller Windows 8-Editionen](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




