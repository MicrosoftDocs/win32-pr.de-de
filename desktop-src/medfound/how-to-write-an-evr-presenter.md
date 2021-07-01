---
description: In diesem Artikel wird beschrieben, wie Sie eine benutzerdefinierte Präsentation für den erweiterten Videorenderer (EVR) schreiben.
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Schreiben eines EVR-Presenters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118775"
---
# <a name="how-to-write-an-evr-presenter"></a>Schreiben eines EVR-Presenters

In diesem Artikel wird beschrieben, wie Sie eine benutzerdefinierte Präsentation für den erweiterten Videorenderer (EVR) schreiben. Eine benutzerdefinierte Präsentation kann sowohl mit DirectShow als auch mit Media Foundation verwendet werden. Die Schnittstellen und das Objektmodell sind für beide Technologien identisch, obwohl die genaue Reihenfolge der Vorgänge variieren kann.

Der Beispielcode in diesem Thema wird aus dem [EVRPresenter-Beispiel](evrpresenter-sample.md)angepasst, das im Windows SDK bereitgestellt wird.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Presenter-Objektmodell](#presenter-object-model)
    -   [Datenfluss innerhalb der EVR](#data-flow-inside-the-evr)
    -   [Presenter States](#presenter-states)
    -   [Presenter-Schnittstellen](#presenter-interfaces)
    -   [Implementieren von IMPLEMENTVIDEODeviceID](#implementing-imfvideodeviceid)
    -   [Implementieren vonTOPTOPOLOGYServiceLookupClient](#implementing-imftopologyservicelookupclient)
    -   [Implementieren von IMPLEMENTVIDEOPresenter](#implementing-imfvideopresenter)
    -   [Implementieren von IMPLEMENTClockStateSink](#implementing-imfclockstatesink)
    -   [Implementieren von IMPLEMENTRATESupport](#implementing-imfratesupport)
    -   [Senden von Ereignissen an die EVR](#sending-events-to-the-evr)
-   [Aushandeln von Formaten](#negotiating-formats)
-   [Verwalten des Direct3D-Geräts](#managing-the-direct3d-device)
    -   [Zuordnen von Direct3D-Oberflächen](#allocating-direct3d-surfaces)
    -   [Überwachungsbeispiele](#tracking-samples)
-   [Verarbeiten der Ausgabe](#processing-output)
    -   [Neumalen von Frames](#repainting-frames)
    -   [Zeitplanungsbeispiele](#scheduling-samples)
    -   [Präsentieren von Beispielen](#presenting-samples)
    -   [Quell- und Zielrechtecke](#source-and-destination-rectangles)
    -   [Ende des Streams](#end-of-stream)
-   [Einzelschritt im Rahmen](#frame-stepping)
    -   [Implementieren von Frameschritten](#implementing-frame-stepping)
-   [Festlegen des Presenters auf der EVR](#setting-the-presenter-on-the-evr)
    -   [Festlegen der Präsentation in DirectShow](#setting-the-presenter-in-directshow)
    -   [Festlegen des Presenters in Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Verwandte Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie eine benutzerdefinierte Präsentation schreiben, sollten Sie mit den folgenden Technologien vertraut sein:

-   Der erweiterte Videorenderer. Weitere Informationen finden Sie unter [Erweiterter Videorenderer.](enhanced-video-renderer.md)
-   Direct3D-Grafiken. Sie müssen keine 3D-Grafiken verstehen, um eine Präsentation zu schreiben, aber Sie müssen wissen, wie Sie ein Direct3D-Gerät erstellen und Direct3D-Oberflächen verwalten. Wenn Sie nicht mit Direct3D vertraut sind, lesen Sie die Abschnitte "Direct3D-Geräte" und "Direct3D-Ressourcen" in der DirectX Graphics SDK-Dokumentation.
-   DirectShow-Filterdiagramme oder die Media Foundation Pipeline, je nachdem, welche Technologie Ihre Anwendung zum Rendern von Videos verwendet.
-   [Media Foundation Transformiert](media-foundation-transforms.md). Der EVR-Mixer ist eine Media Foundation-Transformation, und der Moderator ruft Methoden direkt auf dem Mixer auf.
-   Implementieren von COM-Objekten. Der Presenter ist ein Prozess-COM-Objekt mit Freethreading.

## <a name="presenter-object-model"></a>Presenter-Objektmodell

Dieser Abschnitt enthält eine Übersicht über das Presenter-Objektmodell und die Schnittstellen.

### <a name="data-flow-inside-the-evr"></a>Datenfluss innerhalb der EVR

Die EVR verwendet zwei Plug-In-Komponenten zum Rendern von Videos: den *Mixer* und den *Presenter*. Der Mixer kombiniert die Videostreams und deinterlaciert das Video bei Bedarf. Die Moderatorin zeichnet (oder *präsentiert*) das Video auf der Anzeige und plant, wann jeder Frame gezeichnet wird. Anwendungen können eines dieser Objekte durch eine benutzerdefinierte Implementierung ersetzen.

Die EVR verfügt über einen oder mehrere Eingabestreams, und der Mixer verfügt über eine entsprechende Anzahl von Eingabestreams. Stream 0 ist immer der *Verweisstream.* Die anderen Streams sind *Unterstreams,* die der Mixer alpha-blendet in den Verweisstream einblendet. Der Verweisstream bestimmt die Masterbildrate für das zusammengesetzte Video. Für jeden Verweisrahmen nimmt der Mixer den neuesten Frame aus jedem Unterstream, blendet sie alpha-blendend in den Referenzrahmen ein und gibt einen einzelnen zusammengesetzten Frame aus. Der Mixer führt bei Bedarf auch Deinterlacing und Farbkonvertierung von YUV in RGB durch. Die EVR fügt den Mixer immer in die Videopipeline ein, unabhängig von der Anzahl der Eingabestreams oder dem Videoformat. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm, das den Verweisstream und den Unterstream zeigt, der auf den Mixer zeigt, der auf die Darstellung zeigt, die auf die Anzeige zeigt](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

Die Moderatorin führt die folgenden Aufgaben aus:

-   Legt das Ausgabeformat für den Mixer fest. Bevor das Streaming beginnt, legt die Moderatorin einen Medientyp für den Ausgabestream des Mixers fest. Dieser Medientyp definiert das Format des zusammengesetzten Bilds.
-   Erstellt das Direct3D-Gerät.
-   Ordnet Direct3D-Oberflächen zu. Der Mixer blitt die zusammengesetzten Frames auf diese Oberflächen.
-   Ruft die Ausgabe des Mixers ab.
-   Zeitpläne, wenn die Frames angezeigt werden. Die EVR stellt die Präsentationsuhr bereit, und der Moderator plant Frames entsprechend dieser Uhr.
-   Stellt jeden Frame mit Direct3D dar.
-   Führt die Einzelschritt- und Bereinigungsschritte des Frames aus.

### <a name="presenter-states"></a>Presenter States

Der Presenter befindet sich jederzeit in einem der folgenden Zustände:

-   *Gestartet.* Die Präsentationsuhr der EVR wird ausgeführt. Die Moderatorin plant Videoframes für die Präsentation, sobald sie eintreffen.
-   *Angehalten.* Die Präsentationsuhr wird angehalten. Der Presenter stellt keine neuen Beispiele vor, behält aber seine Warteschlange mit geplanten Stichproben bei. Wenn neue Beispiele empfangen werden, fügt die Moderatorin sie der Warteschlange hinzu.
-   *Stopped*(Beendet): Dies ist der anfängliche Status des Kanals nach seiner Erstellung (es sei denn, im Portal wurde das automatische Starten gewählt). Die Präsentationsuhr wird beendet. Die Präsentation verwirft alle geplanten Beispiele.
-   *Fahren Sie herunter.* Die Präsentation gibt alle Ressourcen frei, die sich auf das Streaming beziehen, z. B. Direct3D-Oberflächen. Dies ist der Anfangszustand des Moderators und der endgültige Zustand, bevor der Presenter zerstört wird.

Im Beispielcode in diesem Thema wird der Darstellungszustand durch eine -Enumeration dargestellt:


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Einige Vorgänge sind ungültig, während sich die Darstellung im Zustand "Herunterfahren" befindet. Der Beispielcode überprüft diesen Zustand, indem eine Hilfsmethode aufgerufen wird:


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a>Presenter-Schnittstellen

Ein Presenter ist erforderlich, um die folgenden Schnittstellen zu implementieren:



| Schnittstelle                                                                | Beschreibung                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ÜBER DIE UHRClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Benachrichtigt den Moderator, wenn sich der Zustand der EVR-Uhr ändert. Weitere Informationen finden Sie unter [Implementieren von IMPLEMENTClockStateSink.](#implementing-imfclockstatesink)                                   |
| [**ÜBER DIE NSDGET-DIENST**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Bietet der Anwendung und anderen Komponenten in der Pipeline eine Möglichkeit, Schnittstellen vom Präsentieren zu erhalten.                                                       |
| [**TOPOLOGYServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Ermöglicht es der Moderatorin, Schnittstellen aus der EVR oder dem Mixer zu erhalten. Weitere Informationen [finden Sie unter ImplementingTOPOLOGYTopologyServiceLookupClient (Implementieren vonTOPOLOGYTopologyServiceLookupClient).](#implementing-imftopologyservicelookupclient) |
| [**BESENVIDEODeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden. Weitere Informationen [finden Sie unter ImplementingUNGVIDEODeviceID](#implementing-imfvideodeviceid).                          |
| [**VERERBUNGVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Verarbeitet Nachrichten vom EVR. Weitere Informationen [finden Sie unter Implementieren vonPRESENTVideoPresenter](#implementing-imfvideopresenter).                                                             |



 

Die folgenden Schnittstellen sind optional:



| Schnittstelle                                                | Beschreibung                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Ermöglicht es dem Moderator, mit geschützten Medien zu arbeiten. Implementieren Sie diese Schnittstelle, wenn ihr Presenter eine vertrauenswürdige Komponente ist, die für die Arbeit im geschützten Medienpfad (PMP) konzipiert ist. |
| [**VERRATRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Gibt den Bereich der Wiedergaberaten an, die der Presenter unterstützt. Weitere Informationen [finden Sie unter Implementieren von DURCHSTRateSupport.](#implementing-imfratesupport)                                         |
| [**CITRIXVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Ordnet Koordinaten auf dem Ausgabevideoframe Koordinaten auf dem Eingabevideoframe zu.                                                                                       |
| [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Meldet Leistungsinformationen. Der EVR verwendet diese Informationen für die Verwaltung der Qualitätskontrolle. Diese Schnittstelle ist im DirectShow SDK dokumentiert.                        |



 

Sie können auch Schnittstellen für die Anwendung bereitstellen, um mit dem Moderator zu kommunizieren. Die Standard-Moderatorin implementiert zu diesem Zweck [**die BENUTZEROBERFLÄCHEVideoDisplayControl-Schnittstelle.**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) Sie können diese Schnittstelle implementieren oder eine eigene definieren. Die Anwendung ruft Schnittstellen aus dem Presenter ab, indem [**sie AUFTGETService::GetService in**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) der EVR aufruft. Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, übergibt der EVR die **GetService-Anforderung** an den Moderator.

### <a name="implementing-imfvideodeviceid"></a>Implementieren von NNTVideoDeviceID

Die [**BENUTZEROBERFLÄCHEVideoDeviceID-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) enthält eine Methode, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)die eine Geräte-GUID zurückgibt. Die Geräte-GUID stellt sicher, dass der Moderator und der Mixer kompatible Technologien verwenden. Wenn die Geräte-GUIDs nicht übereinstimmen, kann die EVR nicht initialisiert werden.

Sowohl der Standardmixer als auch der Presenter verwenden Direct3D 9, und die Geräte-GUID entspricht **IID_IDirect3DDevice9.** Wenn Sie Ihre benutzerdefinierte Präsentation mit dem Standardmixer verwenden möchten, muss die Geräte-GUID des Moderators **IID_IDirect3DDevice9.** Wenn Sie beide Komponenten ersetzen, können Sie eine neue Geräte-GUID definieren. Im weiteren Verlauf dieses Artikels wird davon ausgegangen, dass der Moderator Direct3D 9 verwendet. Hier ist die Standardimplementierung [**von GetDeviceID:**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



Die Methode sollte auch dann erfolgreich sein, wenn der Presenter heruntergefahren wird.

### <a name="implementing-imftopologyservicelookupclient"></a>Implementieren vonTOPOLOGYTopologyServiceLookupClient

Die [**SCHNITTSTELLETOPOLOGYTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) ermöglicht es dem Moderator, Schnittstellenzeiger wie folgt vom EVR und vom Mixer zu erhalten:

1.  Wenn der EVR den Presenter initialisiert, ruft er [**dieTOPOLOGYTopologyServiceLookupClient::InitServicePointers-Methode**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) des Presenters auf. Das -Argument ist ein Zeiger auf [**dieTOPOLOGYServiceLookup-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) des EVR.
2.  Die Moderatorin ruft [**DENTOPOLOGYServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) auf, um Schnittstellenzeiger entweder vom EVR oder vom Mixer zu erhalten.

Die [**LookupService-Methode**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ähnelt der [**METHODE "GEGETService::GetService".**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Beide Methoden nehmen eine Dienst-GUID und eine Schnittstellen-ID (IID) als Eingabe an, **lookupService** gibt jedoch ein Array von Schnittstellenzeigern zurück, während **GetService** einen einzelnen Zeiger zurückgibt. In der Praxis können Sie die Arraygröße jedoch immer auf 1 festlegen. Das abgefragte Objekt hängt von der Dienst-GUID ab:

-   Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, wird die EVR abgefragt.
-   Wenn die Dienst-GUID **MR_VIDEO_MIXER_SERVICE** ist, wird der Mixer abgefragt.

Verwenden Sie in Ihrer [**Implementierung von InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)die folgenden Schnittstellen aus der EVR:



| EVR-Schnittstelle                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Bietet dem Moderator eine Möglichkeit, Nachrichten an die EVR zu senden. Diese Schnittstelle wird im DirectShow SDK definiert, sodass die Nachrichten dem Muster für DirectShow-Ereignisse folgen, nicht Media Foundation Ereignisse.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DEADClock**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Stellt die Uhr des EVR dar. Die Präsentation verwendet diese Schnittstelle, um Beispiele für die Präsentation zu planen. Die EVR kann ohne Uhr ausgeführt werden, sodass diese Schnittstelle möglicherweise nicht verfügbar ist. Wenn nicht, ignorieren Sie den Fehlercode aus [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).<br/> Die Uhr implementiert auch die [**BENUTZEROBERFLÄCHETimer-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) In der Media Foundation implementiert die Uhr die [**BERPresentationClock-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) Diese Schnittstelle wird in DirectShow nicht implementiert.<br/> |



 

Erhalten Sie die folgenden Schnittstellen aus dem Mixer:



| Mixerschnittstelle                              | Beschreibung                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Ermöglicht dem Moderator die Kommunikation mit dem Mixer.       |
| [**BESENVIDEODeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Ermöglicht es dem Moderator, die Geräte-GUID des Mixers zu überprüfen. |



 

Der folgende Code implementiert die [**InitServicePointers-Methode:**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Wenn die von [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) erhaltenen Schnittstellenzeigen nicht mehr gültig sind, ruft der EVR [**DEN TOPOLOGIEdienstLookupClient::ReleaseServicePointers auf.**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) Geben Sie in dieser Methode alle Schnittstellenzeiger frei, und legen Sie den Presenter-Zustand auf "Herunterfahren" fest:


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



Der EVR ruft [**ReleaseServicePointers aus**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) verschiedenen Gründen auf, z. B.:

-   Trennen oder Erneutes Verbinden von Pins (DirectShow) oder Hinzufügen oder Entfernen von Streamsenken (Media Foundation).
-   Ändern des Formats.
-   Festlegen einer neuen Uhr.
-   Endgültiges Herunterfahren der EVR.

Während der Lebensdauer des Moderators kann der EVR [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) und [**ReleaseServicePointers mehrmals**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) aufrufen.

### <a name="implementing-imfvideopresenter"></a>Implementieren vonPRESENTVideoPresenter

Die [**BERDVideoPresenter-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) erbt [**DENTLOCKStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) und fügt zwei Methoden hinzu:



| Methode                                                               | Beschreibung                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Gibt den Medientyp der zusammengesetzten Videoframes zurück. |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Signalisiert dem Moderator, verschiedene Aktionen durchzuführen.      |



 

Die [**GetCurrentMediaType-Methode**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) gibt den Medientyp des Presenters zurück. (Weitere Informationen zum Festlegen des Medientyps finden Sie unter [Aushandeln von Formaten.)](#negotiating-formats) Der Medientyp wird als [**INTERFACEMediaType-Schnittstellenzeiger VOM TYP 1**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) zurückgegeben. Im folgenden Beispiel wird davon ausgegangen, dass der Presenter den Medientyp als [**EINFMediaType-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) speichert. Rufen Sie QueryInterface auf, um die **BENUTZEROBERFLÄCHEVideoMediaType-Schnittstelle** vom **Medientyp zu erhalten:**


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Die [**ProcessMessage-Methode**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) ist der primäre Mechanismus, mit dem die EVR mit dem Moderator kommunizieren kann. Die folgenden Meldungen werden definiert. Die Details zur Implementierung der einzelnen Nachrichten finden Sie im weiteren Verlauf dieses Themas.



| `Message`                                | BESCHREIBUNG                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | Der Ausgabemedientyp des Mixers ist ungültig. Der Moderator sollte einen neuen Medientyp mit dem Mixer aushandeln. Weitere Informationen [finden Sie unter Aushandeln von Formaten.](#negotiating-formats)                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | Das Streaming wurde gestartet. Für diese Nachricht ist keine bestimmte Aktion erforderlich, aber Sie können sie zum Zuordnen von Ressourcen verwenden.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | Das Streaming wurde beendet. Geben Sie alle Ressourcen frei, die Sie als Reaktion auf die **MFVP_MESSAGE_BEGINSTREAMING** zugeordnet haben.                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | Der Mixer hat ein neues Eingabebeispiel erhalten und kann möglicherweise einen neuen Ausgaberahmen generieren. Der Presenter sollte [**IMTRANSFORM::P rocessOutput für**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) den Mixer aufrufen. Weitere Informationen finden [Sie unter Verarbeiten der Ausgabe](#processing-output). |
| **MFVP_MESSAGE_ENDOFSTREAM**         | Die Präsentation wurde beendet. Weitere Informationen [finden Sie unter Ende des Datenstroms.](#end-of-stream)                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | Der EVR leert die Daten in seiner Renderingpipeline. Der Moderator sollte alle Videoframes verwerfen, die für die Präsentation geplant sind.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Fordert den Moderator an, N Frames schrittweise vorwärts zu bringen. Der Moderator sollte die nächsten N-1 Frames verwerfen und den N. Frame anzeigen. Weitere Informationen finden [Sie unter Frame Stepping (Frameschritt).](#frame-stepping)                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Bricht frame stepping ab.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Implementieren von DEADClockStateSink

Der Präsentationser muss im Rahmen seiner Implementierung von [**VORZEIGERVideoPresenter,**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)der **DEN NAMEN ZUNEClockStateSink erbt, die INTERFACEClockStateSink-Schnittstelle implementieren.** [](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) Die EVR verwendet diese Schnittstelle, um den Moderator zu benachrichtigen, wenn sich der Status der EVR-Uhr ändert. Weitere Informationen zu den Uhrzuständen finden Sie unter [Presentation Clock](presentation-clock.md).

Hier sind einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle. Alle Methoden sollten fehlschlagen, wenn der Presenter heruntergefahren wird.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></td>
<td><ol>
<li>Legen Sie den Presenterzustand auf Gestartet fest.</li>
<li>Wenn <em>llClockStartOffset</em> nicht <strong>PRESENTATION_CURRENT_POSITION</strong>ist, leeren Sie die Warteschlange der Beispiele des Moderators. (Dies entspricht dem Empfangen <strong>einer</strong> MFVP_MESSAGE_FLUSH Nachricht.)</li>
<li>Wenn eine vorherige Frameschrittanforderung noch aussteht, verarbeiten Sie die Anforderung (siehe <a href="#frame-stepping">Frame Stepping</a>). Versuchen Sie andernfalls, die Ausgabe des Mixers zu verarbeiten (siehe <a href="#processing-output">Verarbeiten der Ausgabe</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></td>
<td><ol>
<li>Legen Sie den Presenterzustand auf Beendet fest.</li>
<li>Leeren Sie die Warteschlange der Warteschlange der Beispiele des Moderators.</li>
<li>Brechen Sie alle ausstehenden Frameschritt-Operation ab.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></td>
<td>Legen Sie den Presenterzustand auf angehalten fest.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></td>
<td>Behandeln Sie dasselbe wie <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart,</strong></a> aber leeren Sie die Warteschlange der Beispiele nicht.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></td>
<td><ol>
<li>Wenn die Rate von null in ungleich 0 (null) geändert wird, brechen Sie frame stepping ab.</li>
<li>Speichern Sie die neue Taktrate. Die Taktrate wirkt sich darauf aus, wenn Stichproben dargestellt werden. Weitere Informationen finden Sie unter <a href="#scheduling-samples">Zeitplanungsbeispiele.</a></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>Implementieren vonTRATERateSupport

Um andere Wiedergaberaten als 1× zu unterstützen, muss die Moderatorin die [**BERATERateSupport-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) implementieren. Hier sind einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle. Alle Methoden sollten fehlschlagen, nachdem der Presenter heruntergefahren wurde. Weitere Informationen zu dieser Schnittstelle finden Sie unter [Rate Control](rate-control.md).



| Wert                                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Gibt 0 (null) zurück, um keine minimale Wiedergaberate anzugeben.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | Bei nicht schlanker Wiedergabe sollte die Wiedergaberate die Aktualisierungsrate des Monitors nicht *überschreiten:* maximale Aktualisierungsrate  =   (Hz) */Videobildrate* (FPS). Die Videobildrate wird im Medientyp des Moderators angegeben. <br/> Bei der schlanken Wiedergabe ist die Wiedergaberate ungebunden. gibt den Wert **FLT_MAX.** In der Praxis sind die Quelle und der Decoder die begrenzenden Faktoren bei der schlanken Wiedergabe. <br/> Geben Sie für die umgekehrte Wiedergabe den negativen Wert der maximalen Rate zurück.<br/> |
| [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Gibt **MF_E_UNSUPPORTED_RATE** zurück, wenn der absolute Wert *von flRate* die maximale Wiedergaberate des Moderators überschreitet. Berechnen Sie die maximale Wiedergaberate wie für [**GetFastestRate beschrieben.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)                                                                                                                                                                                                                                                                                    |



 

Das folgende Beispiel zeigt, wie die [**GetFastestRate-Methode implementiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) wird:


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



Im vorherigen Beispiel wird die Hilfsmethode GetMaxRate zum Berechnen der maximalen Vorwärtswiedergaberate aufruft:

Das folgende Beispiel zeigt, wie die [**IsRateSupported-Methode implementiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) wird:


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a>Senden von Ereignissen an die EVR

Der Moderator muss den EVR über verschiedene Ereignisse benachrichtigen. Zu diesem Zwecke wird die [**IMediaEventSink-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) des EVR verwendet, die beim Aufrufen der [**METHODETOPOLOGYServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) des Moderators durch den EVR ermittelt wird. (Die **IMediaEventSink-Schnittstelle** ist ursprünglich eine DirectShow-Schnittstelle, wird jedoch sowohl im DirectShow EVR als auch im Media Foundation.) Der folgende Code zeigt, wie sie ein Ereignis an die EVR senden:


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



In der folgenden Tabelle sind die ereignisse aufgeführt, die der Moderator zusammen mit den Ereignisparametern sendet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ereignis</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>Der Moderator hat das Rendern aller Frames nach der MFVP_MESSAGE_ENDOFSTREAM abgeschlossen.<br/>
<ul>
<li><em>Param1:</em>HRESULT, das den Status des Vorgangs angibt.</li>
<li><em>Param2:</em>Nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#end-of-stream">Ende des Streams.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>Das Direct3D-Gerät wurde geändert.<br/>
<ul>
<li><em>Param1:</em>Nicht verwendet.</li>
<li><em>Param2:</em>Nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#managing-the-direct3d-device">Verwalten des Direct3D-Geräts.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>Es ist ein Fehler aufgetreten, der das Beenden des Streamings erfordert.<br/>
<ul>
<li><em>Param1</em>: <strong>HRESULT gibt</strong> den aufgetretenen Fehler an.</li>
<li><em>Param2:</em>Nicht verwendet.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>Gibt die Zeit an, die der Presenter zum Rendern der einzelnen Frames in Zeit nimmt. (Optional.)<br/>
<ul>
<li><em>Param1:</em>Zeiger auf einen konstanten <strong>LONGLONG-Wert,</strong> der die Zeit zum Verarbeiten des Frames in Einheiten von 100 Nanosekunden enthält.</li>
<li><em>Param2:</em>Nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#processing-output">Verarbeiten der Ausgabe</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>Gibt die aktuelle Verzögerungszeit in Renderingbeispielen an. Wenn der Wert positiv ist, liegen die Stichproben hinter dem Zeitplan. Wenn der Wert negativ ist, liegen die Stichproben dem Zeitplan voraus. (Optional.)<br/>
<ul>
<li><em>Param1:</em>Zeiger auf einen konstanten <strong>LONGLONG-Wert,</strong> der die Verzögerungszeit in Einheiten von 100 Nanosekunden enthält.</li>
<li><em>Param2:</em>Nicht verwendet.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>Wird unmittelbar <strong>nach</strong> EC_STEP_COMPLETE gesendet, wenn die Wiedergaberate 0 (null) ist. Dieses Ereignis enthält den Zeitstempel des angezeigten Frames.<br/>
<ul>
<li><em>Param1:</em>Niedrigere 32 Bits des Zeitstempels.</li>
<li><em>Param2:</em>Obere 32 Bits des Zeitstempels.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Stepping</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>Der Presenter hat einen Frameschritt abgeschlossen oder abgebrochen.<br/>
<ul>
<li><em>Param1:</em>Nicht verwendet.</li>
<li><em>Param2:</em>Nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Stepping</a>.<br/>
<blockquote>
[!Note]<br />
In einer früheren Version der Dokumentation wurde <em>Param1 falsch</em> beschrieben. Dieser Parameter wird für dieses Ereignis nicht verwendet.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>Aushandeln von Formaten

Wenn der Moderator eine **MFVP_MESSAGE_INVALIDATEMEDIATYPE** evr empfängt, muss er das Ausgabeformat für den Mixer wie folgt festlegen:

1.  Rufen [**Sie IMTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) für den Mixer auf, um einen möglichen Ausgabetyp zu erhalten. Dieser Typ beschreibt ein Format, das der Mixer mit den Eingabestreams und den Videoverarbeitungsfunktionen des Grafikgeräts erzeugen kann.
2.  Überprüfen Sie, ob der Presenter diesen Medientyp als Renderingformat verwenden kann. Hier sind einige Dinge zu überprüfen, obwohl Ihre Implementierung möglicherweise eigene Anforderungen hat:

    -   Das Video muss unkomprimiert sein.
    -   Das Video darf nur progressive Frames haben. Überprüfen Sie, [**ob MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) Attribut gleich **MFVideoInterlace_Progressive.**
    -   Das Format muss mit dem Direct3D-Gerät kompatibel sein.

    Wenn der Typ nicht akzeptabel ist, kehren Sie zu Schritt 1 zurück, und erhalten Sie den nächsten vorgeschlagenen Typ des Mixers.

3.  Erstellen Sie einen neuen Medientyp, der ein Klon des ursprünglichen Typs ist, und ändern Sie dann die folgenden Attribute:

    -   Legen Sie [**MF_MT_FRAME_SIZE-Attribut**](mf-mt-frame-size-attribute.md) auf die Breite und Höhe fest, die Sie für die Direct3D-Oberflächen verwenden möchten, die Sie zuordnen möchten.
    -   Legen Sie das [**MF_MT_PAN_SCAN_ENABLED-Attribut**](mf-mt-pan-scan-enabled-attribute.md) auf **FALSE fest.**
    -   Legen Sie [**MF_MT_PIXEL_ASPECT_RATIO-Attribut**](mf-mt-pixel-aspect-ratio-attribute.md) auf den PAR-Wert der Anzeige fest (in der Regel 1:1).
    -   Legen Sie die[](mf-mt-geometric-aperture-attribute.md) geometrische Öffnung ( MF_MT_GEOMETRIC_APERTURE-Attribut) auf ein Rechteck innerhalb der Direct3D-Oberfläche fest. Wenn der Mixer einen Ausgaberahmen generiert, schneide er das Quellbild auf dieses Rechteck. Die geometrische Öffnung kann so groß wie die Oberfläche sein, oder es kann sich um ein Unterrektgle innerhalb der Oberfläche befinden. Weitere Informationen finden Sie unter [Quell- und Zielrechtecke.](#source-and-destination-rectangles)

4.  Um zu testen, ob der Mixer den geänderten Ausgabetyp akzeptiert, rufen Sie [**DIETRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) mit dem MFT_SET_TYPE_TEST_ONLY **auf.** Wenn der Mixer den Typ ablehnt, wechseln Sie zurück zu Schritt 1, und erhalten Sie den nächsten Typ.
5.  Ordnen Sie einen Pool von Direct3D-Oberflächen zu, wie unter [Zuordnen von Direct3D-Oberflächen beschrieben.](#allocating-direct3d-surfaces) Der Mixer verwendet diese Oberflächen, wenn er die zusammengesetzten Videoframes zeichnet.
6.  Legen Sie den Ausgabetyp für den Mixer fest, indem [**Sie SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) ohne Flags aufrufen. Wenn der erste Aufruf von **SetOutputType** in Schritt 4 erfolgreich war, sollte die Methode erneut erfolgreich sein.

Wenn die Typen des Mixers nicht mehr vorhanden sind, gibt die [**GetOutputAvailableType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) MF_E_NO_MORE_TYPES. Wenn der Moderator keinen geeigneten Ausgabetyp für den Mixer finden kann, kann der Stream nicht gerendert werden. In diesem Fall können DirectShow oder Media Foundation ein anderes Streamformat ausprobieren. Daher kann der Moderator mehrere Nachrichten MFVP_MESSAGE_INVALIDATEMEDIATYPE **in** einer Zeile empfangen, bis ein gültiger Typ gefunden wird.

Der Mixer postiert das Video automatisch und berücksichtigt dabei das Pixel-Seitenverhältnis (PAR) der Quelle und des Ziels. Um optimale Ergebnisse zu erzielen, sollten die Breite und Höhe der Oberfläche und die geometrische Öffnung der tatsächlichen Größe des Videos auf der Anzeige entspricht. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm, das einen zusammengesetzten Fram zeigt, der zu einer direct3d-Oberfläche führt, die zu einem Fenster führt](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

Der folgende Code zeigt die Gliederung des Prozesses. Einige der Schritte werden in Hilfsfunktionen platziert, deren genaue Details von den Anforderungen Ihrer Moderatorin abhängen.


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



Weitere Informationen zu Videomedientypen finden Sie unter [Videomedientypen.](video-media-types.md)

## <a name="managing-the-direct3d-device"></a>Verwalten des Direct3D-Geräts

Der Moderator erstellt das Direct3D-Gerät und behandelt jeglichen Geräteverlust während des Streamings. Der Presenter hostet auch den Direct3D-Geräte-Manager, der anderen Komponenten die Verwendung desselben Geräts ermöglicht. Der Mixer verwendet z. B. das Direct3D-Gerät, um Unterstreams zu mischen, zu deinterketten und Farbanpassungen durchzuführen. Decoder können das Direct3D-Gerät für die videobeschleunigte Decodierung verwenden. (Weitere Informationen zur Videobeschleunigung finden Sie unter [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).)

Führen Sie zum Einrichten des Direct3D-Geräts die folgenden Schritte aus:

1.  Erstellen Sie das Direct3D-Objekt, indem Sie **Direct3DCreate9** oder **Direct3DCreate9Ex aufrufen.**
2.  Erstellen Sie das Gerät, indem Sie **IDirect3D9::CreateDevice** oder **IDirect3D9Ex::CreateDevice aufrufen.**
3.  Erstellen Sie den Geräte-Manager, indem Sie [**DXVA2CreateDirect3DDeviceManager9 aufrufen.**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)
4.  Legen Sie das Gerät auf dem Geräte-Manager fest, indem [**Sie IDirect3DDeviceManager9::ResetDevice aufrufen.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)

Wenn eine andere Pipelinekomponente den Geräte-Manager benötigt, ruft sie AUF DER  EVR [**DEN DIENSTGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf und gibt MR_VIDEO_ACCELERATION_SERVICE für die Dienst-GUID an. Der EVR übergibt die Anforderung an den Moderator. Nachdem das Objekt den [**IDirect3DDeviceManager9-Zeiger**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) erhalten hat, kann es ein Handle für das Gerät erhalten, indem [**es IDirect3DDeviceManager9::OpenDeviceHandle aufruft.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) Wenn das Objekt das Gerät verwenden muss, übergibt es das Gerätehandchen an die [**IDirect3DDeviceManager9::LockDevice-Methode,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) die einen **IDirect3DDevice9-Zeiger** zurückgibt.

Wenn der Moderator nach der Geräteeinrichtung das Gerät zerstört und ein neues erstellt, muss er [**ResetDevice erneut**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) aufrufen. Die **ResetDevice-Methode** macht alle vorhandenen Gerätehandles ungültig, wodurch [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE.** Dieser Fehlercode signalisiert anderen Objekten, die das Gerät verwenden, dass sie ein neues Gerätehand handle öffnen sollten. Weitere Informationen zur Verwendung des Geräte-Managers finden Sie unter [Direct3D Geräte-Manager](direct3d-device-manager.md).

Der Moderator kann das Gerät im Fenstermodus oder im exklusiven Vollbildmodus erstellen. Für den Fenstermodus sollten Sie der Anwendung eine Möglichkeit bieten, das Videofenster anzugeben. Die Standard-Moderatorin implementiert zu diesem Zweck [**die METHODE DURCHEVIDEODisplayControl::SetVideoWindow.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) Sie müssen das Gerät erstellen, wenn die Präsentation zum ersten Mal erstellt wird. In der Regel kennen Sie derzeit nicht alle Geräteparameter, z. B. das Fenster oder das Format des Hintergrundpuffers. Sie können ein temporäres Gerät erstellen und später durch&ersetzen. Denken Sie daran, \# [**ResetDevice im**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) Geräte-Manager aufzurufen.

Wenn Sie ein neues Gerät erstellen oder **IDirect3DDevice9::Reset** oder **IDirect3DDevice9Ex::ResetEx** auf einem vorhandenen Gerät aufrufen, senden Sie ein [**EC_DISPLAY_CHANGED-Ereignis an**](../directshow/ec-display-changed.md) die EVR. Dieses Ereignis benachrichtigt den EVR, den Medientyp erneut zu ausgehandelt. Der EVR ignoriert die Ereignisparameter für dieses Ereignis.

### <a name="allocating-direct3d-surfaces"></a>Zuordnen von Direct3D-Oberflächen

Nachdem der Moderator den Medientyp definiert hat, kann er die Direct3D-Oberflächen zuordnen, die der Mixer zum Schreiben der Videoframes verwendet. Die Oberfläche muss mit dem Medientyp des Moderators übereinstimmen:

-   Das Oberflächenformat muss mit dem Medienuntertyp übereinstimmen. Wenn der Untertyp beispielsweise MFVideoFormat_RGB24 **ist,** muss das Oberflächenformat **D3DFMT_X8R8G8B8.** Weitere Informationen zu Untertypen und Direct3D-Formaten finden Sie unter [Video Subtype GUIDs](video-subtype-guids.md).
-   Die Breite und Höhe der Oberfläche muss mit den Dimensionen übereinstimmen, die im [**MF_MT_FRAME_SIZE-Attribut**](mf-mt-frame-size-attribute.md) des Medientyps angegeben sind.

Die empfohlene Methode zum Zuordnen von Oberflächen hängt davon ab, ob die Präsentation im Fenstermodus oder im Vollbildmodus ausgeführt wird.

Wenn für das Direct3D-Gerät ein Fenster angezeigt wird, können Sie mehrere Swapketten mit jeweils einem einzelnen Hintergrundpuffer erstellen. Bei diesem Ansatz können Sie jede Oberfläche unabhängig voneinander präsentieren, da die Präsentation einer Auslagerungskette die anderen Austauschketten nicht beeinträchtigt. Der Mixer kann Daten auf eine Oberfläche schreiben, während eine andere Oberfläche für die Präsentation geplant ist.

Entscheiden Sie zunächst, wie viele Swapketten erstellt werden. Es werden mindestens drei empfohlen. Führen Sie für jede Auslagerungskette folgende Schritte aus:

1.  Rufen **Sie IDirect3DDevice9::CreateAdditionalSwapChain** auf, um die Swapkette zu erstellen.
2.  Rufen **Sie IDirect3DSwapChain9::GetBackBuffer** auf, um einen Zeiger auf die Hintergrundpufferoberfläche der Austauschkette zu erhalten.
3.  Rufen [**Sie MFCreateVideoSampleFromSurface auf,**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) und übergeben Sie einen Zeiger auf die Oberfläche. Diese Funktion gibt einen Zeiger auf ein Videobeispielobjekt zurück. Das Videobeispielobjekt implementiert die [**METHODESAMPLE-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) und der Moderator verwendet diese Schnittstelle, um die Oberfläche an den Mixer zu übertragen, wenn der Moderator die [**METHODE "VORZEIGETransform::P rocessOutput"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers aufruft. Weitere Informationen zum Videobeispielobjekt finden Sie unter [Videobeispiele.](video-samples.md)
4.  Speichern Sie [**den WARTESCHLANGENsample-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in einer Warteschlange. Der Presenter pullt Während der Verarbeitung Stichproben aus dieser Warteschlange, wie unter [Processing Output (Verarbeiten der Ausgabe) beschrieben.](#processing-output)
5.  Behalten Sie einen Verweis auf den **IDirect3DSwapChain9-Zeiger** bei, damit die Swapkette nicht freigegeben wird.

Im exklusiven Vollbildmodus kann das Gerät nicht mehr als eine Auslagerungskette haben. Diese Swapkette wird implizit erstellt, wenn Sie das Vollbildgerät erstellen. Die Auslagerungskette kann mehr als einen Hintergrundpuffer haben. Wenn Sie jedoch einen Hintergrundpuffer präsentieren, während Sie in einen anderen Hintergrundpuffer in derselben Swapkette schreiben, gibt es keine einfache Möglichkeit, die beiden Vorgänge zu koordinieren. Dies liegt an der Art und Weise, wie Direct3D Das Spiegeln von Oberflächen implementiert. Wenn Sie Present aufrufen, aktualisiert der Grafiktreiber die Surface-Zeiger im Grafikspeicher. Wenn Sie beim Aufrufen von **Present** **IDirect3DSurface9-Zeiger** halten, zeigen diese auf verschiedene Puffer, nachdem der **Present-Aufruf** zurückgegeben wurde.

Die einfachste Möglichkeit besteht in der Erstellung eines Videobeispiels für die Austauschkette. Wenn Sie diese Option auswählen, führen Sie die gleichen Schritte wie für den Fenstermodus aus. Der einzige Unterschied ist, dass die Beispielwarteschlange ein einzelnes Videobeispiel enthält. Eine weitere Möglichkeit ist das Erstellen von Offscreenoberflächen und das anschließende Aufschneiden in den Hintergrundpuffer. Die von Ihnen erstellten Oberflächen müssen die [**IDirectXVideoProcessor::VideoProcessBlt-Methode**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) unterstützen, die der Mixer zum Zusammenstellen der Ausgabeframes verwendet.

### <a name="tracking-samples"></a>Überwachungsbeispiele

Wenn die Moderatorin die Videobeispiele zum ersten Mal zuteilen, werden sie in eine Warteschlange gestellt. Der Presenter zeichnet immer dann aus dieser Warteschlange, wenn er einen neuen Frame aus dem Mixer erhalten muss. Nachdem der Mixer den Frame ausgegeben hat, verschiebt der Moderator das Beispiel in eine zweite Warteschlange. Die zweite Warteschlange ist für Beispiele vorgesehen, die auf ihre geplanten Präsentationszeiten warten.

Um das Nachverfolgen des Status der einzelnen Stichproben zu vereinfachen, implementiert das Videobeispielobjekt die [**BENUTZEROBERFLÄCHETRACKedSample-Schnittstelle.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) Sie können diese Schnittstelle wie folgt verwenden:

1.  Implementieren Sie [**dieASYNCCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) in Ihrer Präsentation.
2.  Bevor Sie ein Beispiel in der geplanten Warteschlange platzieren, fragen Sie das Videobeispielobjekt für die [**BENUTZEROBERFLÄCHENTtrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab.

3.  Rufen Sie MIT EINEM Zeiger auf Ihre Rückrufschnittstelle [**DEN CALLTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) auf.
4.  Wenn das Beispiel zur Präsentation bereit ist, entfernen Sie es aus der geplanten Warteschlange, stellen Sie es vor, und geben Sie alle Verweise auf das Beispiel frei.
5.  Im Beispiel wird der Rückruf aufgerufen. (Das Beispielobjekt wird in diesem Fall nicht gelöscht, da es einen Verweiszähler für sich selbst enthält, bis der Rückruf aufgerufen wird.)
6.  Geben Sie innerhalb des Rückrufs das Beispiel an die verfügbare Warteschlange zurück.

Eine Moderatorin ist nicht erforderlich, um [**MITTTTrackedSample Beispiele**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) nachverfolgungen zu können. Sie können jede Technik implementieren, die für Ihren Entwurf am besten funktioniert. Ein Vorteil von **RENDERTrackedSample** ist, dass Sie die Planungs- und Renderingfunktionen des Moderators in Hilfsobjekte verschieben können, und diese Objekte benötigen keinen speziellen Mechanismus zum Aufrufen zurück an den Moderator, wenn sie Videobeispiele veröffentlichen, da das Beispielobjekt diesen Mechanismus bietet.

Der folgende Code zeigt, wie der Rückruf festgelegt wird:


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



Rufen Sie im Rückruf [**DIEASYNCResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) für das asynchrone Ergebnisobjekt auf, um einen Zeiger auf das Beispiel abzurufen:


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a>Verarbeiten der Ausgabe

Wenn der Mixer ein neues Eingabebeispiel empfängt, sendet der EVR eine MFVP_MESSAGE_PROCESSINPUTNOTIFY **nachricht** an den Moderator. Diese Meldung gibt an, dass der Mixer möglicherweise über einen neuen Videoframe für die Bereitstellung verfügen kann. Als Antwort ruft die Moderatorin [**IM MIXERTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf. Wenn die Methode erfolgreich ist, wird das Beispiel von der Präsentation geplant.

Führen Sie die folgenden Schritte aus, um die Ausgabe des Mixers zu erhalten:

1.  Überprüfen Sie den Uhrzustand. Wenn die Uhr angehalten ist, ignorieren Sie die **MFVP_MESSAGE_PROCESSINPUTNOTIFY,** es sei denn, dies ist der erste Videoframe. Wenn die Uhr ausgeführt wird oder dies der erste Videoframe ist, fahren Sie fort.
2.  Hier finden Sie ein Beispiel aus der Warteschlange der verfügbaren Beispiele. Wenn die Warteschlange leer ist, bedeutet dies, dass derzeit alle zugeordneten Stichproben für die Präsentation geplant sind. Ignorieren Sie in diesem Fall **die MFVP_MESSAGE_PROCESSINPUTNOTIFY** Nachricht. Wenn das nächste Beispiel verfügbar ist, wiederholen Sie die hier aufgeführten Schritte.
3.  (Optional.) Wenn die Uhr verfügbar ist, rufen Sie die aktuelle Uhrzeit (*T1*) ab, indem [**Sie DENKlock::GetCorrelatedTime aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)
4.  Rufen [**Sie IM MIXERTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf. Wenn **ProcessOutput erfolgreich** ist, enthält das Beispiel einen Videoframe. Wenn bei der Methode ein Fehler auftritt, überprüfen Sie den Rückgabecode. Die folgenden Fehlercodes aus **ProcessOutput** sind keine kritischen Fehler:

    

    | Fehlercode                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | Der Mixer benötigt mehr Eingaben, bevor er einen neuen Ausgaberahmen erzeugen kann.<br/> Wenn Sie diesen Fehlercode erhalten, überprüfen Sie, ob die EVR das Ende des Streams erreicht hat, und antworten Sie entsprechend, wie unter [Ende des Streams beschrieben.](#end-of-stream) Ignorieren Sie andernfalls **MF_E_TRANSFORM_NEED_MORE_INPUT** Meldung. Der EVR sendet eine weitere, wenn der Mixer mehr Eingaben erhält.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | Der Ausgabetyp des Mixers ist ungültig geworden, möglicherweise aufgrund einer Formatänderung im Upstream.<br/> Wenn Sie diesen Fehlercode erhalten, legen Sie den Medientyp des Presenters auf **NULL fest.** Der EVR fordert ein neues Format an.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | Der Mixer erfordert einen neuen Medientyp.<br/> Wenn Sie diesen Fehlercode erhalten, können Sie den Ausgabetyp des Mixers erneut aushandeln, wie unter [Aushandeln von Formaten beschrieben.](#negotiating-formats)<br/>                                                                                                                                                                                                        |

    

     

    Wenn [**ProcessOutput erfolgreich**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ist, fahren Sie fort.

5.  (Optional.) Wenn die Uhr verfügbar ist, erhalten Sie die aktuelle Uhrzeit (*T2*). Die vom Mixer eingeführte Latenzzeit beträgt (*T2*  -  *T1*). Senden Sie **EC_PROCESSING_LATENCY** Ereignis mit diesem Wert an die EVR. Der EVR verwendet diesen Wert für die Qualitätskontrolle. Wenn keine Uhr verfügbar ist, gibt es keinen Grund, das Ereignis **EC_PROCESSING_LATENCY** senden.
6.  (Optional.) Fragen Sie das Beispiel [**für DIETTTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab, und rufen Sie [**DANNTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) auf, wie unter [Tracking Samples (Nachverfolgungsbeispiele) beschrieben.](#tracking-samples)
7.  Planen Sie das Beispiel für die Präsentation.

Diese Sequenz von Schritten kann beendet werden, bevor der Moderator eine Ausgabe vom Mixer erhält. Um sicherzustellen, dass keine Anforderungen gelöscht werden, sollten Sie dieselben Schritte wiederholen, wenn Folgendes auftritt:

-   Die METHODE [**DER PRÄSENTATIONClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) oder **DERENTLOCKSTATESink::OnClockStart** wird aufgerufen. Dies behandelt den Fall, in dem der Mixer Eingaben ignoriert, da die Uhr angehalten wird (Schritt 1).
-   Der [**RÜCKRUFTrackedSample-Rückruf**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) wird aufgerufen. Dies behandelt den Fall, in dem der Mixer Eingaben empfängt, aber alle Videobeispiele des Moderators verwendet werden (Schritt 2).

Die nächsten Codebeispiele zeigen diese Schritte ausführlicher. Der Presenter ruft die -Methode auf (wie im folgenden Beispiel gezeigt), wenn sie die MFVP_MESSAGE_PROCESSINPUTNOTIFY `ProcessInputNotify` erhält. 


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



Diese `ProcessInputNotify` Methode legt ein boolesches Flag fest, um die Tatsache zu erfassen, dass der Mixer über eine neue Eingabe verfügt. Anschließend ruft sie die `ProcessOutputLoop` -Methode auf, die im nächsten Beispiel gezeigt wird. Diese Methode versucht, so viele Beispiele wie möglich aus dem Mixer zu pullen:


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



Die `ProcessOutput` -Methode, die im nächsten Beispiel gezeigt wird, versucht, einen einzelnen Videoframe aus dem Mixer zu erhalten. Wenn kein Videoframe verfügbar ist, gibt S_FALSE oder einen Fehlercode zurück, der die `ProcessSample` Schleife in `ProcessOutputLoop` unterbricht. Der Großteil der Arbeit erfolgt innerhalb der `ProcessOutput` -Methode:


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



Einige Hinweise zu diesem Beispiel:

-   Die *m_SamplePool* Variable wird als Sammlungsobjekt angenommen, das die Warteschlange der verfügbaren Videobeispiele enthält. Die -Methode des `GetSample` -Objekts gibt MF_E_SAMPLEALLOCATOR_EMPTY zurück, wenn  die Warteschlange leer ist.
-   Wenn die [**ProcessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers MF_E_TRANSFORM_NEED_MORE_INPUT zurückgibt, bedeutet dies, dass der Mixer keine weitere Ausgabe erzeugen kann, sodass der Moderator das m_fSampleNotify *wird.*
-   Die `TrackSample` -Methode, mit der der [**RÜCKRUF VON DURCHTTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) bestimmt wird, wird im Abschnitt Tracking Samples [(Nachverfolgungsbeispiele) gezeigt.](#tracking-samples)

### <a name="repainting-frames"></a>Neupaintieren von Frames

Gelegentlich muss der Moderator möglicherweise den neuesten Videoframe neu anpainten. Beispielsweise wird der Rahmen von der Standard-Moderatorin in den folgenden Situationen neu gepaint:

-   Im Fenstermodus als Reaktion auf **WM_PAINT,** die vom Fenster der Anwendung empfangen werden. Weitere [**Informationen finden Sie unter ATTRIBUTEVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   Wenn sich das Zielrechteck ändert, wenn die Anwendung [**DIEVIDEODisplayControl::SetVideoPosition aufruft.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)

Führen Sie die folgenden Schritte aus, um den Mixer an fordern, den neuesten Frame neu zu erstellen:

1.  Hier erhalten Sie ein Videobeispiel aus der Warteschlange.
2.  Fragen Sie das Beispiel für die [**BENUTZEROBERFLÄCHEDesiredSample-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) ab.
3.  Rufen [**Sie DANNDESiredSample::SetDesiredSampleTimeAndDuration auf.**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration) Geben Sie den Zeitstempel des letzten Videoframes an. (Sie müssen diesen Wert zwischenspeichern und für jeden Frame aktualisieren.)
4.  Rufen [**Sie ProcessOutput für**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) den Mixer auf.

Beim Neupaintieren eines Frames können Sie die Präsentationsuhr ignorieren und den Rahmen sofort präsentieren.

### <a name="scheduling-samples"></a>Zeitplanungsbeispiele

Videoframes können den EVR jederzeit erreichen. Der Presenter ist dafür verantwortlich, jeden Frame zum richtigen Zeitpunkt basierend auf dem Zeitstempel des Frames zu präsentieren. Wenn der Moderator ein neues Beispiel aus dem Mixer erhält, wird das Beispiel in die geplante Warteschlange eingereiht. In einem separaten Thread ruft der Moderator kontinuierlich das erste Beispiel vom Anfang der Warteschlange ab und bestimmt, ob Dies der Fall ist:

-   Stellen Sie das Beispiel vor.
-   Behalten Sie das Beispiel in der Warteschlange bei, da es früh ist.
-   Verwerfen Sie das Beispiel, da es zu spät ist. Obwohl Sie möglichst vermeiden sollten, Frames zu löschen, müssen Sie dies möglicherweise machen, wenn der Moderator ständig ins Rückstand geraten soll.

Um den Zeitstempel für einen Videoframe zu erhalten, rufen Sie [**IMTSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) im Videobeispiel auf. Der Zeitstempel ist relativ zur Präsentationsuhr des EVR. Um die aktuelle Uhrzeit zu erhalten, rufen [**Sie DIEClock::GetCorrelatedTime auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime) Wenn der EVR keine Präsentationsuhr hat oder ein Beispiel keinen Zeitstempel hat, können Sie das Beispiel sofort nach dem Erhalten präsentieren.

Um die Dauer jedes Beispiels zu erhalten, rufen [**Sie DIESAMPLE::GetSampleDuration auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) Wenn das Beispiel über keine Dauer verfügt, können Sie die [**Funktion MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) verwenden, um die Dauer aus der Framerate zu berechnen.

Beachten Sie beim Planen von Beispielen Folgendes:

-   Wenn die Wiedergaberate schneller oder langsamer als die normale Geschwindigkeit ist, wird die Uhr mit einer schnelleren oder langsameren Geschwindigkeit ausgeführt. Das bedeutet, dass der Zeitstempel für ein Beispiel immer die richtige Zielzeit relativ zur Präsentationsuhr liefert. Wenn Sie die Präsentationszeiten jedoch in eine andere Uhrzeit (z. B. den Leistungsindikator für hohe Auflösung) übersetzen, müssen Sie die Zeiten basierend auf der Taktgeschwindigkeit skalieren. Wenn sich die Taktgeschwindigkeit ändert, ruft der EVR die [**METHODE DER MODERATORClockStateSink::OnClockSetRate auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate)
-   Die Wiedergaberate kann bei umgekehrter Wiedergabe negativ sein. Wenn die Wiedergaberate negativ ist, wird die Präsentationsuhr rückwärts ausgeführt. Anders ausgedrückt: Die *Zeit N* + 1 tritt vor der Zeit *N auf.*

Im folgenden Beispiel wird berechnet, wie früh oder spät ein Beispiel relativ zur Präsentationsuhr ist:


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



Die Präsentationsuhr wird in der Regel von der Systemuhr oder dem Audiorenderer gesteuert. (Der Audiorenderer leitet die Zeit von der Rate ab, mit der die Soundkarte Audiodaten verwendet.) Im Allgemeinen wird die Präsentationsuhr nicht mit der Aktualisierungsrate des Monitors synchronisiert.

Wenn Ihre Direct3D-Präsentationsparameter D3DPRESENT_INTERVAL_DEFAULT oder **D3DPRESENT_INTERVAL_ONE** für das Präsentationsintervall angeben, wartet der Present-Vorgang auf die vertikale Rückverziehung des Monitors.   Dies ist eine einfache Möglichkeit, um Dasins zu verhindern, verringert jedoch die Genauigkeit Ihres Planungsalgorithmus. Wenn das Präsentationsintervall hingegen D3DPRESENT_INTERVAL_IMMEDIATE **ist,** wird die **Present-Methode** sofort ausgeführt. Dies führt zu einer Tränkung, es sei denn, Ihr Planungsalgorithmus ist genau genug, dass Sie **Present** nur während des vertikalen Rücklaufzeitraums aufrufen.

Mit den folgenden Funktionen können Sie genaue Zeitsteuerungsinformationen erhalten:

-   **IDirect3DDevice9::GetRasterStatus** gibt Informationen zum Raster zurück, einschließlich der aktuellen Scanzeile und ob sich das Raster im vertikalen leeren Bereich befindet.
-   **DwmGetCompositionTimingInfo gibt** Zeitsteuerungsinformationen für den Desktopfenster-Manager zurück. Diese Informationen sind nützlich, wenn die Desktopkomposition aktiviert ist.

### <a name="presenting-samples"></a>Präsentieren von Beispielen

In diesem Abschnitt wird davon ausgegangen, dass Sie eine separate Austauschkette für jede Oberfläche erstellt haben, wie unter [Allocating Direct3D Surfaces (Zuordnen von Direct3D-Oberflächen) beschrieben.](#allocating-direct3d-surfaces) Um ein Beispiel zu präsentieren, erhalten Sie die Swap-Kette wie folgt aus dem Videobeispiel:

1.  Rufen [**Sie IMBSAMPLE::GetBufferByIndex im**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) Videobeispiel auf, um den Puffer zu erhalten.
2.  Fragen Sie den Puffer für die [**BENUTZEROBERFLÄCHEGetService-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ab.
3.  Rufen [**SieGEGETService::GetService auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) um die **IDirect3DSurface9-Schnittstelle** der Direct3D-Oberfläche zu erhalten. (Sie können diesen Schritt und den vorherigen Schritt zu einem Schritt kombinieren, indem Sie [**MFGetService aufrufen.)**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)
4.  Rufen **Sie IDirect3DSurface9::GetContainer** auf der Oberfläche auf, um einen Zeiger auf die Austauschkette zu erhalten.
5.  Rufen **Sie IDirect3DSwapChain9::P für die** Swapkette zurück.

Diese Schritte sind im folgenden Code dargestellt:


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a>Quell- und Zielrechtecke

Das *Quellrechteck* ist der Anzuzeigende Teil des Videoframes. Sie wird relativ zu einem normalisierten Koordinatensystem definiert, bei dem der gesamte Videoframe ein Rechteck mit den Koordinaten {0, 0, 1, 1} einnimmt. Das *Zielrechteck* ist der Bereich innerhalb der Zieloberfläche, in dem der Videoframe gezeichnet wird. Mit dem Standardvorzeiger kann eine Anwendung diese Rechtecke festlegen, indem [**SIE DENKVideoDisplayControl::SetVideoPosition aufruft.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)

Es gibt mehrere Optionen zum Anwenden von Quell- und Zielrechtecke. Die erste Option besteht in der Anwendung durch den Mixer:

-   Legen Sie das Quellrechteck [**mithilfe**](video-zoom-rect-attribute.md) des VIDEO_ZOOM_RECT fest. Der Mixer wird das Quellrechteck anwenden, wenn er das Video auf die Zieloberfläche blitt. Das Standardquellenrechteck des Mixers ist der gesamte Frame.
-   Legen Sie das Zielrechteck als geometrische Öffnung im Ausgabetyp des Mixers fest. Weitere Informationen finden Sie unter [Aushandeln von Formaten.](#negotiating-formats)

Die zweite Option besteht in der Anwendung der Rechtecke, wenn Sie **IDirect3DSwapChain9::P resent** verwenden, indem Sie die *Parameter pSourceRect* und *pDestRect* in der **Present-Methode** angeben. Sie können diese Optionen kombinieren. Beispielsweise können Sie das Quellrechteck für den Mixer festlegen, aber das Zielrechteck in der **Present-Methode** anwenden.

Wenn die Anwendung das Zielrechteck ändert oder die Größe des Fensters ändert, müssen Sie möglicherweise neue Oberflächen zuordnen. Wenn dies der Fall ist, müssen Sie darauf achten, diesen Vorgang mit Ihrem Planungsthread zu synchronisieren. Leeren Sie die Planungswarteschlange, und verwerfen Sie die alten Stichproben, bevor Sie neue Oberflächen zuordnen.

### <a name="end-of-stream"></a>Ende des Streams

Wenn jeder Eingabedatenstrom auf der EVR beendet wurde, sendet der EVR eine MFVP_MESSAGE_ENDOFSTREAM **nachricht** an den Moderator. An dem Punkt, an dem Sie die Nachricht empfangen, müssen jedoch möglicherweise noch einige Videoframes verarbeitet werden. Bevor Sie auf die Nachricht zum Ende des Streams antworten, müssen Sie die ganze Ausgabe des Mixers leeren und alle verbleibenden Frames anzeigen. Nachdem der letzte Frame angezeigt wurde, senden Sie **ein** EC_COMPLETE an die EVR.

Das nächste Beispiel zeigt eine Methode, die das **EC_COMPLETE** sendet, wenn verschiedene Bedingungen erfüllt sind. Andernfalls wird S_OK zurückgegeben, ohne das Ereignis zu senden:


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



Diese Methode überprüft die folgenden Zustände:

-   Wenn die *m_fSampleNotify* true **ist,** bedeutet dies, dass der Mixer über einen oder mehrere Frames verfügt, die noch nicht verarbeitet wurden. (Weitere Informationen finden Sie unter [Processing Output](#processing-output).)
-   Die *m_fEndStreaming* variable ist ein boolesches Flag, dessen Anfangswert **FALSE ist.** Der Moderator legt das Flag auf **TRUE fest,** wenn der EVR **die** MFVP_MESSAGE_ENDOFSTREAM sendet.
-   Es wird davon ausgegangen, dass die Methode TRUE zurück gibt, solange ein oder mehrere Frames `AreSamplesPending` in der geplanten Warteschlange warten. 

Legen Sie [**in der METHODE VORVIDEOPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) m_fEndStreaming **TRUE** fest, und rufen Sie auf, wenn die EVR die MFVP_MESSAGE_ENDOFSTREAM  `CheckEndOfStream` sendet: 


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Rufen Sie darüber hinaus auf, wenn `CheckEndOfStream` die [**METHODE VERFORMTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers MF_E_TRANSFORM_NEED_MORE_INPUT.  Dieser Fehlercode gibt an, dass der Mixer keine Eingabebeispiele mehr enthält (siehe [Verarbeiten der Ausgabe](#processing-output)).

## <a name="frame-stepping"></a>Rahmenschritt

Der EVR ist für die Unterstützung von Rahmenschritten in DirectShow und bereinigung in Media Foundation. Frameschritt- und Bereinigungsschritte sind konzeptionell ähnlich. In beiden Fällen fordert die Anwendung einen Videoframe nach dem anderen an. Intern verwendet der Presenter denselben Mechanismus, um beide Features zu implementieren.

Frameschritte in DirectShow funktionieren wie folgt:

-   Die Anwendung ruft [**IVideoFrameStep::Step auf.**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step) Die Anzahl der Schritte wird im *dwSteps-Parameter* angegeben. Der EVR sendet eine **MFVP_MESSAGE_STEP** nachricht an den Moderator, wobei der Message-Parameter (*ulParam*) die Anzahl der Schritte ist.
-   Wenn die Anwendung [**IVideoFrameStep::CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) aufruft oder den Graphzustand ändert (wird ausgeführt, angehalten oder **beendet),** sendet die EVR eine MFVP_MESSAGE_CANCELSTEP Nachricht.

Die Bereinigung in Media Foundation funktioniert wie folgt:

-   Die Anwendung legt die Wiedergaberate auf 0 (null) fest, indem [**sie DURCH AUFRUFEN VONTRATEControl::SetRate aufruft.**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
-   Um einen neuen Frame zu rendern, ruft die Anwendung [**DIETMEDIASession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) mit der gewünschten Position auf. Der EVR sendet **eine** MFVP_MESSAGE_STEP nachricht mit *ulParam* gleich 1.
-   Um die Bereinigung zu beenden, legt die Anwendung die Wiedergaberate auf einen Wert ungleich 0 (null) fest. Der EVR sendet die **MFVP_MESSAGE_CANCELSTEP** Nachricht.

Nachdem die **MFVP_MESSAGE_STEP** empfangen wurde, wartet die Moderatorin, bis der Zielframe eintrifft. Wenn die Anzahl der Schritte *N beträgt,* verwirft der Moderator die nächsten (*N* - 1) Beispiele und stellt das *N-te* Beispiel vor. Wenn die Moderatorin den Rahmenschritt abgeschlossen [](../directshow/ec-step-complete.md) hat, sendet sie ein EC_STEP_COMPLETE-Ereignis an die EVR, bei dem *lParam1* auf **FALSE festgelegt ist.** Wenn die Wiedergaberate 0 (null) ist, sendet die Moderatorin außerdem [**ein**](../directshow/ec-scrub-time.md) EC_SCRUB_TIME Ereignis. Wenn die EVR frame stepping abbricht, während ein Frameschrittvorgang  noch aussteht, sendet die Moderatorin ein EC_STEP_COMPLETE-Ereignis, wobei *lParam1* auf **TRUE festgelegt ist.**

Die Anwendung kann schritt- oder bereinigungsschritte  mehrmals umrahmen, sodass der Moderator möglicherweise mehrere MFVP_MESSAGE_STEP empfangen kann, bevor er eine MFVP_MESSAGE_CANCELSTEP **erhält.** Außerdem kann der Moderator  die MFVP_MESSAGE_STEP empfangen, bevor die Uhr gestartet wird oder während die Uhr ausgeführt wird.

### <a name="implementing-frame-stepping"></a>Implementieren von Rahmenschritten

In diesem Abschnitt wird ein Algorithmus zum Implementieren von Rahmenschritten beschrieben. Der Frameschrittalgorithmus verwendet die folgenden Variablen:

-   *step_count*. Eine ganze Zahl ohne Vorzeichen, die die Anzahl der Schritte im aktuellen Rahmenschrittvorgang angibt.
-   *step_queue*. Eine Warteschlange [**von WARTESCHLANGENsample-Zeigern.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
-   *step_state*. Der Moderator kann sich in Bezug auf die Rahmenschritte jederzeit in einem der folgenden Zustände befingen: 

    | State         | Beschreibung                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Keine Rahmenschritte.                                                                                                                                                                                             |
    | WAITING       | Der Moderator hat die **MFVP_MESSAGE_STEP** empfangen, aber die Uhr wurde nicht gestartet.                                                                                                                  |
    | PENDING (AUSSTEHEND)       | Der Moderator hat die **MFVP_MESSAGE_STEP** empfangen, und die Uhr wurde gestartet, aber der Moderator wartet auf den Empfang des Zielframes.                                                             |
    | Geplant     | Der Präsentationser hat den Zielframe empfangen und für die Präsentation geplant, aber der Frame wurde nicht dargestellt.                                                                                        |
    | vollständig      | Der Moderator hat den Zielframe dargestellt und das EC_STEP_COMPLETE [**gesendet**](../directshow/ec-step-complete.md) und wartet auf die nächste MFVP_MESSAGE_STEP **oder** **MFVP_MESSAGE_CANCELSTEP** Nachricht. |

    

     

    Diese Zustände sind unabhängig von den Presenterzuständen, die im Abschnitt [Presenter States aufgeführt sind.](#presenter-states)

Die folgenden Verfahren sind für den Algorithmus für die Frameschritt-Prozedur definiert:

PrepareFrameStep-Prozedur

1.  *Inkrement step_count*.
2.  Legen *step_state* auf WAITING fest.
3.  Wenn die Uhr ausgeführt wird, rufen Sie StartFrameStep auf.

StartFrameStep-Prozedur

1.  Wenn *step_state* warte, legen *Sie* step_state ausstehend fest. Rufen Sie für jedes Beispiel in *step_queue* DeliverFrameStepSample auf.
2.  Wenn *step_state* gleich NOT_STEPPING, entfernen Sie alle Beispiele aus *step_queue,* und planen Sie sie für die Präsentation.

CompleteFrameStep-Prozedur

1.  Legen *step_state* auf COMPLETE fest.
2.  Senden Sie das EC_STEP_COMPLETE mit *lParam1*  =  **FALSE**.
3.  Wenn die Taktrate null ist, senden Sie **das** EC_SCRUB_TIME mit der Beispielzeit.

DeliverFrameStepSample-Prozedur

1.  Wenn die Taktrate 0 (null) und *die* Stichprobendauer  +  *der Stichprobendauer*  <  ist, verwerfen Sie die Stichprobe. Beenden
2.  Wenn *step_state* SCHEDULED oder COMPLETE ist, fügen Sie das Beispiel zu *step_queue.* Beenden
3.  Dekrementierung *step_count*.
4.  Wenn *step_count* > 0 ist, verwerfen Sie das Beispiel. Beenden
5.  Wenn *step_state* warte, fügen Sie das Beispiel zu *step_queue.* Beenden
6.  Planen Sie das Beispiel für die Präsentation.
7.  Legen *step_state* auf SCHEDULED fest.

CancelFrameStep-Prozedur

1.  Legen *step_state* auf NOT_STEPPING
2.  Setzen *step_count* auf 0 (null) zurück.
3.  Wenn der vorherige Wert von *step_state* WAITING, PENDING oder SCHEDULED war, senden Sie EC_STEP_COMPLETE *lParam1*  =  **TRUE.**

Rufen Sie diese Verfahren wie folgt auf:



| Presenter-Nachricht oder -Methode                                                   | Prozedur           |
|-------------------------------------------------------------------------------|---------------------|
| **MFVP_MESSAGE_STEP-Nachricht**                                               | `PrepareFrameStep`  |
| **MFVP_MESSAGE_STEP-Nachricht**                                               | `CancelStep`        |
| [**DEADClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**DEADClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| [**RÜCKRUFTrackedSample-Rückruf**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)                         | `CompleteFrameStep` |
| [**DEADClockStateSink::OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**DEADClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

Das folgende Flussdiagramm zeigt die Prozeduren für die Frameschritte.

![Flussdiagramm mit Pfaden, die mit mfvp message step und \- \- mfvp message processinputnotify beginnen und mit \- \- "state = complete" enden](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Festlegen des Presenters auf der EVR

Nach der Implementierung des Presenters besteht der nächste Schritt im Konfigurieren der EVR für die Verwendung.

### <a name="setting-the-presenter-in-directshow"></a>Festlegen des Presenters in DirectShow

Legen Sie in einer DirectShow-Anwendung den Presenter auf der EVR wie folgt fest:

1.  Erstellen Sie den EVR-Filter, indem **Sie CoCreateInstance aufrufen.** Die CLSID ist **CLSID_EnhancedVideoRenderer**.
2.  Fügen Sie die EVR dem Filterdiagramm hinzu.
3.  Erstellen Sie eine Instanz Ihrer Präsentation. Ihre Moderatorin kann die Com-Standardobjekterstellung über **IClassFactory** unterstützen, dies ist jedoch nicht zwingend erforderlich.
4.  Fragen Sie den EVR-Filter für die [**BENUTZEROBERFLÄCHEVideoRenderer-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) ab.
5.  Rufen [**Sie DIE NSDVideoRenderer::InitializeRenderer auf.**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)

### <a name="setting-the-presenter-in-media-foundation"></a>Festlegen des Presenters in Media Foundation

In Media Foundation stehen Ihnen mehrere Optionen zur Verfügung, je nachdem, ob Sie die EVR-Mediensenke oder das EVR-Aktivierungsobjekt erstellen. Weitere Informationen zu Aktivierungsobjekten finden Sie unter [Activation Objects](activation-objects.md).

Gehen Sie für die EVR-Mediensenke wie folgt vor:

1.  Rufen [**Sie MFCreateVideoRenderer auf,**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) um die Mediensenke zu erstellen.
2.  Erstellen Sie eine Instanz Ihrer Präsentation.
3.  Fragen Sie die EVR-Mediensenke für die [**BENUTZEROBERFLÄCHEVideoRenderer-Schnittstelle**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) ab.
4.  Rufen [**Sie DIE NSDVideoRenderer::InitializeRenderer auf.**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)

Gehen Sie für das EVR-Aktivierungsobjekt wie folgt vor:

1.  Rufen [**Sie MFCreateVideoRendererActivate auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) um das Aktivierungsobjekt zu erstellen.
2.  Legen Sie eines der folgenden Attribute für das Aktivierungsobjekt fest: 

    | attribute                                                                                                         | Beschreibung                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Zeiger auf ein Aktivierungsobjekt für den Presenter.<br/> Mit diesem Flag müssen Sie ein Aktivierungsobjekt für Ihre Präsentation bereitstellen. Das Aktivierungsobjekt muss die [**-SCHNITTSTELLE FÜR DIE-Aktivierung**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) implementieren.<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID des Presenters.<br/> Mit diesem Flag muss Ihr Presenter die Standardmäßigerstellung von COM-Objekten über **IClassFactory** unterstützen.<br/>                                                                                         |

    

     

3.  Legen Sie optional das [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS-Attribut**](mf-activate-custom-video-presenter-flags-attribute.md) für das Aktivierungsobjekt fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> <dt>

[EVRPresenter-Beispiel](evrpresenter-sample.md)
</dt> </dl>

 

 
