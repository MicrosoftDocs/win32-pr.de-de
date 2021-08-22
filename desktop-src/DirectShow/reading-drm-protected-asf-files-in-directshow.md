---
description: In diesem Thema wird beschrieben, wie Sie DirectShow zum Wiedergeben von Mediendateien verwenden, die mit Windows Media Digital Rights Management (DRM) geschützt sind.
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lesen DRM-Protected ASF-Dateien in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709a3f7e9398b075f826e29b5b60f362d94795ac551440c34f2f882a9ec0e2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072824"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lesen DRM-Protected ASF-Dateien in DirectShow

In diesem Thema wird beschrieben, wie Sie DirectShow zum Wiedergeben von Mediendateien verwenden, die mit Windows Media Digital Rights Management (DRM) geschützt sind.

## <a name="drm-concepts"></a>DRM-Konzepte

Der Schutz einer Mediendatei mit Windows Medien-DRM umfasst zwei unterschiedliche Schritte:

-   Der Inhaltsanbieter packt die Datei, d. h. verschlüsselt die Datei und fügt Lizenzierungsinformationen an den ASF-Dateiheader an. Die Lizenzierungsinformationen enthalten eine URL, unter der der Client die Lizenz abrufen kann.
-   Die Clientanwendung erwirbt eine Lizenz für den Inhalt.

Die Paketierung erfolgt, bevor die Datei verteilt wird. Der Lizenzerwerb erfolgt, wenn der Benutzer versucht, die Datei wiederzuspielen oder zu kopieren. Der Lizenzerwerb kann entweder *unbeaufsichtigt* oder *nicht unbeaufsichtigt* erfolgen. Für den automatischen Erwerb ist keine Interaktion mit dem Benutzer erforderlich. Nicht automatischer Erwerb erfordert, dass die Anwendung ein Browserfenster öffnet und dem Benutzer eine Webseite anzeigt. An diesem Punkt muss der Benutzer dem Inhaltsanbieter möglicherweise eine Art von Informationen bereitstellen. Beide Arten des Lizenzerwerbs erfordern jedoch, dass der Client eine HTTP-Anforderung an einen Lizenzserver sendet.

### <a name="drm-versions"></a>DRM-Versionen

Es gibt mehrere Versionen von Windows Medien-DRM. Aus Sicht einer Clientanwendung können sie in zwei Kategorien gruppiert werden: DRM Version 1 und DRM Version 7 oder höher. (Die zweite Kategorie umfasst die DRM-Versionen 9 und 10 sowie Version 7.) Der Grund für die Kategorisierung von DRM-Versionen auf diese Weise ist, dass Lizenzen der Version 1 etwas anders behandelt werden als Lizenzen der Version 7 oder höher. In dieser Dokumentation steht der Begriff *Lizenzversion 7* für Version 7 oder höher.

Es ist auch wichtig, die DRM-Paketierung von der DRM-Lizenz zu unterscheiden. Wenn die Datei mit Windows Media Rights Manager Version 7 oder höher gepackt wird, kann der DRM-Header zusätzlich zur Lizenz-URL der Version 7 eine Lizenz-URL der Version 1 enthalten. Die Lizenz-URL der Version 1 ermöglicht es älteren Playern, die Version 7 nicht unterstützen, eine Lizenz für den Inhalt zu erhalten. Das Umgekehrte trifft jedoch nicht zu, sodass eine Datei mit der Paketierung der Version 1 keine Lizenz-URL der Version 7 aufweisen kann.

### <a name="application-security-level"></a>Anwendungssicherheitsstufe

Um DRM-geschützte Dateien wiedergeben zu können, muss die Clientanwendung mit einer statischen Bibliothek verknüpft werden, die von Microsoft in binärer Form bereitgestellt wird. Diese Bibliothek, die die Anwendung eindeutig identifiziert, wird manchmal als Stubbibliothek bezeichnet. Die Stubbibliothek verfügt über eine zugewiesene Sicherheitsstufe, deren Wert durch den Lizenzvertrag bestimmt wird, den Sie beim Erhalt der Stubbibliothek unterzeichnet haben.

Der Inhaltsanbieter legt eine Mindestsicherheitsstufe fest, die für den Erwerb der Lizenz erforderlich ist. Wenn die Sicherheitsstufe Ihrer Stubbibliothek kleiner als die für den Lizenzserver erforderliche Mindestsicherheitsstufe ist, kann die Anwendung die Lizenz nicht abrufen.

### <a name="individualization"></a>Individualisierung

Um die Sicherheit zu erhöhen, kann eine Anwendung die DRM-Komponenten auf dem Clientcomputer aktualisieren. Dieses Als Individualisierung bezeichnete Update unterscheidet die Kopie der Anwendung des Benutzers von allen anderen Kopien derselben Anwendung. Der DRM-Header einer geschützten Datei kann eine mindeste Individualisierungsstufe angeben. (Weitere Informationen finden Sie in der Dokumentation zu WMRMHeader.IndividualizedVersion im Windows Media Rights Manager SDK.)

