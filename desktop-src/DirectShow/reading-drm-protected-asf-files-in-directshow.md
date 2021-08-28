---
description: In diesem Thema wird beschrieben, wie Sie Mit DirectShow Mediendateien wiederverspielen, die mit Windows Media Digital Rights Management (DRM) geschützt sind.
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lesen DRM-Protected ASF-Dateien in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178dc0dbaa9a8b8e2e849164106816afc6990c89
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786966"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lesen DRM-Protected ASF-Dateien in DirectShow

In diesem Thema wird beschrieben, wie Sie Mit DirectShow Mediendateien wiederverspielen, die mit Windows Media Digital Rights Management (DRM) geschützt sind.

## <a name="drm-concepts"></a>DRM-Konzepte

Der Schutz einer Mediendatei mit Windows Media DRM umfasst zwei verschiedene Schritte:

-   Der Inhaltsanbieter packt die Datei, d.&a; verschlüsselt die Datei und hängt Lizenzierungsinformationen an den ASF-Dateiheader an. Die Lizenzierungsinformationen enthalten eine URL, über die der Client die Lizenz erhalten kann.
-   Die Clientanwendung erhält eine Lizenz für den Inhalt.

Die Paketierung erfolgt, bevor die Datei verteilt wird. Der Lizenzerwerb erfolgt, wenn der Benutzer versucht, die Datei wieder zu spielen oder zu kopieren. Der Lizenzerwerb kann entweder automatisch *oder* *nicht automatisch sein.* Für den automatischen Erwerb ist keine Interaktion mit dem Benutzer erforderlich. Für den nicht automatischen Erwerb muss die Anwendung ein Browserfenster öffnen und dem Benutzer eine Webseite anzeigen. An diesem Punkt muss der Benutzer möglicherweise eine Art von Informationen für den Inhaltsanbieter bereitstellen. Beide Arten des Lizenzerwerbs erfordern jedoch, dass der Client eine HTTP-Anforderung an einen Lizenzserver sendet.

### <a name="drm-versions"></a>DRM-Versionen

Es sind mehrere Versionen Windows Medien-DRM vorhanden. Aus Sicht einer Clientanwendung können sie in zwei Kategorien unterteilt werden: DRM Version 1 und DRM Version 7 oder höher. (Die zweite Kategorie umfasst die DRM-Versionen 9 und 10 sowie Version 7.) Der Grund für die Kategorisierung von DRM-Versionen auf diese Weise ist, dass Lizenzen der Version 1 anders behandelt werden als Lizenzen ab Version 7. In dieser Dokumentation beträgt der Begriff *Lizenzversion 7* Version 7 oder höher.

Es ist auch wichtig, die DRM-Paketierung von der DRM-Lizenz zu unterscheiden. Wenn die Datei mit Windows Media Rights Manager Version 7 oder höher gepackt wird, kann der DRM-Header zusätzlich zur Lizenz-URL der Version 7 eine Lizenz-URL der Version 1 enthalten. Die Lizenz-URL von Version 1 ermöglicht älteren Playern, die Version 7 nicht unterstützen, das Abrufen einer Lizenz für den Inhalt. Das Gegenteil trifft jedoch nicht zu, sodass eine Datei mit Paketen der Version 1 keine Lizenz-URL der Version 7 enthalten kann.

### <a name="application-security-level"></a>Anwendungssicherheitsebene

Zur Wiedergabe von DRM-geschützten Dateien muss die Clientanwendung mit einer statischen Bibliothek verknüpft sein, die von Microsoft in binärer Form bereitgestellt wird. Diese Bibliothek, die die Anwendung eindeutig identifiziert, wird manchmal als Stubbibliothek bezeichnet. Der Stubbibliothek ist eine Sicherheitsstufe zugewiesen, deren Wert durch den Lizenzvertrag bestimmt wird, den Sie beim Erhalten der Stubbibliothek unterzeichnet haben.

Der Inhaltsanbieter legt eine Mindestsicherheitsstufe fest, die zum Erwerb der Lizenz erforderlich ist. Wenn die Sicherheitsstufe Ihrer Stubbibliothek kleiner als die für den Lizenzserver erforderliche Mindestsicherheitsstufe ist, kann die Anwendung die Lizenz nicht abrufen.

### <a name="individualization"></a>Individualisierung

Um die Sicherheit zu erhöhen, kann eine Anwendung die DRM-Komponenten auf dem Clientcomputer aktualisieren. Dieses Update, das als Individualisierung bezeichnet wird, unterscheidet die Kopie der Anwendung des Benutzers von allen anderen Kopien derselben Anwendung. Der DRM-Header einer geschützten Datei kann eine minimale Individualisierungsstufe angeben. (Weitere Informationen finden Sie in der Dokumentation zu WMRMHeader.IndividualizedVersion im Windows Media Rights Manager SDK.)

Da der Microsoft Individualization Service Informationen des Benutzers verarbeitet, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der Microsoft-Website bereitstellen, bevor Ihre Anwendung individualisiert wird: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Bereitstellen des Softwarezertifikats

