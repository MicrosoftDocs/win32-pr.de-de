---
description: Microsoft Media Foundation wurde in Windows Vista als Ersatz für DirectShow eingeführt. DirectShow wird natürlich weiterhin in Windows 7 unterstützt, Entwickler sollten jedoch Media Foundation in ihren neuen digitalen Medienanwendungen verwenden.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Neuerungen für Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd2cd2b70ce23968ba9a302e4ab4e825914931ebffff651b534ee0974d75cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012060"
---
# <a name="whats-new-for-media-foundation"></a>Neuerungen bei Media Foundation

Microsoft Media Foundation wurde in Windows Vista als Ersatz für DirectShow eingeführt. DirectShow wird natürlich weiterhin in Windows 7 unterstützt, Entwickler sollten jedoch Media Foundation in ihren neuen digitalen Medienanwendungen verwenden.

Die Verbesserungen an Media Foundation können wie folgt zusammengefasst werden:

-   Bessere Formatunterstützung, einschließlich MPEG-4
-   Unterstützung für Erfassungsgeräte und Hardwarecodecs
-   Ein vereinfachtes Programmiermodell
-   Verbesserungen an der Plattform

## <a name="better-format-support"></a>Bessere Formatunterstützung

Die Media Foundation Audio-/Videopipeline wurde in Windows Vista implementiert, unterstützte aber eine begrenzte Anzahl von Formaten und Dateicontainern, was bedeutete, dass einige Anwendungen auf ältere Technologien wie DirectShow zurückgreifen mussten. In Windows 7 enthält Media Foundation die folgenden neuen Codecs, Medienquellen und Mediensenken:

-   AAC-Decoder
-   AAC-Encoder
-   AVI/WAVE-Dateiquelle
-   DV-Videodecoder
-   H.264-Videodecoder
-   H.264-Videoencoder
-   MJPEG-Decoder
-   MP3-Dateisenke\*
-   MP4/3GP-Dateiquelle
-   MP4/3GP-Dateisenke

> [!Note]  
> Die MP3-Dateisenke enthält keinen MP3-Audioencoder.

 

Weitere Informationen finden Sie unter [Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Hardwaregeräteunterstützung

Media Foundation unterstützt jetzt die folgenden Arten von Hardwaregeräten in der Audio-/Videopipeline:

-   UVC 1.1-Videoaufnahmegeräte wie Webcams
-   Audioaufnahmegeräte
-   Hardwareencoder und Decoder
-   Hardwarevideoprozessoren wie Farbraumkonverter

Hardwarecodecs können eine sehr schnelle Videotranscodierung durchführen. Beispielsweise kann eine Anwendung Windows WMV-Dateien (Media Video) auf ein Mobiltelefon übertragen, das nur 3GP-Dateien unterstützt. Mithilfe eines Hardwareencoders kann die Anwendung die Datei im Backgound transcodieren, kurz bevor sie auf das Gerät übertragen wird.

Hardwaregeräte werden in Media Foundation durch ein Proxyobjekt dargestellt und in der Pipeline genauso wie softwarebasierte Komponenten verwendet.

## <a name="simplified-programming-model"></a>Vereinfachtes Programmiermodell

In Windows Vista Media Foundation einen relativ niedrigen Satz von APIs verfügbar gemacht. Diese APIs sind flexibel, aber zu komplex für einfache Aufgaben. Windows 7 werden neue apIs auf hoher Ebene hinzugefügt, die das Schreiben von Medienanwendungen in C++ vereinfachen. Diese neuen apis auf hoher Ebene umfassen Folgendes.



| API                                | Beschreibung                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Quellleser](source-reader.md) | Der Quellleser pullt unformatierte oder decodierte Daten aus einer Mediendatei. Beispielsweise können Sie den Quellleser verwenden, um Miniaturbildbitmaps aus einer Videodatei abzurufen oder die Wellenformdaten in einer Audiodatei zu analysieren. Sie können auch den Quellleser verwenden, um Livedaten von einem Audio- oder Videoaufnahmegerät abzurufen. <br/> |
| [Sink Writer](sink-writer.md)     | Mit dem Senkenwriter können Sie Mediendateien erstellen, indem Sie unkomprimierte oder codierte Daten übergeben. Beispielsweise können Sie damit eine Videodatei erneut codieren oder Livevideos von einer Webcam in einer Datei erfassen.                                                                                                         |
| [Transcodieren der API](transcode-api.md) | Dieses Feature unterstützt die gängigsten Audio-/Videocodierungsszenarien.<br/>                                                                                                                                                                                                                               |



 

Sie können weiterhin die low-level-APIs in Media Foundation verwenden. Sie können dies tun, wenn Sie mehr Kontrolle über die Audio-/Videopipeline benötigen.

