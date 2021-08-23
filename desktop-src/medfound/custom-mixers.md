---
description: Benutzerdefinierte Mixer
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Benutzerdefinierte Mixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587206f7bc34d1fad4a64a12aeff9ab8ad21e18a84c92c8f2302776fdc126a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605990"
---
# <a name="custom-mixers"></a>Benutzerdefinierte Mixer

In diesem Thema wird beschrieben, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) geschrieben wird. Sie können einen benutzerdefinierten Mixer mit der Media Foundation EVR-Mediensenke oder dem DirectShow EVR-Filter verwenden. Weitere Informationen zu Mixern und Moderatoren finden Sie unter [Enhanced Video Renderer](enhanced-video-renderer.md).

Der Mixer ist eine Media Foundation-Transformation (MFT) mit mindestens einer Eingabe (dem Verweisstream plus den Unterstreams) und einer Ausgabe. Der Eingabestream empfängt Beispiele vom Upstream. Der Ausgabestream übermittelt Beispiele an die Moderatorin. Die EVR ist für den Aufruf von [**"CSVTransform::P rocessInput"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) auf dem Mixer verantwortlich, und der Presenter ist für den Aufruf von [**"MIXERTransform::P rocessOutput"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)verantwortlich.

Ein EVR-Mixer muss mindestens die folgenden Schnittstellen implementieren:



