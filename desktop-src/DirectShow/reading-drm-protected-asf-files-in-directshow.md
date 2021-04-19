---
description: In diesem Thema wird die Verwendung von DirectShow zum Wiedergeben von Mediendateien beschrieben, die mit Windows Media Digital Rights Management (DRM) geschützt sind.
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lesen von DRM-Protected von ASF-Dateien in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355109"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lesen von DRM-Protected von ASF-Dateien in DirectShow

In diesem Thema wird die Verwendung von DirectShow zum Wiedergeben von Mediendateien beschrieben, die mit Windows Media Digital Rights Management (DRM) geschützt sind.

## <a name="drm-concepts"></a>DRM-Konzepte

Der Schutz einer Mediendatei mit Windows Media DRM umfasst zwei unterschiedliche Schritte:

-   Der Inhaltsanbieter verpackt die Datei – das heißt, die Datei wird verschlüsselt, und es werden Lizenzierungsinformationen an den ASF-Dateiheader angefügt. Die Lizenzierungsinformationen beinhalten eine URL, über die der Client die Lizenz abrufen kann.
-   Die Client Anwendung erhält eine Lizenz für den Inhalt.

Die Paket Erstellung erfolgt vor der Verteilung der Datei. Der Lizenzerwerb erfolgt, wenn der Benutzer versucht, die Datei wiederzugeben oder zu kopieren. Der Lizenzerwerb ist möglich *erweise entweder* unbeaufsichtigt oder *nicht* automatisch. Der automatische Erwerb erfordert keine Interaktion mit dem Benutzer. Nicht automatische Käufe erfordert, dass die Anwendung ein Browserfenster öffnet und eine Webseite für den Benutzer anzeigt. An diesem Punkt muss der Benutzer möglicherweise einige Informationen für den Inhaltsanbieter bereitstellen. Für beide Arten von Lizenz Käufen ist es jedoch erforderlich, dass der Client eine HTTP-Anforderung an einen Lizenzserver sendet.

### <a name="drm-versions"></a>DRM-Versionen

Es sind mehrere Versionen von Windows Media DRM vorhanden. Aus Sicht einer Client Anwendung können Sie in zwei Kategorien unterteilt werden: DRM-Version 1 und DRM-Version 7 oder höher. (Die zweite Kategorie umfasst DRM-Versionen 9 und 10 sowie Version 7.) Der Grund für die Kategorisierung von DRM-Versionen auf diese Weise ist, dass die Lizenzen der Version 1 etwas anders behandelt werden als Version 7 oder höher. In dieser Dokumentation bedeutet der Begriff *Version 7 der Lizenz* Version 7 oder höher.

Es ist auch wichtig, die DRM-Verpackung von der DRM-Lizenz zu unterscheiden. Wenn die Datei mit Windows Media Rights Manager Version 7 oder höher verpackt ist, kann der DRM-Header zusätzlich zur Lizenz-URL der Version 7 eine Lizenz-URL der Version 1 enthalten. Mit der Lizenz-URL der Version 1 können ältere Spieler, die Version 7 nicht unterstützen, eine Lizenz für den Inhalt erhalten. Die Konversation ist jedoch nicht wahr, sodass eine Datei mit der Paketversion 1 keine Lizenz-URL der Version 7 aufweisen kann.

### <a name="application-security-level"></a>Anwendungs Sicherheitsstufe

Zum Abspielen von DRM-geschützten Dateien muss die Client Anwendung mit einer statischen Bibliothek verknüpft werden, die von Microsoft in binärer Form bereitgestellt wird. Diese Bibliothek, die die Anwendung eindeutig identifiziert, wird manchmal als stubbibliothek bezeichnet. Der Stub-Bibliothek ist eine Sicherheitsstufe zugewiesen, deren Wert durch den Lizenzvertrag bestimmt wird, den Sie beim Erwerb der stubbibliothek signiert haben.

Der Inhaltsanbieter legt eine minimal erforderliche Sicherheitsstufe fest, um die Lizenz zu erwerben. Wenn die Sicherheitsstufe ihrer Stub-Bibliothek niedriger ist als die vom Lizenzserver benötigte mindestsicherheitsstufe, kann die Anwendung die Lizenz nicht abrufen.

### <a name="individualization"></a>Individualisierung

Um die Sicherheit zu erhöhen, kann eine Anwendung die DRM-Komponenten auf dem Client Computer aktualisieren. Dieses Update, das als "Individual alization" bezeichnet wird, unterscheidet die Kopie der Anwendung des Benutzers von allen anderen Kopien der gleichen Anwendung. Der DRM-Header einer geschützten Datei kann angeben, dass eine minimale Individualisierungs Ebene angibt. (Weitere Informationen finden Sie in der Dokumentation zu WMRMHeader. IndividualizedVersion im Windows Media Rights Manager SDK.)