Damit die Anwendung die DRM-Lizenz verwenden kann, muss  die Anwendung ein Softwarezertifikat oder einen Schlüssel für den Filter Graph Manager bereitstellen. Dieser Schlüssel ist in einer statischen Bibliothek enthalten, die für die Anwendung individualisiert ist. Informationen zum Abrufen der individualisierten Bibliothek finden Sie unter Abrufen der erforderlichen [DRM-Bibliothek](../wmformat/obtaining-the-required-drm-library.md) in der Windows Media Format SDK-Dokumentation.

Führen Sie zum Bereitstellen des Softwareschlüssels die folgenden Schritte aus:

1.  Link zur statischen Bibliothek.
2.  Implementieren Sie die **IServiceProvider-Schnittstelle.**
3.  Fragen Sie den Filter Graph Manager für die [**IObjectWithSite-Schnittstelle**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) ab.
4.  Rufen [**Sie IObjectWithSite::SetSite mit**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) einem Zeiger auf Ihre Implementierung von **IServiceProvider auf.**
5.  Der Filter Graph-Manager aufruft **IServiceProvider::QueryService** und gibt **IID \_ IWMReader** als Dienstbezeichner an.
6.  Rufen Sie in Ihrer **Implementierung von QueryService** [**WMCreateCertificate auf,**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) um den Softwareschlüssel zu erstellen.

Der folgende Code zeigt, wie die **QueryService-Methode implementiert** wird:


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



Der folgende Code zeigt, wie [**SetSite im**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) Filter-manager Graph wird:


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a>Erstellen der Graph

Führen Sie die folgenden Schritte aus, um eine DURCH DRM geschützte ASF-Datei wiederderherzustellen:

1.  Erstellen Sie [den Filter Graph Manager,](filter-graph-manager.md) und verwenden Sie die [**IMediaEventEx-Schnittstelle,**](/windows/desktop/api/Control/nn-control-imediaeventex) um sich für Graphereignisse zu registrieren.
2.  Rufen [**Sie CoCreateInstance auf,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um eine neue Instanz des [WM ASF-Leserfilters zu](wm-asf-reader-filter.md) erstellen.
3.  Rufen [**Sie IFilterGraph::AddFilter auf,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) um dem Filterdiagramm den Filter hinzuzufügen.
4.  Fragen Sie den Filter für die [**IFileSourceFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) ab.
5.  Rufen [**Sie IFileSourceFilter::Load mit**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) der URL der Datei auf.
6.  Behandeln [**von EC \_ WMT \_ EVENT-Ereignissen.**](ec-wmt-event.md)
7.  Fragen Sie beim ersten [**EC \_ WMT \_ EVENT-Ereignis**](ec-wmt-event.md) den [WM ASF-Readerfilter](wm-asf-reader-filter.md) für die **IServiceProvider-Schnittstelle** ab.
8.  Rufen **Sie IServiceProvider::QueryService auf,** um einen Zeiger auf die [**IWMDRMReader-Schnittstelle zu**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) erhalten.
9.  Rufen [**Sie IGraphBuilder::Render auf,**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) um die Ausgabepins des [WM ASF-Readerfilters zu](wm-asf-reader-filter.md) rendern.

> [!Note]  
> Rufen Sie beim Öffnen einer DRM-geschützten Datei [**nicht IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) auf, um das Filterdiagramm zu erstellen. Der WM ASF-Readerfilter kann erst dann eine Verbindung mit anderen Filtern herstellen, wenn die DRM-Lizenz erworben wurde. Für diesen Schritt muss die Anwendung die [**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) verwenden, die wie in den Schritten 7 bis 8 beschrieben aus dem Filter erhalten werden muss. Daher müssen Sie den Filter erstellen und dem Diagramm hinzufügen.

 

> [!Note]  
> Es ist wichtig, sich für Graphereignisse (Schritt 1) zu registrieren, bevor Sie dem Diagramm den [WM ASF-Readerfilter](wm-asf-reader-filter.md) hinzufügen (Schritt 3), da die Anwendung die [**EC \_ WMT \_ EVENT-Ereignisse verarbeiten**](ec-wmt-event.md) muss. Die Ereignisse werden gesendet, wenn [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) aufgerufen wird (Schritt 5).

 

Der folgende Code zeigt, wie sie das Diagramm erstellen:


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```




| C++ | 
|-----|
| <pre><code>            if (FAILED(hr))            {                goto done;            }            hr = RenderOutputPins(pGraph, m_pReader);    }    else    {        // Not a Windows Media file, so just render the standard way.        hr = pGraph-&gt;RenderFile(pwszFile, NULL);    }done:    return hr;}</code></pre> | 




Im vorherigen Code listet die Funktion die Ausgabepins im `RenderOutputPins` [WM ASF-Readerfilter](wm-asf-reader-filter.md) auf und ruft [**IGraphBuilder::Render für**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) jeden Pin auf.


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



Der folgende Code zeigt, wie Sie einen Zeiger auf die [**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) aus dem [WM ASF-Reader erhalten:](wm-asf-reader-filter.md)


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
