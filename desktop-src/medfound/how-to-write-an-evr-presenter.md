---
description: In diesem Artikel wird beschrieben, wie Sie einen benutzerdefinierten Presenter für den erweiterten Videorenderer (EVR) schreiben.
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Schreiben von EVR Presenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557063"
---
# <a name="how-to-write-an-evr-presenter"></a>Schreiben von EVR Presenter

In diesem Artikel wird beschrieben, wie Sie einen benutzerdefinierten Presenter für den erweiterten Videorenderer (EVR) schreiben. Ein benutzerdefinierter Presenter kann sowohl mit DirectShow als auch mit Media Foundation verwendet werden. die Schnittstellen und das Objektmodell sind für beide Technologien identisch, obwohl die genaue Reihenfolge der Vorgänge variieren kann.

Der Beispielcode in diesem Thema wird aus dem [evrpresenter](evrpresenter-sample.md)-Beispiel, das im Windows SDK bereitgestellt wird, angepasst.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Presenter-Objektmodell](#presenter-object-model)
    -   [Datenfluss innerhalb des EVR](#data-flow-inside-the-evr)
    -   [Presenter-Zustände](#presenter-states)
    -   [Presenter-Schnittstellen](#presenter-interfaces)
    -   [Implementieren von IMF videode viceid](#implementing-imfvideodeviceid)
    -   [Implementieren von imftopologyservicelookupclient](#implementing-imftopologyservicelookupclient)
    -   [Implementieren von IMF videopresenter](#implementing-imfvideopresenter)
    -   [Implementieren von IMF-staatink](#implementing-imfclockstatesink)
    -   [Implementieren von imfratesupport](#implementing-imfratesupport)
    -   [Senden von Ereignissen an den EVR](#sending-events-to-the-evr)
-   [Aushandeln von Formaten](#negotiating-formats)
-   [Verwalten des Direct3D-Geräts](#managing-the-direct3d-device)
    -   [Zuordnen von Direct3D-Flächen](#allocating-direct3d-surfaces)
    -   [Überwachungsbeispiele](#tracking-samples)
-   [Ausgabe wird verarbeitet](#processing-output)
    -   [Neuzeichnen von Frames](#repainting-frames)
    -   [Beispiele für Zeitplanung](#scheduling-samples)
    -   [Präsentieren von Beispielen](#presenting-samples)
    -   [Quell-und Ziel Rechtecke](#source-and-destination-rectangles)
    -   [Ende des Streams](#end-of-stream)
-   [Frame Schritt Schritt](#frame-stepping)
    -   [Implementieren von Frame-Stepping](#implementing-frame-stepping)
-   [Festlegen des Präsentators für den EVR](#setting-the-presenter-on-the-evr)
    -   [Festlegen des Präsentators in DirectShow](#setting-the-presenter-in-directshow)
    -   [Festlegen des Präsentators in Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie einen benutzerdefinierten Presenter schreiben, sollten Sie mit den folgenden Technologien vertraut sein:

-   Der erweiterte Videorenderer. Siehe [verbesserter Videorenderer](enhanced-video-renderer.md).
-   Direct3D-Grafiken. Sie müssen keine 3D-Grafiken verstehen, um einen Presenter zu schreiben, aber Sie müssen wissen, wie Sie ein Direct3D-Gerät erstellen und Direct3D-Oberflächen verwalten. Wenn Sie mit Direct3D nicht vertraut sind, lesen Sie die Abschnitte "Direct3D Devices" und "Direct3D Resources" in der Dokumentation zum DirectX Graphics SDK.
-   DirectShow-Filter Diagramme oder die Media Foundation Pipeline, abhängig von der Technologie, die Ihre Anwendung zum Rendering von Videos verwendet.
-   [Media Foundation Transformationen](media-foundation-transforms.md). Der EVR-Mixer ist eine Media Foundation Transformation, und der Presenter ruft Methoden direkt auf dem Mixer auf.
-   Implementieren von COM-Objekten. Der Presenter ist ein Prozess interner, frei Thread-com-Objekt.

## <a name="presenter-object-model"></a>Presenter-Objektmodell

Dieser Abschnitt enthält eine Übersicht über das Presenter-Objektmodell und Schnittstellen.

### <a name="data-flow-inside-the-evr"></a>Datenfluss innerhalb des EVR

Der EVR verwendet zwei Plug-in-Komponenten, um das Video zu Rendering: den *Mixer* und den *Presenter*. Der Mixer mischt die Videostreams und deinstalmengt das Video bei Bedarf. Der Presenter zeichnet das Video auf der Anzeige und plant, wenn jeder Frame gezeichnet wird. Anwendungen können eines dieser Objekte durch eine benutzerdefinierte Implementierung ersetzen.

Der EVR verfügt über einen oder mehrere Eingabedaten Ströme, und der Mixer verfügt über eine entsprechende Anzahl von Eingabedaten strömen. Stream 0 ist immer der *Verweis Datenstrom*. Die anderen Streams sind *Substreams*, die der mischungsstream in den Verweis Datenstrom einfügt. Der Verweis Datenstrom bestimmt die Master Frame-Rate für das zusammengesetzte Video. Der Mixer nimmt für jeden Verweis Rahmen den neuesten Frame aus jedem substream, mischt sie in den Verweis Rahmen und gibt einen einzelnen zusammengesetzten Frame aus. Der Mixer führt bei Bedarf auch Deinterlacing-und Farb Konvertierungen von YUV in RGB aus. Der EVR fügt den Mixer immer in die Video Pipeline ein, unabhängig von der Anzahl der Eingabedaten Ströme oder des Video Formats. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![das Diagramm zeigt den Verweis Datenstrom und den unter Datenstrom, der auf den Mixer zeigt, der auf den Presenter zeigt, der auf die Anzeige zeigt.](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

Der Presenter führt die folgenden Aufgaben aus:

-   Legt das Ausgabeformat auf dem Mixer fest. Bevor das Streaming beginnt, legt der Presenter einen Medientyp für den Ausgabestream des Mischers fest. Dieser Medientyp definiert das Format des zusammengesetzten Bilds.
-   Erstellt das Direct3D-Gerät.
-   Weist Direct3D-Oberflächen zu. Der Mixer bliert die zusammengesetzten Frames auf diese Oberflächen.
-   Ruft die Ausgabe des Mischers ab.
-   Plant, wann die Frames angezeigt werden. Der EVR stellt die Präsentationszeit bereit, und der Presenter plant Frames entsprechend dieser Uhr.
-   Stellt jeden Frame mithilfe von Direct3D dar.
-   Führt Frame-und Scrubbing aus.

### <a name="presenter-states"></a>Presenter-Zustände

Der Presenter befindet sich jederzeit in einem der folgenden Zustände:

-   *Gestartet*. Die Präsentations Uhr der EVR wird ausgeführt. Der Presenter plant Video Frames für die Präsentation, sobald sie eintreffen.
-   *Angeh* alten. Die Präsentations Uhr ist angehalten. Der Presenter zeigt keine neuen Beispiele an, behält jedoch die Warteschlange geplanter Beispiele bei. Wenn neue Beispiele empfangen werden, fügt der Presenter Sie der Warteschlange hinzu.
-   *Stopped*(Beendet): Dies ist der anfängliche Status des Kanals nach seiner Erstellung (es sei denn, im Portal wurde das automatische Starten gewählt). Die Präsentations Uhr wurde beendet. Der Presenter verwirft alle geplanten Beispiele.
-   *Herunterfahren.* Der Presenter gibt alle Ressourcen im Zusammenhang mit dem Streaming frei, z. b. Direct3D Dies ist der Anfangszustand des Presenter und der endgültige Zustand, bevor der Presenter zerstört wird.

Im Beispielcode in diesem Thema wird der Presenter-Zustand durch eine Enumeration dargestellt:


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Einige Vorgänge sind ungültig, während sich der Presenter im Zustand "Herunterfahren" befindet. Im Beispielcode wird dieser Zustand durch Aufrufen einer Hilfsmethode überprüft:


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

Ein Präsentator ist erforderlich, um die folgenden Schnittstellen zu implementieren:



| Schnittstelle                                                                | BESCHREIBUNG                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMF-staatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Benachrichtigt den Presenter, wenn die Uhr die Uhr den Zustand ändert. Siehe [Implementieren von IMF-staatink](#implementing-imfclockstatesink).                                   |
| [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Bietet eine Möglichkeit für die Anwendung und andere Komponenten in der Pipeline, Schnittstellen vom Präsentator zu erhalten.                                                       |
| [**Imftopologyservicelookupclient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Ermöglicht dem Presenter, Schnittstellen vom EVR oder dem Mixer zu erhalten. Weitere Informationen finden Sie unter [Implementieren von imftopologyservicelookupclient](#implementing-imftopologyservicelookupclient). |
| [**IMF videoabviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden. Weitere Informationen finden Sie unter [Implementieren von IMF videode viceid](#implementing-imfvideodeviceid).                          |
| [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Verarbeitet Nachrichten aus dem EVR. Weitere Informationen finden Sie unter [Implementieren von IMF videopresenter](#implementing-imfvideopresenter).                                                             |



 

Die folgenden Schnittstellen sind optional:



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ievrtreuhändvideoplugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Ermöglicht dem Presenter, mit geschützten Medien zu arbeiten. Implementieren Sie diese Schnittstelle, wenn es sich bei dem Presenter um eine vertrauenswürdige Komponente handelt, die im geschützten Medien Pfad (PMP) funktionieren soll. |
| [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Meldet den Bereich der Wiedergabe Raten, die der Presenter unterstützt. Siehe [Implementieren von imfratesupport](#implementing-imfratesupport).                                         |
| [**IMF videopositionmapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Ordnet die Koordinaten im Video Frame der Ausgabe den Koordinaten des eingabevideoframes zu.                                                                                       |
| [**Iqualprop**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Meldet Leistungsinformationen. Der EVR verwendet diese Informationen für die Verwaltung der Qualitätskontrolle. Diese Schnittstelle ist im DirectShow SDK dokumentiert.                        |



 

Sie können auch Schnittstellen für die Anwendung bereitstellen, um mit dem Presenter zu kommunizieren. Der Standard Presenter implementiert zu diesem Zweck die [**IMF videodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle. Sie können diese Schnittstelle implementieren oder eigene definieren. Die Anwendung erhält Schnittstellen vom Präsentator, indem [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf dem EVR aufgerufen wird. Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, übergibt der EVR die **GetService** -Anforderung an den Presenter.

### <a name="implementing-imfvideodeviceid"></a>Implementieren von IMF videode viceid

Die [**IMF videodeviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) -Schnittstelle enthält eine Methode, [**getdeviceid**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), die eine Geräte-GUID zurückgibt. Die Geräte-GUID stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden. Wenn die Geräte-GUIDs nicht stimmen, kann der EVR nicht initialisiert werden.

Sowohl der Standard-Mixer als auch der Presenter verwenden Direct3D 9, wobei die Geräte-GUID gleich **IID_IDirect3DDevice9** ist. Wenn Sie Ihren benutzerdefinierten Presenter mit dem Standard-Mixer verwenden möchten, muss die Geräte-GUID des Präsentators **IID_IDirect3DDevice9** werden. Wenn Sie beide Komponenten ersetzen, können Sie eine neue Geräte-GUID definieren. Im restlichen Teil dieses Artikels wird davon ausgegangen, dass der Presenter Direct3D 9 verwendet. Hier ist die Standard Implementierung von [**getdeviceid**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):


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

### <a name="implementing-imftopologyservicelookupclient"></a>Implementieren von imftopologyservicelookupclient

Die [**imftopologyservicelookupclient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) -Schnittstelle ermöglicht dem Presenter das erhalten von Schnittstellen Zeigern aus dem EVR und vom Mixer wie folgt:

1.  Wenn der EVR den Presenter initialisiert, ruft er die [**imftopologyservicelookupclient:: initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) -Methode des Presenter auf. Das-Argument ist ein Zeiger auf die [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) -Schnittstelle von EVR.
2.  Der Presenter ruft [**IMFTopologyServiceLookup:: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) auf, um Schnittstellen Zeiger aus dem EVR oder dem Mixer zu erhalten.

Die [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) -Methode ähnelt der [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) -Methode. Beide Methoden übernehmen eine Dienst-GUID und eine Schnittstellen-ID (IID) als Eingabe, aber **LookupService** gibt ein Array von Schnittstellen Zeigern zurück, während **GetService** einen einzelnen Zeiger zurückgibt. In der Praxis können Sie jedoch die Array Größe immer auf 1 festlegen. Das Objekt, das abgefragt wird, hängt von der Dienst-GUID ab:

-   Wenn die Dienst-GUID **MR_VIDEO_RENDER_SERVICE** ist, wird der EVR abgefragt.
-   Wenn die Dienst-GUID **MR_VIDEO_MIXER_SERVICE** ist, wird der Mixer abgefragt.

Holen Sie in der Implementierung von [**initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)die folgenden Schnittstellen aus dem EVR:



| EVR-Schnittstelle                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Bietet eine Möglichkeit für den Presenter, Nachrichten an den EVR zu senden. Diese Schnittstelle wird im DirectShow SDK definiert, sodass die Nachrichten dem Muster für DirectShow-Ereignisse, nicht Media Foundation Ereignissen folgen.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**IMF**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Stellt die Uhr der EVR dar. Der Presenter verwendet diese Schnittstelle, um Beispiele für die Präsentation zu planen. Der EVR kann ohne eine Uhr ausgeführt werden, sodass diese Schnittstelle möglicherweise nicht verfügbar ist. Wenn dies nicht der Wert ist, ignorieren Sie den Fehlercode von [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).<br/> Die Uhr implementiert auch die [**IMF Timer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) -Schnittstelle. In der Media Foundation Pipeline implementiert die Uhr die [**IMF presentationclock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) -Schnittstelle. Diese Schnittstelle wird in DirectShow nicht implementiert.<br/> |



 

Holen Sie sich die folgenden Schnittstellen vom Mixer:



| Mixer-Schnittstelle                              | BESCHREIBUNG                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Ermöglicht es dem Presenter, mit dem Mixer zu kommunizieren.       |
| [**IMF videoabviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Ermöglicht es dem Presenter, die Geräte-GUID des Mischers zu validieren. |



 

Der folgende Code implementiert die [**initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) -Methode:


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



Wenn die von [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) erhaltenen Schnittstellen Zeiger nicht mehr gültig sind, ruft der EVR [**imftopologyservicelookupclient:: releaseservicezeigern**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)auf. Geben Sie in dieser Methode alle Schnittstellen Zeiger frei, und legen Sie den präsentatorzustand auf Herunterfahren fest:


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



Der EVR ruft [**releaseservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) aus verschiedenen Gründen auf, einschließlich:

-   Trennen oder erneutes Verbinden von Pins (DirectShow) oder hinzufügen oder Entfernen von streamsenken (Media Foundation).
-   Das Format wird geändert.
-   Festlegen einer neuen Uhr.
-   Das abschließende Herunterfahren des EVR.

Während der Lebensdauer des Presenter kann der EVR mehrmals [**initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) und [**releaseservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) aufrufen.

### <a name="implementing-imfvideopresenter"></a>Implementieren von IMF videopresenter

Die [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) -Schnittstelle erbt " [**IMF clockstaatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) " und fügt zwei Methoden hinzu:



| Methode                                                               | BESCHREIBUNG                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Getcurrentmediatype**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Gibt den Medientyp der zusammengesetzten Videorahmen zurück. |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Signalisiert dem Presenter, verschiedene Aktionen auszuführen.      |



 

Die [**getcurrentmediatype**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) -Methode gibt den Medientyp des Präsentators zurück. (Ausführliche Informationen zum Festlegen des Medientyps finden Sie unter [Aushandeln von Formaten](#negotiating-formats).) Der Medientyp wird als [**IMF videomediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) -Schnittstellen Zeiger zurückgegeben. Im folgenden Beispiel wird davon ausgegangen, dass der Presenter den Medientyp als [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Zeiger speichert. Um die **imfvideomediatype** -Schnittstelle aus dem Medientyp abzurufen, nennen Sie **QueryInterface**:


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



Die [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) -Methode ist der primäre Mechanismus für die Kommunikation zwischen EVR und Presenter. Die folgenden Meldungen sind definiert. Weitere Informationen zum Implementieren der einzelnen Nachrichten finden Sie im weiteren Verlauf dieses Themas.



| `Message`                                | BESCHREIBUNG                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | Der Ausgabe Medientyp des Mischers ist ungültig. Der Presenter sollte mit dem Mixer einen neuen Medientyp aushandeln. Siehe [Aushandeln von Formaten](#negotiating-formats).                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | Streaming wurde gestartet. Eine bestimmte Aktion ist für diese Nachricht nicht erforderlich, Sie können Sie jedoch verwenden, um Ressourcen zuzuordnen.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | Streaming wurde beendet. Geben Sie alle Ressourcen frei, die Sie als Antwort auf die **MFVP_MESSAGE_BEGINSTREAMING** Nachricht zugeordnet haben.                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | Der Mixer hat eine neue Eingabe Stichprobe erhalten und kann ggf. einen neuen Ausgabe Rahmen generieren. Der Presenter sollte [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer aufzurufen. Siehe [Verarbeitung der Ausgabe](#processing-output). |
| **MFVP_MESSAGE_ENDOFSTREAM**         | Die Präsentation wurde beendet. Siehe [Ende des Datenstroms](#end-of-stream).                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | Der EVR Leerung die Daten in seiner Renderingpipeline. Der Presenter sollte alle Video Frames verwerfen, die für die Präsentation geplant sind.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Fordert den Presenter auf, einen Schritt vorwärts für N-Frames durchzusetzen Der Presenter sollte die nächsten N-1-Frames verwerfen und den Nth-Frame anzeigen. Siehe [Frame-Stepping](#frame-stepping).                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Bricht die Frame-Schritt Verarbeitung ab.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Implementieren von IMF-staatink

Der Presenter muss die [**imatclockstaatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) -Schnittstelle als Teil der Implementierung von [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)implementieren, die **IMF-staatink** erbt. Der EVR verwendet diese Schnittstelle, um den Presenter zu benachrichtigen, wenn sich der Zustand der EVR-Uhr ändert. Weitere Informationen zu den uhrzuständen finden Sie unter [Präsentations Uhr](presentation-clock.md).

Im folgenden finden Sie einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle. Alle Methoden sollten fehlschlagen, wenn der Presenter heruntergefahren wird.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>Onclockstart</strong></a></td>
<td><ol>
<li>Legen Sie den präsentatorstatus auf Started fest.</li>
<li>Wenn <em>llclockstarteset</em> nicht <strong>PRESENTATION_CURRENT_POSITION</strong>ist, leeren Sie die Warteschlange der Beispiele für den Presenter. (Dies entspricht dem Empfangen einer <strong>MFVP_MESSAGE_FLUSH</strong> Nachricht.)</li>
<li>Wenn eine vorherige Frame-Step-Anforderung noch aussteht, verarbeiten Sie die Anforderung (siehe <a href="#frame-stepping">Frame</a>-Step). Versuchen Sie andernfalls, die Ausgabe des Mischers zu verarbeiten (siehe <a href="#processing-output">Verarbeitung der Ausgabe</a>).</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>Onclockstoppt</strong></a></td>
<td><ol>
<li>Legen Sie den präsentatorstatus auf beendet fest.</li>
<li>Leert die Warteschlange von Beispielen für den Presenter.</li>
<li>Abbrechen Sie alle ausstehenden Rahmen Schritt Vorgänge.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>Onclockpause</strong></a></td>
<td>Legen Sie den präsentatorstatus auf angehalten fest.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>Onclockrestart</strong></a></td>
<td>Behandeln Sie das gleiche wie bei <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>onclockstart</strong></a> , aber lassen Sie die Warteschlange von Beispielen nicht leeren.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>Onclock-trate</strong></a></td>
<td><ol>
<li>Wenn die Rate von 0 (null) in einen Wert ungleich 0 (null) wechselt, brechen Sie die Frame</li>
<li>Speichern Sie die neue Taktrate. Die Taktfrequenz wirkt sich auf die Anzeige von Beispielen aus. Weitere Informationen finden Sie unter <a href="#scheduling-samples">Beispiele</a>für die Planung.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>Implementieren von imfratesupport

Zur Unterstützung von Wiedergabe Raten mit Ausnahme von 1 × Geschwindigkeit muss der Presenter die [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle implementieren. Im folgenden finden Sie einige Richtlinien für die Implementierung der Methoden in dieser Schnittstelle. Alle Methoden sollten fehlschlagen, nachdem der Presenter heruntergefahren wurde. Weitere Informationen zu dieser Schnittstelle finden Sie unter [Raten Steuerung](rate-control.md).



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Geort lowestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Gibt 0 (null) zurück, um keine minimale Wiedergabe Rate anzugeben.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Getfastestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | Bei einer nicht dünnen Wiedergabe sollte die Wiedergabe Rate nicht die Aktualisierungsrate des Monitors überschreiten: *Maximale Raten*  =  *Aktualisierungsrate* (Hz)/ *Video Frame Rate* (fps). Die Video Frame Rate wird im Medientyp des Presenter angegeben. <br/> Bei der dünnen Wiedergabe ist die Wiedergabe Rate unbegrenzt. Gibt den Wert **FLT_MAX** zurück. In der Praxis sind Quelle und Decoder die einschränkenden Faktoren bei der dünnen Wiedergabe. <br/> Geben Sie für die umgekehrte Wiedergabe den negativen Wert der maximalen Rate zurück.<br/> |
| [**Isratesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Gibt **MF_E_UNSUPPORTED_RATE** zurück, wenn der absolute Wert von *flrate* die maximale Wiedergabe Rate des Presenter überschreitet. Berechnen Sie die maximale Wiedergabe Rate, wie für [**getfastestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)beschrieben.                                                                                                                                                                                                                                                                                    |



 

Im folgenden Beispiel wird gezeigt, wie die [**getfastestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) -Methode implementiert wird:


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



Im vorherigen Beispiel wird die Hilfsmethode getmaxrate aufgerufen, um die maximale vorwärts Wiedergabe Rate zu berechnen:

Im folgenden Beispiel wird gezeigt, wie die [**isratesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) -Methode implementiert wird:


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



### <a name="sending-events-to-the-evr"></a>Senden von Ereignissen an den EVR

Der Presenter muss den EVR verschiedener Ereignisse benachrichtigen. Hierfür wird die [**imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) -Schnittstelle von EVR verwendet, die abgerufen wird, wenn der EVR die [**imftopologyservicelookupclient:: initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) -Methode des Presenter aufruft. (Die **imediaeventsink** -Schnittstelle ist ursprünglich eine DirectShow-Schnittstelle, wird aber sowohl in DirectShow EVR als auch in der Media Foundation verwendet.) Der folgende Code zeigt, wie ein Ereignis an den EVR gesendet wird:


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



In der folgenden Tabelle werden die vom Presenter gesendeten Ereignisse zusammen mit den Ereignis Parametern aufgelistet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ereignis</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>Der Presenter hat das Rendern aller Frames nach der MFVP_MESSAGE_ENDOFSTREAM Meldung abgeschlossen.<br/>
<ul>
<li><em>Param1</em>: HRESULT, das den Status des Vorgangs angibt.</li>
<li><em>Param2</em>: nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#end-of-stream">Ende des Datenstroms</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>Das Direct3D-Gerät wurde geändert.<br/>
<ul>
<li><em>Param1</em>: nicht verwendet.</li>
<li><em>Param2</em>: nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#managing-the-direct3d-device">Verwalten des Direct3D-Geräts</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>Ein Fehler ist aufgetreten, bei dem das Streaming beendet werden muss.<br/>
<ul>
<li><em>Param1</em>: <strong>HRESULT</strong> , das den Fehler angibt, der aufgetreten ist.</li>
<li><em>Param2</em>: nicht verwendet.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>Gibt die Zeitspanne an, die der Presenter zum Rendering der einzelnen Frames einnimmt. (Optional.)<br/>
<ul>
<li><em>Param1</em>: Zeiger auf einen Konstanten <strong>Longlong</strong> -Wert, der die Zeitspanne für die Verarbeitung des Frames in 100-Nanosecond-Einheiten enthält.</li>
<li><em>Param2</em>: nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#processing-output">Verarbeiten der Ausgabe</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>Gibt die aktuelle Verzögerungszeit in renderingbeispielen an. Wenn der Wert positiv ist, werden die Beispiele hinter dem Zeitplan angezeigt. Wenn der Wert negativ ist, werden die Beispiele vor dem Zeitplan angezeigt. (Optional.)<br/>
<ul>
<li><em>Param1</em>: Zeiger auf einen Konstanten <strong>Longlong</strong> -Wert, der die Verzögerungszeit in 100-Nanosecond-Einheiten enthält.</li>
<li><em>Param2</em>: nicht verwendet.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>Wird unmittelbar nach <strong>EC_STEP_COMPLETE</strong> gesendet, wenn die Wiedergabe Rate 0 (null) ist. Dieses Ereignis enthält den Zeitstempel des Bilds, der angezeigt wurde.<br/>
<ul>
<li><em>Param1</em>: niedrigere 32 Bits des Zeitstempels.</li>
<li><em>Param2</em>: Obere 32 Bits des Zeitstempels.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Step Stepping</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>Der Presenter hat einen Frame Schritt abgeschlossen oder abgebrochen.<br/>
<ul>
<li><em>Param1</em>: nicht verwendet.</li>
<li><em>Param2</em>: nicht verwendet.</li>
</ul>
Weitere Informationen finden Sie unter <a href="#frame-stepping">Frame Step Stepping</a>.<br/>
<blockquote>
[!Note]<br />
Eine frühere Version der beschriebenen Dokumentation <em>param1</em> falsch. Dieser Parameter wird für dieses Ereignis nicht verwendet.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>Aushandeln von Formaten

Jedes Mal, wenn der Presenter eine **MFVP_MESSAGE_INVALIDATEMEDIATYPE** Nachricht vom EVR empfängt, muss er wie folgt das Ausgabeformat auf dem Mixer festlegen:

1.  Wenn Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf dem Mixer aufrufen, erhalten Sie einen möglichen Ausgabetyp. Dieser Typ beschreibt ein Format, das der Mixer mithilfe der Eingabestreams und der Video Verarbeitungsfunktionen des Grafik Geräts erzeugt.
2.  Überprüfen Sie, ob der Presenter diesen Medientyp als Renderingformat verwenden kann. Im folgenden finden Sie einige Dinge, die Sie überprüfen müssen, obwohl ihre Implementierung möglicherweise eigene Anforderungen erfüllt:

    -   Das Video muss nicht komprimiert werden.
    -   Das Video darf nur progressive Frames enthalten. Überprüfen Sie, ob das [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) Attribut **MFVideoInterlace_Progressive** ist.
    -   Das Format muss mit dem Direct3D-Gerät kompatibel sein.

    Wenn der Typ nicht zulässig ist, kehren Sie zu Schritt 1 zurück, und holen Sie den nächsten vorgeschlagenen Typ des Mischers.

3.  Erstellen Sie einen neuen Medientyp, bei dem es sich um einen Klon des ursprünglichen Typs handelt, und ändern Sie dann die folgenden Attribute:

    -   Legen Sie für die Direct3D-Oberflächen, die Sie zuordnen möchten, das [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) -Attribut gleich der Breite und Höhe fest.
    -   Legen Sie das [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) -Attribut auf " **false**" fest.
    -   Legen Sie das [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) -Attribut auf das Par der Anzeige fest (in der Regel 1:1).
    -   Legen Sie die geometrische Aperture ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) -Attribut) auf ein Rechteck innerhalb der Direct3D-Oberfläche fest. Wenn der Mixer einen Ausgabe Rahmen generiert, wird das Quell Bild auf dieses Rechteck gebliert. Die geometrische Öffnung kann so groß wie die Oberfläche sein, oder es kann sich um ein unter Rechteck innerhalb der Oberfläche handeln. Weitere Informationen finden Sie unter [Quell-und Ziel Rechtecke](#source-and-destination-rectangles).

4.  Um zu testen, ob der Mixer den geänderten Ausgabetyp akzeptiert, müssen Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) mit dem **MFT_SET_TYPE_TEST_ONLY** -Flag aufrufen. Wenn der Mixer den Typ ablehnt, kehren Sie zu Schritt 1 zurück, und rufen Sie den nächsten Typ ab.
5.  Ordnen Sie einen Pool mit Direct3D-Oberflächen zu, wie unter [Zuordnen von Direct3D-Oberflächen](#allocating-direct3d-surfaces)beschrieben Der Mixer verwendet diese Oberflächen, wenn die zusammengesetzten Video Frames gezeichnet werden.
6.  Legen Sie den Ausgabetyp für den Mixer fest, indem Sie [**setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) ohne Flags aufrufen. Wenn der erste aufzurufende **setoutputtype** -Befehl in Schritt 4 erfolgreich war, sollte die-Methode erneut ausgeführt werden.

Wenn der Mixer nicht mehr über Typen verfügt, gibt die [**getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode **MF_E_NO_MORE_TYPES** zurück. Wenn der Presenter keinen geeigneten Ausgabetyp für den Mixer finden kann, kann der Stream nicht gerendert werden. In diesem Fall kann DirectShow oder Media Foundation ein anderes Streamformat ausprobieren. Aus diesem Grund kann der Presenter mehrere **MFVP_MESSAGE_INVALIDATEMEDIATYPE** Nachrichten in einer Zeile erhalten, bis ein gültiger Typ gefunden wird.

Der Mixer zieht das Video automatisch ein, wobei das Pixel Seitenverhältnis (par) der Quelle und des Ziels berücksichtigt wird. Um optimale Ergebnisse zu erzielen, sollten die Breite und Höhe der Oberfläche und die geometrische Öffnung gleich der tatsächlichen Größe sein, die das Video in der Anzeige anzeigen soll. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Diagramm, das einen zusammengesetzten Fram anzeigt, der zu einer Direct3D-Oberfläche führt, die zu einem Fenster führt](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

Der folgende Code zeigt die Gliederung des Prozesses. Einige der Schritte werden in Hilfsfunktionen platziert, die genaue Details, die von den Anforderungen Ihres Presenter abhängen.


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



Weitere Informationen zu Video Medientypen finden Sie unter [Video Medientypen](video-media-types.md).

## <a name="managing-the-direct3d-device"></a>Verwalten des Direct3D-Geräts

Der Presenter erstellt das Direct3D-Gerät und verarbeitet alle Geräte Verluste beim Streaming. Außerdem hostet der Presenter den Direct3D-Geräte-Manager, der es anderen Komponenten ermöglicht, dasselbe Gerät zu verwenden. Beispielsweise verwendet der Mixer das Direct3D-Gerät zum Mischen von Substreams, deinterlace und zum Durchführen von Farbanpassungen. Decoderer können das Direct3D-Gerät für die Video beschleunigte Decodierung verwenden. (Weitere Informationen zur Videobeschleunigung finden Sie unter [DirectX-Videobeschleunigung 2,0](directx-video-acceleration-2-0.md).)

Führen Sie die folgenden Schritte aus, um das Direct3D-Gerät einzurichten:

1.  Erstellen Sie das Direct3D-Objekt durch Aufrufen von **Direct3DCreate9** oder **Direct3DCreate9Ex**.
2.  Erstellen Sie das Gerät durch Aufrufen von **IDirect3D9:: createdevice** oder **IDirect3D9Ex:: createdevice**.
3.  Erstellen Sie den Geräte-Manager durch Aufrufen von [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).
4.  Legen Sie das Gerät im Geräte-Manager durch Aufrufen von [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)fest.

Wenn eine andere Pipeline Komponente den Geräte-Manager benötigt, ruft Sie [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf dem EVR auf und gibt **MR_VIDEO_ACCELERATION_SERVICE** für die Dienst-GUID an. Der EVR übergibt die Anforderung an den Presenter. Nachdem das Objekt den [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Zeiger abgerufen hat, kann es durch Aufrufen von [**IDirect3DDeviceManager9:: opendevicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle)ein Handle für das Gerät abrufen. Wenn das Objekt das Gerät verwenden muss, übergibt es das Geräte Handle an die [**IDirect3DDeviceManager9:: lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) -Methode, die einen **IDirect3DDevice9** -Zeiger zurückgibt.

Nachdem das Gerät erstellt wurde und der Presenter das Gerät zerstört und ein neues erstellt hat, muss der Presenter [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) erneut aufrufen. Die **ResetDevice** -Methode macht alle vorhandenen Geräte Handles ungültig, was dazu führt, dass [**lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE** zurückgibt. Mit diesem Fehlercode wird anderen Objekten das Gerät signalisiert, dass ein neues Geräte Handle geöffnet werden soll. Weitere Informationen zum Verwenden des Geräte-Managers finden Sie unter [Direct3D Device Manager](direct3d-device-manager.md).

Der Presenter kann das Gerät im Fenstermodus oder im Vollbildmodus im exklusiven Modus erstellen. Für den Fenstermodus sollten Sie eine Möglichkeit zur Angabe des Videofensters für die Anwendung bereitstellen. Der Standard Presenter implementiert zu diesem Zweck die [**IMF videodisplaycontrol:: setvideowindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) -Methode. Sie müssen das Gerät erstellen, wenn der Presenter erstmalig erstellt wird. Normalerweise kennen Sie nicht alle Geräteparameter zu diesem Zeitpunkt, z. b. das Fenster oder das Hintergrund Puffer Format. Sie können ein temporäres Gerät erstellen und es später&ersetzen \# . denken Sie daran, dass Sie [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) für den Geräte-Manager aufrufen.

Wenn Sie ein neues Gerät erstellen oder **IDirect3DDevice9:: Reset** oder **IDirect3DDevice9Ex:: reltex** auf einem vorhandenen Gerät aufzurufen, senden Sie ein [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) Ereignis an den EVR. Dieses Ereignis benachrichtigt den EVR, dass er den Medientyp erneut aushandeln soll. Der EVR ignoriert die Ereignis Parameter für dieses Ereignis.

### <a name="allocating-direct3d-surfaces"></a>Zuordnen von Direct3D-Flächen

Nachdem der Presenter den Medientyp festgelegt hat, kann er die Direct3D-Oberflächen zuordnen, die der Mixer zum Schreiben der Video Frames verwendet. Die Oberfläche muss dem Medientyp des Presenter entsprechen:

-   Das Oberflächen Format muss mit dem Medien Untertyp identisch sein. Wenn der Untertyp z. b. **MFVideoFormat_RGB24** ist, muss das Oberflächen Format **D3DFMT_X8R8G8B8** sein. Weitere Informationen zu Untertypen und Direct3D-Formaten finden Sie unter [Video Untertyp-GUIDs](video-subtype-guids.md).
-   Die Breite und Höhe der Oberfläche muss den Dimensionen entsprechen, die im [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) -Attribut des Medientyps angegeben sind.

Die empfohlene Vorgehensweise zum Zuordnen von Oberflächen hängt davon ab, ob der Presenter im Fenster oder voll Bildschirm ausgeführt wird.

Wenn das Direct3D-Gerät in einem Fenster angezeigt wird, können Sie mehrere Austausch Ketten erstellen, die jeweils über einen einzelnen Hintergrund Puffer verfügen. Bei diesem Ansatz können Sie jede Oberfläche unabhängig präsentieren, da die Darstellung einer Swapkette nicht die anderen Swapketten beeinträchtigt. Der Mixer kann Daten auf eine Oberfläche schreiben, während eine andere Oberfläche für die Präsentation geplant ist.

Entscheiden Sie zuerst, wie viele Austausch Ketten erstellt werden sollen. Mindestens drei wird empfohlen. Gehen Sie für jede Austausch Kette wie folgt vor:

1.  Rufen Sie **IDirect3DDevice9:: kreateadditionalswapchain** auf, um die Austausch Kette zu erstellen.
2.  Aufrufen von **IDirect3DSwapChain9:: GetBackBuffer** zum Abrufen eines Zeigers auf die Hintergrund Puffer Oberfläche der Austausch Kette.
3.  Aufrufen von [**mfcreatevideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) und übergeben eines Zeigers auf die-Oberfläche. Diese Funktion gibt einen Zeiger auf ein Video Sample-Objekt zurück. Das Video Sample-Objekt implementiert die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle, und der Presenter verwendet diese Schnittstelle, um die Oberfläche an den Mixer zu übermitteln, wenn der Presenter die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode des Mischers aufruft. Weitere Informationen zum Video Sample-Objekt finden Sie unter [Video Samples (Videobeispiele](video-samples.md)).
4.  Speichert den [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeiger in einer Warteschlange. Der Presenter Ruft bei der Verarbeitung Beispiele aus dieser Warteschlange ab, wie in [Verarbeiten der Ausgabe](#processing-output)beschrieben.
5.  Bewahren Sie einen Verweis auf den **IDirect3DSwapChain9** -Zeiger auf, damit die SwapChain nicht freigegeben wird.

Im Vollbildmodus (exklusiv) kann das Gerät nicht mehr als eine SwapChain aufweisen. Diese austauschkette wird implizit erstellt, wenn Sie das voll Bild Gerät erstellen. Die SwapChain kann über mehr als einen Hintergrund Puffer verfügen. Wenn Sie jedoch einen backpuffer darstellen, während Sie in einen anderen Hintergrund Puffer in derselben Swapkette schreiben, gibt es keine einfache Möglichkeit, die beiden Vorgänge zu koordinieren. Dies liegt an der Art und Weise, in der Direct3D das Oberflächen Flipping implementiert. Wenn Sie "Present" aufgerufen haben, aktualisiert der Grafiktreiber die Surface-Zeiger im Grafikspeicher. Wenn Sie **IDirect3DSurface9** -Zeiger mit dem Befehl " **Present**" speichern, zeigen Sie auf verschiedene Puffer, nachdem der **aktuelle** Rückruf zurückgegeben wurde.

Die einfachste Möglichkeit besteht darin, ein Video Beispiel für die Swapkette zu erstellen. Wenn Sie diese Option auswählen, führen Sie dieselben Schritte aus, die für den Fenstermodus ausgeführt werden. Der einzige Unterschied besteht darin, dass die Beispiel Warteschlange ein einzelnes Video Beispiel enthält. Eine andere Möglichkeit besteht darin, Offscreen-Oberflächen zu erstellen und Sie dann in den Hintergrund Puffer zu versetzen. Die von Ihnen erstellten Oberflächen müssen die [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) -Methode unterstützen, die der Mixer zum Zusammenführen der Ausgabe Frames verwendet.

### <a name="tracking-samples"></a>Überwachungsbeispiele

Wenn der Presenter die Videobeispiele zuerst ordnet, werden diese in einer Warteschlange platziert. Der Presenter zeichnet sich aus dieser Warteschlange aus, wenn er einen neuen Frame vom Mixer erhalten muss. Nachdem der Mixer den Frame ausgegeben hat, verschiebt der Presenter das Beispiel in eine zweite Warteschlange. Die zweite Warteschlange ist für Beispiele, die auf Ihre geplanten Präsentations Zeiten warten.

Um die Nachverfolgung des Status der einzelnen Beispiele zu vereinfachen, implementiert das Video Sample-Objekt die [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Schnittstelle. Sie können diese Schnittstelle wie folgt verwenden:

1.  Implementieren Sie die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle in Ihrem Presenter.
2.  Bevor Sie ein Beispiel in der geplanten Warteschlange platzieren, Fragen Sie das Video Sample-Objekt für die [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Schnittstelle ab.

3.  Rufen Sie [**imftrackedsample:: abtallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) mit einem Zeiger auf Ihre Rückruf Schnittstelle auf.
4.  Wenn das Beispiel zur Präsentation bereit ist, entfernen Sie es aus der geplanten Warteschlange, stellen Sie es bereit, und geben Sie alle Verweise auf das Beispiel frei.
5.  Das Beispiel ruft den Rückruf auf. (Das Sample-Objekt wird in diesem Fall nicht gelöscht, da es einen Verweis Zähler auf sich selbst enthält, bis der Rückruf aufgerufen wird.)
6.  Geben Sie im Rückruf das Beispiel in die verfügbare Warteschlange ein.

Zum Nachverfolgen von Beispielen ist kein Presenter erforderlich, um [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) zu verwenden. Sie können jede Technik implementieren, die für Ihren Entwurf am besten geeignet ist. Ein Vorteil von **imftrackedsample** besteht darin, dass Sie die Planungs-und Renderingfunktionen von Presenter in Hilfsobjekte verschieben können. diese Objekte benötigen keinen besonderen Mechanismus zum Rückrufe an den Presenter, wenn Sie Videobeispiele veröffentlichen, da das Beispiel Objekt diesen Mechanismus bereitstellt.

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



Rufen Sie im Rückruf [**imfasynkresult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) für das asynchrone Ergebnis Objekt auf, um einen Zeiger auf das Beispiel abzurufen:


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

    /*** Begin lock **_/

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

    /_*_ End lock _*_/

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



## <a name="processing-output"></a>Ausgabe wird verarbeitet

Immer wenn der Mixer ein neues Eingabe Beispiel empfängt, sendet der EVR eine _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY**-Meldung an den Presenter. Diese Meldung gibt an, dass der Mixer möglicherweise über einen neuen Videorahmen verfügt. Als Antwort ruft der Presenter [**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer auf. Wenn die Methode erfolgreich ist, plant der Presenter das Beispiel für die Präsentation.

Um die Ausgabe vom Mixer zu erhalten, führen Sie die folgenden Schritte aus:

1.  Überprüfen Sie den Uhrzustand. Wenn die Uhr angehalten ist, ignorieren Sie die **MFVP_MESSAGE_PROCESSINPUTNOTIFY** Meldung, es sei denn, dies ist der erste Videoframe. Wenn die Uhr ausgeführt wird, oder wenn es sich um den ersten Videoframe handelt, fahren Sie fort.
2.  Holen Sie sich ein Beispiel aus der Warteschlange mit verfügbaren Beispielen. Wenn die Warteschlange leer ist, bedeutet dies, dass alle zugeordneten Beispiele aktuell für die Darstellung geplant sind. Ignorieren Sie in diesem Fall die **MFVP_MESSAGE_PROCESSINPUTNOTIFY** Meldung zu diesem Zeitpunkt. Wenn das nächste Beispiel verfügbar wird, wiederholen Sie die hier aufgeführten Schritte.
3.  (Optional) Wenn die Uhr verfügbar ist, rufen Sie die aktuelle Uhrzeit (*T1*) ab, indem Sie [**imfclock:: getcorrelatedtime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)aufrufen.
4.  Rückrufe [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer. Wenn **ProcessOutput** erfolgreich ist, enthält das Beispiel einen Videoframe. Wenn die Methode fehlschlägt, überprüfen Sie den Rückgabecode. Die folgenden Fehlercodes aus **ProcessOutput** sind keine kritischen Fehler:

    

    | Fehlercode                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | Der Mixer benötigt mehr Eingaben, bevor er einen neuen Ausgabe Frame erzeugt.<br/> Wenn Sie diesen Fehlercode erhalten, überprüfen Sie, ob der EVR das Ende des Streams erreicht hat, und reagieren Sie entsprechend der Beschreibung am [Ende des Streams](#end-of-stream). Andernfalls ignorieren Sie diese **MF_E_TRANSFORM_NEED_MORE_INPUT** Meldung. Der EVR sendet einen weiteren, wenn der Mixer mehr Eingaben erhält.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | Der Ausgabetyp des Mischers wurde ungültig, möglicherweise aufgrund einer upstreamänderung im Format.<br/> Wenn Sie diesen Fehlercode erhalten, legen Sie den Medientyp des Presenter auf **null** fest. Der EVR fordert ein neues Format an.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | Für den Mixer ist ein neuer Medientyp erforderlich.<br/> Wenn Sie diesen Fehlercode erhalten, wiederholen Sie den Ausgabetyp des Mischers, wie in den [Aushandeln von Formaten](#negotiating-formats)beschrieben.<br/>                                                                                                                                                                                                        |

    

     

    Wenn [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) erfolgreich ist, fahren Sie fort.

5.  (Optional) Wenn die Uhr verfügbar ist, erhalten Sie die aktuelle Uhrzeit (*T2*). Die vom Mixer eingeführte Latenzzeit ist (*T2*  -  *T1*). Senden Sie ein **EC_PROCESSING_LATENCY** Ereignis mit diesem Wert an den EVR. Der EVR verwendet diesen Wert für die Qualitätskontrolle. Wenn keine Uhr verfügbar ist, gibt es keinen Grund, das **EC_PROCESSING_LATENCY** Ereignis zu senden.
6.  (Optional) Fragen Sie das Beispiel nach [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab, und nennen Sie [**imftrackedsample::**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) Set Sample, wie in nach [Verfolgungs Beispielen](#tracking-samples)beschrieben.
7.  Planen Sie das Beispiel für die Präsentation.

Diese Schritt Sequenz kann beendet werden, bevor der Presenter eine Ausgabe vom Mixer erhält. Um sicherzustellen, dass keine Anforderungen gelöscht werden, sollten Sie die gleichen Schritte wiederholen, wenn Folgendes geschieht:

-   Die [**imfclockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) -Methode oder die **imfclockstaatink:: onclockstart** -Methode des Presenter wird aufgerufen. Dies behandelt die Groß-/Kleinschreibung, in der der Mixer Eingaben ignoriert, da die Uhr angehalten wird (Schritt 1).
-   Der [**imftrackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Rückruf wird aufgerufen. Dies behandelt den Fall, in dem der Mixer Eingaben empfängt, aber alle Videobeispiele des Presenter verwendet werden (Schritt 2).

Die folgenden Codebeispiele zeigen diese Schritte ausführlicher. Der Presenter Ruft die- `ProcessInputNotify` Methode auf (wie im folgenden Beispiel gezeigt), wenn die **MFVP_MESSAGE_PROCESSINPUTNOTIFY** Nachricht abgerufen wird.


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



Diese `ProcessInputNotify` Methode legt ein boolesches Flag fest, um die Tatsache aufzuzeichnen, dass der Mixer über neue Eingaben verfügt. Anschließend wird die- `ProcessOutputLoop` Methode aufgerufen, wie im nächsten Beispiel gezeigt. Diese Methode versucht, so viele Beispiele wie möglich vom Mixer abzurufen:


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



Die `ProcessOutput` im nächsten Beispiel gezeigte-Methode versucht, einen einzelnen Videoframe aus dem Mixer zu erhalten. Wenn kein Videoframe verfügbar ist, `ProcessSample` gibt S_FALSE oder einen Fehlercode zurück, von dem beide die Schleife unterbrechen `ProcessOutputLoop` . Die meisten Aufgaben werden innerhalb der-Methode durchgeführt `ProcessOutput` :


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

-   Bei der *m_SamplePool* Variablen handelt es sich um ein Auflistungs Objekt, das die Warteschlange von verfügbaren Videobeispielen enthält. Die-Methode des-Objekts `GetSample` gibt **MF_E_SAMPLEALLOCATOR_EMPTY** zurück, wenn die Warteschlange leer ist.
-   Wenn die [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode des Mischers MF_E_TRANSFORM_NEED_MORE_INPUT zurückgibt, bedeutet dies, dass der Mixer keine Ausgabe mehr ausgeben kann, sodass der Presenter das *m_fSampleNotify* -Flag löscht.
-   Die- `TrackSample` Methode, mit der der [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Rückruf festgelegt wird, wird im Abschnitt nach [Verfolgungs Beispielen](#tracking-samples)gezeigt.

### <a name="repainting-frames"></a>Neuzeichnen von Frames

Gelegentlich muss der Presenter möglicherweise den neuesten Videoframe neu zeichnen. Der Standard Presenter zeichnet den Frame z. b. in den folgenden Situationen:

-   Im Fenstermodus als Reaktion auf **WM_PAINT** vom Anwendungsfenster empfangene Nachrichten. Weitere Informationen finden Sie unter [**IMF videodisplaycontrol:: repaintvideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   , Wenn das Ziel Rechteck geändert wird, wenn die Anwendung [**IMF videodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)aufruft.

Führen Sie die folgenden Schritte aus, um den Mixer aufzufordern, den letzten Frame neu zu erstellen:

1.  Holen Sie sich ein Video Beispiel aus der Warteschlange.
2.  Fragen Sie das Beispiel nach der [**imbodesiredsample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) -Schnittstelle ab.
3.  [**Imfdesiredsample:: setdesiredsampletimeandduration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration)aufrufen. Geben Sie den Zeitstempel des letzten Video Rahmens an. (Sie müssen diesen Wert Zwischenspeichern und für jeden Frame aktualisieren.)
4.  Ruft [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer auf.

Wenn Sie einen Frame neu zeichnen, können Sie die Präsentations Uhr ignorieren und den Frame sofort darstellen.

### <a name="scheduling-samples"></a>Beispiele für Zeitplanung

Video Frames können jederzeit den EVR erreichen. Der Presenter ist für die Darstellung der einzelnen Frames zur richtigen Zeit basierend auf dem Zeitstempel des Frames verantwortlich. Wenn der Presenter ein neues Beispiel aus dem Mixer erhält, wird das Beispiel in die geplante Warteschlange eingefügt. In einem separaten Thread ruft der Presenter das erste Beispiel kontinuierlich vom Anfang der Warteschlange ab und bestimmt, ob Folgendes möglich ist:

-   Stellen Sie das Beispiel dar.
-   Behalten Sie das Beispiel in der Warteschlange, da es frühzeitig ist.
-   Verwerfen Sie das Beispiel, weil es spät ist. Obwohl Sie nach Möglichkeit das Löschen von Frames vermeiden sollten, ist es möglicherweise erforderlich, wenn der Presenter ständig dahinter stürzt.

Um den Zeitstempel für einen Videorahmen abzurufen, nennen Sie [**imfsample:: getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) im Video Beispiel. Der Zeitstempel ist relativ zur Präsentations Uhr des EVR. Um die aktuelle Uhrzeit abzurufen, wenden Sie [**imfclock:: getcorrelatedtime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime)an. Wenn der EVR keine Präsentations Uhr hat oder wenn ein Beispiel keinen Zeitstempel hat, können Sie das Beispiel sofort nach dem Get-Vorgang darstellen.

Um die Dauer der einzelnen Stichproben abzurufen, müssen Sie [**imfsample:: getsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration)aufrufen. Wenn das Beispiel keine Dauer hat, können Sie die [**mfframerateesaveragetimeperframe**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) -Funktion verwenden, um die Dauer der Framerate zu berechnen.

Beachten Sie beim Planen von Beispielen Folgendes:

-   Wenn die Wiedergabe Rate schneller oder langsamer als die normale Geschwindigkeit ist, wird die Uhr schneller oder langsamer ausgeführt. Dies bedeutet, dass der Zeitstempel in einem Beispiel immer die richtige Zielzeit in Relation zur Präsentationszeit ergibt. Wenn Sie die Präsentations Zeiten jedoch in eine andere Uhrzeit übersetzen (z. b. den Leistungs-Leistungs-Leistungs-Leistungs-Leistungs-Leistungs-Leistungs Bewert), müssen Sie die Zeiten basierend auf der Taktfrequenz skalieren. Wenn sich die Taktfrequenz ändert, ruft der EVR die [**imfclockstaatink:: onclockertrate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) -Methode des Presenter auf.
-   Die Wiedergabe Rate kann für die umgekehrte Wiedergabe negativ sein. Wenn die Wiedergabe Rate negativ ist, wird die Präsentations Uhr rückwärts ausgeführt. Anders ausgedrückt: Zeit *n* + 1 tritt vor der Zeit *n* auf.

Im folgenden Beispiel wird berechnet, wie früh oder spät ein Beispiel relativ zur Präsentations Uhr ist:


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



Die Präsentationszeit wird normalerweise durch die Systemuhr oder den audiorenderer gesteuert. (Der audiorenderer leitet die Uhrzeit von der Rate ab, mit der die Audiokarte Audiodaten verbraucht.) Im Allgemeinen wird die Präsentations Uhr nicht mit der Aktualisierungsrate des Monitors synchronisiert.

Wenn Ihre Direct3D Presentation-Parameter für das Präsentations Intervall **D3DPRESENT_INTERVAL_DEFAULT** oder **D3DPRESENT_INTERVAL_ONE** angeben, wartet der **aktuelle** Vorgang auf die vertikale neuverfolgung des Monitors. Dies ist eine einfache Möglichkeit, das Zerreißen zu verhindern, aber die Genauigkeit des Planungs Algorithmus zu verringern. Wenn das Präsentations Intervall **D3DPRESENT_INTERVAL_IMMEDIATE** ist, wird die **aktuelle** Methode sofort ausgeführt. Dies führt zu einem ausreißenden, es sei denn, der Zeit Planungs Algorithmus ist genau genug, den **Sie nur während** des vertikalen zurückverfolgen-Zeitraums aufzurufen.

Die folgenden Funktionen können Ihnen helfen, genaue Zeit Steuerungsinformationen zu erhalten:

-   **IDirect3DDevice9:: getrasterstatus** gibt Informationen zum Raster zurück, einschließlich der aktuellen Überprüfungs Zeile und der Angabe, ob sich das Raster im vertikalen leeren Zeitraum befindet.
-   **Dwmgetcompositiontiminginfo** gibt Zeit Steuerungsinformationen für den Desktop Fenster-Manager zurück. Diese Informationen sind nützlich, wenn die Desktop Komposition aktiviert ist.

### <a name="presenting-samples"></a>Präsentieren von Beispielen

In diesem Abschnitt wird davon ausgegangen, dass Sie eine separate austauschkette für jede Oberfläche erstellt haben, wie unter [Zuordnen von Direct3D-Oberflächen](#allocating-direct3d-surfaces) Um ein Beispiel zu präsentieren, können Sie die SwapChain aus dem Video Beispiel wie folgt erstellen:

1.  Aufrufen von [**imfsample:: getbufferbyindex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) für das Video Beispiel zum Abrufen des Puffers.
2.  Abfragen des Puffers für die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle.
3.  Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) zum Abrufen der **IDirect3DSurface9** -Schnittstelle der Direct3D-Oberfläche. (Sie können diesen Schritt und den vorherigen Schritt in einem Schritt kombinieren, indem Sie [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)aufrufen.)
4.  Aufrufen von **IDirect3DSurface9:: getContainer** auf der-Oberfläche, um einen Zeiger auf die Swapkette zu erhalten.
5.  **IDirect3DSwapChain9::P erneut** an die Swapkette gesendet.

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



### <a name="source-and-destination-rectangles"></a>Quell-und Ziel Rechtecke

Das *Quell Rechteck* ist der Teil des Video Frames, der angezeigt werden soll. Sie wird relativ zu einem normalisierten Koordinatensystem definiert, in dem der gesamte Videorahmen ein Rechteck mit den Koordinaten {0, 0, 1, 1} einnimmt. Das *Ziel Rechteck* ist der Bereich innerhalb der Ziel Oberfläche, in dem der Videorahmen gezeichnet wird. Der Standard Presenter ermöglicht einer Anwendung, diese Rechtecke durch Aufrufen von [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)festzulegen.

Es gibt mehrere Optionen für das Anwenden von Quell-und Ziel Rechtecke. Die erste Option besteht darin, den Mixer darauf anzuwenden:

-   Legen Sie das Quell Rechteck mithilfe des [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) -Attributs fest. Der Mixer wendet das Quell Rechteck an, wenn es das Video auf der Ziel Oberfläche Blicke. Das standardmäßige Quell Rechteck des Mischers ist der gesamte Frame.
-   Legen Sie das Ziel Rechteck als geometrische Öffnung im Ausgabetyp des Mischers fest. Weitere Informationen finden Sie unter [Aushandeln von Formaten](#negotiating-formats).

Die zweite Option ist das Anwenden der Rechtecke bei der **IDirect3DSwapChain9::P erneut gesendet** , indem die Parameter *psourcerect* und *pdestrect* in der **aktuellen** Methode angegeben werden. Diese Optionen können kombiniert werden. Beispielsweise können Sie das Quell Rechteck auf dem Mixer festlegen, aber das Ziel Rechteck in der **aktuellen** Methode anwenden.

Wenn die Anwendung das Ziel Rechteck ändert oder die Größe des Fensters ändert, müssen Sie möglicherweise neue Oberflächen zuordnen. Wenn dies der Fall ist, müssen Sie darauf achten, diesen Vorgang mit Ihrem Zeit Planungs Thread zu synchronisieren. Leeren Sie die Planungs Warteschlange, und verwerfen Sie die alten Beispiele, bevor Sie neue Oberflächen

### <a name="end-of-stream"></a>Ende des Streams

Wenn jeder Eingabedaten Strom im EVR beendet wurde, sendet der EVR eine **MFVP_MESSAGE_ENDOFSTREAM** Meldung an den Presenter. An dem Punkt, an dem Sie die Nachricht erhalten, kann es jedoch noch einige Video Frames geben, die verarbeitet werden müssen. Bevor Sie auf das Ende der Stream-Nachricht reagieren, müssen Sie die gesamte Ausgabe des Mischers ableiten und alle verbleibenden Frames darstellen. Nachdem der letzte Frame angezeigt wurde, senden Sie ein **EC_COMPLETE** Ereignis an den EVR.

Das nächste Beispiel zeigt eine Methode, die das **EC_COMPLETE** Ereignis sendet, wenn verschiedene Bedingungen erfüllt sind. Andernfalls wird S_OK zurückgegeben, ohne das Ereignis zu senden:


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

-   Wenn die *m_fSampleNotify* Variable den Wert **true** aufweist, bedeutet dies, dass der Mixer über einen oder mehrere Frames verfügt, die noch nicht verarbeitet wurden. (Ausführliche Informationen finden Sie unter [Verarbeiten der Ausgabe](#processing-output).)
-   Die *m_fEndStreaming* Variable ist ein boolesches Flag, dessen ursprünglicher Wert **false** ist. Der Presenter legt das-Flag auf **true** fest, wenn der EVR die **MFVP_MESSAGE_ENDOFSTREAM** Nachricht sendet.
-   `AreSamplesPending`Es wird davon ausgegangen, dass die Methode " **true** " zurückgibt, solange mindestens ein Rahmen in der geplanten Warteschlange wartet.

Legen Sie in der [**imfvideopresenter::P rocess Message**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) -Methode *m_fEndStreaming* auf **true** fest, und geben Sie an, `CheckEndOfStream` Wenn der EVR die **MFVP_MESSAGE_ENDOFSTREAM** Nachricht sendet:


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



Außerdem wird aufgerufen, `CheckEndOfStream` Wenn die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode von Mixer **MF_E_TRANSFORM_NEED_MORE_INPUT** zurückgibt. Dieser Fehlercode gibt an, dass der Mixer keine weiteren Eingabe Beispiele hat (siehe [Verarbeitung der Ausgabe](#processing-output)).

## <a name="frame-stepping"></a>Frame Schritt Schritt

Der EVR ist so konzipiert, dass Frame Step in DirectShow und Bereinigungs in Media Foundation unterstützt wird. Frame-Step und Bereinigungs sind konzeptionell ähnlich. In beiden Fällen fordert die Anwendung einen Video Frame gleichzeitig an. Intern verwendet der Presenter denselben Mechanismus zum Implementieren beider Features.

Das schrittweise Ausführen von Frame Works in DirectShow funktioniert wie folgt:

-   Die Anwendung ruft [**ivideoframestep:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step)auf. Die Anzahl der Schritte wird im Parameter " *dwsteps* " angegeben. Der EVR sendet eine **MFVP_MESSAGE_STEP** Meldung an den Presenter, wobei der Message-Parameter (*ulparam*) die Anzahl von Schritten ist.
-   Wenn die Anwendung [**ivideoframestep:: cancelstep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) aufruft oder den Diagramm Zustand ändert (wird ausgeführt, angehalten oder beendet), sendet der EVR eine **MFVP_MESSAGE_CANCELSTEP** Nachricht.

Das Scrubbing in Media Foundation funktioniert wie folgt:

-   Die Anwendung legt die Wiedergabe Rate auf NULL fest, indem [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)aufgerufen wird.
-   Um einen neuen Frame zu erzeugen, ruft die Anwendung [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) an der gewünschten Position auf. Der EVR sendet eine **MFVP_MESSAGE_STEP** Nachricht mit *ulparam* gleich 1.
-   Um das Scrubbing zu verhindern, legt die Anwendung die Wiedergabe Rate auf einen Wert ungleich 0 (null) fest. Der EVR sendet die **MFVP_MESSAGE_CANCELSTEP** Nachricht.

Nach dem Empfang der **MFVP_MESSAGE_STEP** Nachricht wartet der Presenter, bis der Zielframe eintrifft. Wenn die Anzahl der Schritte *N* ist, verwirft der Presenter die nächsten (*n* -1) Beispiele und zeigt das *N* -te Beispiel an. Wenn der Presenter den Rahmen Schritt abgeschlossen hat, sendet er ein [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) Ereignis an den EVR, wobei *lParam1* auf **false** festgelegt ist. Wenn die Wiedergabe Rate NULL ist, sendet der Presenter außerdem ein [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) Ereignis. Wenn der EVR die Frame Ausführung abbricht, während ein Rahmen Schritt noch aussteht, sendet der Presenter ein **EC_STEP_COMPLETE** Ereignis, wobei *lParam1* auf **true** festgelegt ist.

Die Anwendung kann den Schritt oder das Bereinigen mehrmals durchlaufen, sodass der Presenter möglicherweise mehrere **MFVP_MESSAGE_STEP** Meldungen empfängt, bevor er eine **MFVP_MESSAGE_CANCELSTEP** Nachricht erhält. Außerdem kann der Presenter die **MFVP_MESSAGE_STEP** Nachricht empfangen, bevor die Uhr beginnt oder während die Uhr ausgeführt wird.

### <a name="implementing-frame-stepping"></a>Implementieren von Frame-Stepping

In diesem Abschnitt wird ein Algorithmus zum Implementieren von Frame-Stepping beschrieben. Der Frame Step-Algorithmus verwendet die folgenden Variablen:

-   *step_count*. Eine ganze Zahl ohne Vorzeichen, die die Anzahl der Schritte im aktuellen Frame-Schritt Vorgang angibt.
-   *step_queue*. Eine Warteschlange von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeigern.
-   *step_state*. Der Präsentator kann jederzeit einen der folgenden Zustände in Bezug auf die Frame-Schrittfolge aufweisen: 

    | State         | BESCHREIBUNG                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Kein Frame Schritt Schritt.                                                                                                                                                                                             |
    | WAITING       | Der Presenter hat die **MFVP_MESSAGE_STEP** Nachricht empfangen, aber die Uhr wurde nicht gestartet.                                                                                                                  |
    | PENDING (AUSSTEHEND)       | Der Presenter hat die **MFVP_MESSAGE_STEP** Nachricht empfangen, und die Uhr wurde gestartet, aber der Presenter wartet darauf, den Zielframe zu empfangen.                                                             |
    | Findet     | Der Präsentator hat den Zielframe empfangen und ihn für die Präsentation eingeplant, aber der Frame wurde nicht präsentiert.                                                                                        |
    | Ganz      | Der Präsentator hat den Zielframe dargestellt und das [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) -Ereignis gesendet und wartet auf die nächste **MFVP_MESSAGE_STEP** oder **MFVP_MESSAGE_CANCELSTEP** Meldung. |

    

     

    Diese Zustände sind unabhängig von den präsentatorzuständen, die im Abschnitt [Presenter States](#presenter-states)aufgeführt sind.

Die folgenden Prozeduren sind für den Frame Step-Algorithmus definiert:

Prepareframestep-Prozedur

1.  *Step_count* Inkrement.
2.  Legen Sie *step_state* auf warten fest.
3.  Wenn die Uhr ausgeführt wird, müssen Sie startframestep aufrufen.

Startframestep-Prozedur

1.  Wenn *step_state* auf "warten" festgelegt ist, legen Sie *step_state* auf Pending Nennen Sie für jedes Beispiel in *step_queue* deliverframestepsample.
2.  Wenn *step_state* NOT_STEPPING ist, entfernen Sie alle Beispiele aus *step_queue* , und planen Sie Sie für die Präsentation.

Completeframestep-Prozedur

1.  Legen Sie *step_state* auf Complete fest.
2.  Senden Sie das EC_STEP_COMPLETE-Ereignis mit *lParam1*  =  **false**.
3.  Wenn die Taktrate NULL ist, senden Sie das **EC_SCRUB_TIME** -Ereignis mit der Beispiel Zeit.

Deliverframestepsample-Prozedur

1.  Wenn die Taktfrequenz 0 (null) und *Beispiel Zeit für Zeit*  +  *Stichprobe* ist  <  , verwerfen Sie das Beispiel. Beenden
2.  Wenn *step_state* auf geplant oder fertiggestellt ist, fügen Sie das Beispiel *step_queue* hinzu. Beenden
3.  Dekrement *step_count*.
4.  Wenn *step_count* > 0, verwerfen Sie das Beispiel. Beenden
5.  Wenn *step_state* den Zustand "warten" entspricht, fügen Sie das Beispiel *step_queue* hinzu. Beenden
6.  Planen Sie das Beispiel für die Präsentation.
7.  Legen Sie *step_state* auf geplant fest.

Cancelframestep-Prozedur

1.  Legen Sie *step_state* auf NOT_STEPPING
2.  *Step_count* auf Null zurücksetzen.
3.  Wenn der vorherige Wert von *step_state* gewartet, Ausstehend oder geplant ist, senden Sie EC_STEP_COMPLETE mit *lParam1*  =  **true**.

Diese Prozeduren werden wie folgt aufgerufen:



| Presenter-Nachricht oder-Methode                                                   | Prozedur           |
|-------------------------------------------------------------------------------|---------------------|
| **MFVP_MESSAGE_STEP** Meldung                                               | `PrepareFrameStep`  |
| **MFVP_MESSAGE_STEP** Meldung                                               | `CancelStep`        |
| [**IMF clockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**IMF clockstaatink:: onclockrestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Rückruf                         | `CompleteFrameStep` |
| [**IMF clockstaatink:: onclockstopp**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**IMF clockstaatink:: onclock-trate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

Im folgenden Flussdiagramm werden die Frame-Step-Prozeduren angezeigt.

![Flussdiagramm mit den Pfaden, die mit dem MF \- -Nachrichten Schritt beginnen, \- und der MF \- \- -Nachricht processinputnotify und am Ende "State = Complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Festlegen des Präsentators für den EVR

Nachdem Sie den Presenter implementiert haben, besteht der nächste Schritt darin, den EVR für seine Verwendung zu konfigurieren.

### <a name="setting-the-presenter-in-directshow"></a>Festlegen des Präsentators in DirectShow

Legen Sie in einer DirectShow-Anwendung den Presenter wie folgt auf den EVR fest:

1.  Erstellen Sie den EVR-Filter durch Aufrufen von **CoCreateInstance**. Die CLSID ist **CLSID_EnhancedVideoRenderer**.
2.  Fügen Sie den EVR dem Filter Diagramm hinzu.
3.  Erstellen Sie eine Instanz Ihres Präsentators. Ihr Presenter kann die Standard-COM-Objekt Erstellung über **IClassFactory** unterstützen, dies ist jedoch nicht zwingend erforderlich.
4.  Fragen Sie den EVR-Filter nach der [**imsvideorenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) -Schnittstelle ab.
5.  [**Imfvideorenderer:: initializererderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)aufrufen.

### <a name="setting-the-presenter-in-media-foundation"></a>Festlegen des Präsentators in Media Foundation

In Media Foundation haben Sie mehrere Optionen, je nachdem, ob Sie die "EVR Media Sink" oder das "EVR Activation"-Objekt erstellen. Weitere Informationen zu Aktivierungs Objekten finden Sie unter [Activation Objects](activation-objects.md).

Führen Sie für die EVR-Medien Senke die folgenden Schritte aus:

1.  Rufen Sie [**mfkreatevideorenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) auf, um die Medien Senke zu erstellen.
2.  Erstellen Sie eine Instanz Ihres Präsentators.
3.  Fragen Sie die EVR-Medien Senke für die [**imlvideorenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) -Schnittstelle ab.
4.  [**Imfvideorenderer:: initializererderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)aufrufen.

Führen Sie für das EVR-Aktivierungs Objekt die folgenden Schritte aus:

1.  Rufen Sie [**mfkreatevideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) auf, um das Aktivierungs Objekt zu erstellen.
2.  Legen Sie eines der folgenden Attribute für das Aktivierungs Objekt fest: 

    | Attribut                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Zeiger auf ein Aktivierungs Objekt für den Presenter.<br/> Mit diesem Flag müssen Sie ein Aktivierungs Objekt für den Presenter bereitstellen. Das Aktivierungs Objekt muss die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle implementieren.<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID des Präsentators.<br/> Mit diesem Flag muss der Presenter eine Standard-COM-Objekt Erstellung über **IClassFactory** unterstützen.<br/>                                                                                         |

    

     

3.  Legen Sie optional das [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) -Attribut für das Aktivierungs Objekt fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> <dt>

[Evrpresenter-Beispiel](evrpresenter-sample.md)
</dt> </dl>

 

 