Da der Microsoft Individual alization Service Informationen vom Benutzer verarbeitet, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der Microsoft-Website angeben, bevor Ihre Anwendung die folgenden Schritte durchführt: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Angeben des Software Zertifikats

Um der Anwendung die Verwendung der DRM-Lizenz zu ermöglichen, muss die Anwendung ein Software Zertifikat oder einen *Schlüssel* für den Filter Graph-Manager bereitstellen. Dieser Schlüssel ist in einer statischen Bibliothek enthalten, die für die Anwendung individuell ist. Weitere Informationen zum Abrufen der individuellen Bibliothek finden Sie unter Abrufen [der erforderlichen DRM-Bibliothek](../wmformat/obtaining-the-required-drm-library.md) in der Dokumentation zum Windows Media-Format SDK.

Führen Sie die folgenden Schritte aus, um den Software Schlüssel anzugeben:

1.  Verknüpfung mit der statischen Bibliothek.
2.  Implementieren Sie die **IServiceProvider** -Schnittstelle.
3.  Fragen Sie den Filter Graph-Manager nach der [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) -Schnittstelle ab.
4.  Aufrufen von [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) mit einem Zeiger auf die Implementierung von **IServiceProvider**.
5.  Der Filter Graph-Manager ruft **IServiceProvider:: QueryService** auf und gibt **IID \_ iwmreader** für den Dienst Bezeichner an.
6.  Rufen Sie in ihrer Implementierung von **QueryService** [**wmkreatecertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) auf, um den Software Schlüssel zu erstellen.

Der folgende Code zeigt, wie die **QueryService** -Methode implementiert wird:


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



Der folgende Code zeigt, wie Sie [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) im Filter Graph-Manager aufrufen:


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





## <a name="building-the-playback-graph"></a>Aufbauen des Wiedergabe Diagramms

Führen Sie die folgenden Schritte aus, um eine DRM-geschützte DRM-Datei wiederzugeben:

1.  Erstellen Sie den [Filter Graph-Manager](filter-graph-manager.md) , und verwenden Sie die [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle, um Graph-Ereignisse zu registrieren.
2.  Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine neue Instanz des WM-- [ASF-Lesefilter](wm-asf-reader-filter.md) zu erstellen.
3.  Wenden Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) an, um den Filter dem Filter Diagramm hinzuzufügen.
4.  Fragen Sie den Filter nach der [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) -Schnittstelle ab.
5.  Nennen Sie [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) mit der URL der Datei.
6.  Behandeln von Ereignissen des [**EC \_ WMT- \_ Ereignisses**](ec-wmt-event.md) .
7.  Fragen Sie auf dem ersten [**\_ WMT- \_ Ereignis**](ec-wmt-event.md) Ereignis den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter nach der **IServiceProvider** -Schnittstelle ab.
8.  Aufrufen von **IServiceProvider:: QueryService** , um einen Zeiger auf die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle zu erhalten.
9.  Ruft [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) auf, um die Ausgabe Pins für den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter zu rendernen.

> [!Note]  
> Wenn Sie eine DRM-geschützte Datei öffnen, rufen Sie nicht [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) auf, um das Filter Diagramm zu erstellen. Der WM-ASF-Lesefilter kann erst dann eine Verbindung mit anderen Filtern herstellen, wenn die DRM-Lizenz abgerufen wurde. Dieser Schritt erfordert, dass die Anwendung die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle verwendet, die vom Filter abgerufen werden muss, wie in den Schritten 7 – 8 beschrieben. Daher müssen Sie den Filter erstellen und dem Diagramm hinzufügen.

 

> [!Note]  
> Es ist wichtig, sich für Graph-Ereignisse (Schritt 1) zu registrieren, bevor Sie dem Diagramm den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter hinzufügen (Schritt 3), da die Anwendung die Ereignisse des [**EC \_ WMT- \_ Ereignisses**](ec-wmt-event.md) verarbeiten muss. Die Ereignisse werden gesendet, wenn [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) aufgerufen wird (Schritt 5).

 

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



Im vorherigen Code `RenderOutputPins` Listet die Funktion die Ausgabe Pins für den WM-ASF- [Reader](wm-asf-reader-filter.md) -Filter auf und ruft [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) für jede PIN auf.


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



Der folgende Code zeigt, wie Sie einen Zeiger auf die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle vom [WM-ASF-Reader](wm-asf-reader-filter.md)erhalten:


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

 

 