Da der Microsoft Individualization Service Informationen vom Benutzer verarbeitet, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der Microsoft-Website bereitstellen, bevor Ihre Anwendung individualisiert wird: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Bereitstellen des Softwarezertifikats

Damit die Anwendung die DRM-Lizenz verwenden kann, muss die Anwendung dem Filter Graph Manager ein Softwarezertifikat oder einen *Schlüssel* bereitstellen. Dieser Schlüssel ist in einer statischen Bibliothek enthalten, die für die Anwendung individualisiert ist. Informationen zum Abrufen der individualisierten Bibliothek finden Sie unter [Abrufen der erforderlichen DRM-Bibliothek](../wmformat/obtaining-the-required-drm-library.md) in der Dokumentation zum Windows Media Format SDK.

Führen Sie die folgenden Schritte aus, um den Softwareschlüssel bereitzustellen:

1.  Link zur statischen Bibliothek.
2.  Implementieren Sie die **IServiceProvider-Schnittstelle.**
3.  Fragen Sie den Filter Graph Manager für die [**IObjectWithSite-Schnittstelle**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) ab.
4.  Rufen Sie [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) mit einem Zeiger auf Ihre Implementierung von **IServiceProvider** auf.
5.  Der Filter-Graph-Manager ruft **IServiceProvider::QueryService** auf und gibt **IID \_ IWMReader** als Dienstbezeichner an.
6.  Rufen Sie in Ihrer Implementierung von **QueryService** [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) auf, um den Softwareschlüssel zu erstellen.

Der folgende Code zeigt, wie die **QueryService-Methode** implementiert wird:


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



Der folgende Code zeigt, wie [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) im Filter Graph Manager aufgerufen wird:


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





## <a name="building-the-playback-graph"></a>Erstellen der Wiedergabe-Graph

Führen Sie die folgenden Schritte aus, um eine DRM-geschützte ASF-Datei wiederzuspielen:

1.  Erstellen Sie den [Filter Graph Manager,](filter-graph-manager.md) und verwenden Sie die [**IMediaEventEx-Schnittstelle,**](/windows/desktop/api/Control/nn-control-imediaeventex) um sich für Graphereignisse zu registrieren.
2.  Rufen Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine neue Instanz des [WM ASF-Leserfilters](wm-asf-reader-filter.md) zu erstellen.
3.  Rufen Sie [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) auf, um den Filter dem Filterdiagramm hinzuzufügen.
4.  Fragen Sie den Filter nach der [**IFileSourceFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) ab.
5.  Rufen Sie [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) mit der URL der Datei auf.
6.  Behandeln von [**EC \_ WMT \_ EVENT-Ereignissen.**](ec-wmt-event.md)
7.  Fragen Sie beim ersten [**EC \_ WMT \_ EVENT-Ereignis**](ec-wmt-event.md) den [WM ASF-Readerfilter](wm-asf-reader-filter.md) nach der **IServiceProvider-Schnittstelle** ab.
8.  Rufen Sie **IServiceProvider::QueryService** auf, um einen Zeiger auf die [**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) abzurufen.
9.  Rufen Sie [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) auf, um die Ausgabepins des [WM ASF-Readerfilters](wm-asf-reader-filter.md) zu rendern.

> [!Note]  
> Rufen Sie beim Öffnen einer DRM-geschützten Datei nicht [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) auf, um das Filterdiagramm zu erstellen. Der WM ASF-Readerfilter kann erst dann eine Verbindung mit anderen Filtern herstellen, wenn die DRM-Lizenz erworben wurde. Für diesen Schritt muss die Anwendung die [**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) verwenden, die aus dem Filter abgerufen werden muss, wie in den Schritten 7 bis 8 beschrieben. Daher müssen Sie den Filter erstellen und dem Diagramm hinzufügen.

 

> [!Note]  
> Es ist wichtig, sich für Graphereignisse (Schritt 1) zu registrieren, bevor Sie dem Diagramm den [WM ASF-Readerfilter](wm-asf-reader-filter.md) hinzufügen (Schritt 3), da die Anwendung die [**EC \_ WMT \_ EVENT-Ereignisse**](ec-wmt-event.md) verarbeiten muss. Die Ereignisse werden gesendet, wenn [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) aufgerufen wird (Schritt 5).

 

Der folgende Code zeigt, wie das Diagramm erstellt wird:


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

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



Im vorherigen Code listet die `RenderOutputPins` Funktion die Ausgabepins für den [WM ASF-Readerfilter](wm-asf-reader-filter.md) auf und ruft [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) für jeden Pin auf.


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



Der folgende Code zeigt, wie Sie einen Zeiger auf die [**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) aus dem [WM ASF-Reader](wm-asf-reader-filter.md)abrufen:


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

 

 