## <a name="platform-improvements"></a>Plattformverbesserungen

Windows 7 enthält zahlreiche Verbesserungen an den zugrunde liegenden Media Foundation Plattform-APIs. Erweiterte Anwendungen können diese APIs direkt verwenden. andere Anwendungen profitieren indirekt von den Vorteilen. Die Verbesserungen umfassen:

-   Änderungen in der Videopipeline, um den Energieverbrauch und die Videospeicherauslastung zu reduzieren.
-   [DXVA-HD:](dxva-hd.md)Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine neue API für die hardwarebeschleunigte Videoverarbeitung. DXVA-HD bietet ein flexibleres Compositingmodell als die vorherige DXVA-Videoverarbeitungs-API und eignet sich besser für High-Definition-Videoformate.
-   Ein neuer Mechanismus zum Auflisten von Quellen und Decodern, der Werte für Dieverwerter und eine Bevorzugte/Blockiert-Liste enthält. Dieses Feature verbessert die allgemeine Zuverlässigkeit des Systems. Weitere Informationen finden Sie in den folgenden Themen:
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**THICKNESSPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Codec-Vererzung](codec-merit.md)

## <a name="sdk-changes"></a>SDK-Änderungen

-   Neue Header und Bibliotheksdateien: [Media Foundation Header und Bibliotheken](media-foundation-headers-and-libraries.md)
-   DLL- und LIB-Änderungen: [Bibliotheksänderungen in Windows 7](media-foundation-headers-and-libraries.md)
-   Neue SDK-Beispiele:
    -   [Beispiel für Audioclip](audio-clip-sample.md)
    -   [DXVA-HD-Beispiel](dxva-hd-sample.md)
    -   [MFCaptureD3D-Beispiel](mfcaptured3d-sample.md)
    -   [MFCaptureToFile-Beispiel](mfcapturetofile-sample.md)
    -   [Beispiel für Transcodierung](transcode-sample.md)
    -   [VideoThumbnail-Beispiel](videothumbnail-sample.md)
-   Verbesserungen an [TopoEdit:](topoedit.md)
    -   Unterstützung für die Transcodierung. Weitere Informationen finden Sie unter Erstellen einer [Transcodetopologie mit TopoEdit.](building-a-transcode-topology-with-topoedit.md)
    -   Unterstützung für Audio- und Videoaufnahmen. Weitere Informationen finden Sie [unter Topologiemenü.](topology-menu.md)

## <a name="new-in-windows-8"></a>Neu in Windows 8

Einige der neuen Updates für Media Foundation mit Windows 8 sind:

-   [**DAS GERÄTCAPTUREEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) steuert ein oder mehrere Erfassungsgeräte. Eine Liste der Attribute finden Sie unter Attribute der [Erfassungs-Engine.](capture-engine-attributes.md) Weitere neue Schnittstellen im Zusammenhang mit der Medienerfassung sind DIE SCHNITTSTELLEN [**"CSVCapturePhotoSink",**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink) [**"ZOOMCapturePreviewSink",**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink) [**"ZOOMCaptureRecordSink",**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink) [**"ZOOMCaptureSink"**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)und [**"ENCAPTURESOURCE".**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource)
-   Die folgenden Media Foundation-Klassenerweiterungen sind für Windows 8 neu:
    -   [**ANDROMEDIAEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**WFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**REALRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**ÜBERPRÜFENSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**SOURCEReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**ÜBERPRÜFENVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**MENUWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   [Direct3D 11 Video API](direct3d-11-video-apis.md) sind neu für Windows 8. Windows 8 Desktop-Apps können weiterhin [die Direct3D 9 Video-API](direct3d-video-apis.md)verwenden, aber Windows Store Apps müssen die neue Direct3D 11 Video-API verwenden. Weitere Informationen zu Microsoft Direct3D 11 Video finden Sie unter [Supporting Direct3D 11 Video Decoding in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Es wurden Updates und Verbesserungen an Media Foundation Arbeitswarteschlangen vorgenommen. Weitere Informationen finden Sie unter [Verbesserungen der Arbeitswarteschlange und des Threadings.](media-foundation-work-queue-and-threading-improvements.md)
-   [H.264 UVC 1.5-Kameraencoder](camera-encoder-h264-uvc-1-5.md).
-   Eine Liste der Media Foundation-API, die mit Windows Store-Apps verwendet werden kann, finden Sie unter Win32 und COM für [Windows Store-Apps (Multimedia).](media-foundation-headers-and-libraries.md)
-   Media Foundation ist nicht in den N- und KN-Editionen von Windows 8. Weitere Informationen finden Sie unter [Microsoft Windows Media Feature Pack für N- und KN-Versionen aller Windows 8 Editionen.](https://support.microsoft.com/kb/2703761)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