| Schnittstelle                                                                | BESCHREIBUNG                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Stellt MFT-Basisfunktionen bereit.                                                                 |
| [**SHOPPERTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Ermöglicht dem Mixer das Abrufen von Schnittstellen aus der EVR.                                                |
| [**DINNERVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Ermöglicht dem Mixer das Abrufen von Schnittstellen aus der EVR.                                                |
| [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Wird verwendet, um das [**MF \_ SA \_ D3D \_ AWARE-Attribut**](mf-sa-d3d-aware-attribute.md) für die EVR verfügbar zu machen. |



 

Optional kann ein MFT eine der folgenden Schnittstellen implementieren:



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Erforderlich, um geschützten Inhalt wiederzuspielen.                                                                                                                  |
| [**VERZRGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Macht Schnittstellen wie Z.B. [**"ORBITVideoMixerBitmap"**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) und [**"WFVideoProcessor"**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) für die Anwendung verfügbar. |
| [**HAPQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Ermöglicht dem Qualitätsmanager, die Videoqualität anzupassen.                                                                                             |
| [**ORBITVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Ermöglicht der Anwendung das Mischen einer statischen Bitmap in das Video.                                                                                       |
| [**CITRIXVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Karten Koordinaten auf dem Ausgabevideorahmen zu Koordinaten für den Eingabevideorahmen.                                                                  |
| [**DENKVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Macht einige DXVA-Videoverarbeitungsfunktionen für die Anwendung verfügbar.                                                                                      |



 

Die Formataushandlung mit dem Mixer funktioniert wie folgt:

1.  Die EVR legt den Medientyp im Verweisstream fest.
2.  Der EVR ruft [**AUFANZEIGEVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) auf dem Presenter mit der **MFVP \_ MESSAGE \_ INVALIDATEMEDIATYPE-Nachricht** auf.

3.  Die Präsentation legt den Medientyp im Ausgabestream des Mixers fest.
4.  Die EVR legt den Medientyp für die Unterstreams fest.

Wenn sich der Medientyp im Verweisstream ändert, sind die anderen Medientypen des Mixers nicht mehr gültig. Die [**MIXERTransform::P rocessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers schlägt dann fehl und gibt **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE** zurück. Der Presenter sollte an diesem Punkt nichts tun. Die EVR initiiert den Formataushandlungsprozess erneut.

Wenn ein Eingabestream das Ende des Datenstroms erreicht, ruft der EVR MIT [**MFT \_ MESSAGE \_ NOTIFY END OF \_ \_ \_ STREAM**](mft-message-notify-end-of-stream.md)DIE [**BENACHRICHTIGUNGSTRANSFORM::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) auf dem Mixer auf.

Der Mixer sendet die folgenden Ereignisse über die [**IMediaEventSink-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) der EVR an die EVR. Diese Schnittstelle ist in der DirectShow SDK-Dokumentation dokumentiert.



| Ereignis                                            | Beschreibung                            |
|--------------------------------------------------|----------------------------------------|
| [**\_EC-BEISPIEL \_ ERFORDERLICH**](../directshow/ec-sample-needed.md) | Der Mixer erfordert ein neues Eingabebeispiel. |



 

Die EVR ruft möglicherweise [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer auf, bevor das Streaming gestartet wird. Der Mixer sollte diese Aufrufe nicht fehlschlagen. Stattdessen sollte die Ausgabeoberfläche mit schwarzen Pixeln gefüllt werden. Der Mixer sollte weiterhin Ausgabebeispiele mit Farben füllen, bis er eine [**MFT \_ MESSAGE NOTIFY \_ BEGIN \_ \_ STREAMING-Nachricht**](mft-message-notify-begin-streaming.md) empfängt oder die [**ProcessInput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) aufgerufen wird. Wenn der Mixer eine [**MFT \_ MESSAGE NOTIFY \_ END \_ \_ STREAMING-Nachricht**](mft-message-notify-end-streaming.md) empfängt, sollte er wieder in den Farbfüllmodus wechseln.

## <a name="implementing-imfvideodeviceid"></a>Implementieren von IMPLEMENTVIDEODeviceID

Die [**INTERFACESVideoDeviceID-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) enthält eine Methode, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)die eine Geräte-GUID zurückgibt. Die Geräte-GUID stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden. Wenn die Geräte-GUIDs nicht übereinstimmen, kann die EVR nicht initialisiert werden.

Sowohl der Standardmixer als auch der Presenter verwenden Direct3D 9, wobei die Geräte-GUID gleich IID \_ IDirect3DDevice9 ist. Wenn Sie Ihre benutzerdefinierte Präsentation mit dem Standardmixer verwenden möchten, muss die Geräte-GUID des Moderators IID \_ IDirect3DDevice9 sein. Wenn Sie beide Komponenten ersetzen, können Sie eine neue Geräte-GUID definieren.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementieren vonTOPTOPOLOGYServiceLookupClient

Der Mixer muss die [**SCHNITTSTELLE "MIXERTopologyServiceLookupClient"**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) implementieren. Bevor mit dem Streaming begonnen wird, ruft der EVR [**DENTOPTOPOLOGYServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) auf und übergibt einen Zeiger auf die [**INTERFACESTopologyServiceLookup-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) der EVR. Der Mixer verwendet diesen Zeiger, um Schnittstellenzeiger von der EVR abzurufen.

Der Mixer muss mindestens die folgende Schnittstelle abfragen:

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Wenn der EVR [**DENTOPTOPOLOGYServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)aufruft, muss der Mixer alle Zeiger freigeben, die aus dem Aufruf von [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)abgerufen wurden.

## <a name="mixer-attributes"></a>Mixer Attribute

Ein Mixer sollte die folgenden Attribute unterstützen.



| attribute                                                                        | Beschreibung                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                          | Gibt an, ob der Mixer DirectX Video Acceleration (DXVA) unterstützt.                                                                                                                                                                               |
| [**MF \_ SA \_ REQUIRED \_ SAMPLE \_ COUNT**](mf-sa-required-sample-count-attribute.md) | Die Anzahl der Videobeispiele, die die EVR für jeden Mixerstream zuordnen sollte. Dieses Attribut gilt für einzelne Streams. verwenden Sie den attributspeicher, der von [**DERTRANSFORM::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)zurückgegeben wird. |



 

## <a name="setting-the-mixer-on-the-evr"></a>Festlegen der Mixer für die EVR

Um einen benutzerdefinierten Mixer für die EVR festzulegen, rufen Sie [**DIE AUFFORDERUNGVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)auf. Sowohl der DirectShow EVR-Filter als auch die EVR-Mediensenke implementieren diese Methode.

**EVR-Aktivierungsobjekt**. Wenn Sie das EVR-Aktivierungsobjekt verwenden, können Sie einen benutzerdefinierten Mixer bereitstellen, indem Sie eines der folgenden Attribute für das EVR-Aktivierungsobjekt festlegen:



| attribute                                                                                                 | Beschreibung                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ ACTIVATE**](mf-activate-custom-video-mixer-activate-attribute.md) | Zeiger auf ein Aktivierungsobjekt für den Mixer. Das Aktivierungsobjekt muss die [**INTERFACESActivate-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) implementieren. |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID des Mixers.                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 
