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
# <a name="reading-drm-protected-asf-files-in-directshow"></a><span data-ttu-id="69a08-103">Lesen von DRM-Protected von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="69a08-103">Reading DRM-Protected ASF Files in DirectShow</span></span>

<span data-ttu-id="69a08-104">In diesem Thema wird die Verwendung von DirectShow zum Wiedergeben von Mediendateien beschrieben, die mit Windows Media Digital Rights Management (DRM) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="69a08-104">This topic describes how to use DirectShow to play media files that are protected with Windows Media Digital Rights Management (DRM).</span></span>

## <a name="drm-concepts"></a><span data-ttu-id="69a08-105">DRM-Konzepte</span><span class="sxs-lookup"><span data-stu-id="69a08-105">DRM Concepts</span></span>

<span data-ttu-id="69a08-106">Der Schutz einer Mediendatei mit Windows Media DRM umfasst zwei unterschiedliche Schritte:</span><span class="sxs-lookup"><span data-stu-id="69a08-106">Protecting a media file with Windows Media DRM involves two distinct steps:</span></span>

-   <span data-ttu-id="69a08-107">Der Inhaltsanbieter verpackt die Datei – das heißt, die Datei wird verschlüsselt, und es werden Lizenzierungsinformationen an den ASF-Dateiheader angefügt.</span><span class="sxs-lookup"><span data-stu-id="69a08-107">The content provider packages the file—that is, encrypts the file and attaches licensing information to the ASF file header.</span></span> <span data-ttu-id="69a08-108">Die Lizenzierungsinformationen beinhalten eine URL, über die der Client die Lizenz abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="69a08-108">The licensing information includes a URL where the client can obtain the license.</span></span>
-   <span data-ttu-id="69a08-109">Die Client Anwendung erhält eine Lizenz für den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="69a08-109">The client application acquires a license for the content.</span></span>

<span data-ttu-id="69a08-110">Die Paket Erstellung erfolgt vor der Verteilung der Datei.</span><span class="sxs-lookup"><span data-stu-id="69a08-110">Packaging happens before the file is distributed.</span></span> <span data-ttu-id="69a08-111">Der Lizenzerwerb erfolgt, wenn der Benutzer versucht, die Datei wiederzugeben oder zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="69a08-111">License acquisition occurs when the user tries to play or copy the file.</span></span> <span data-ttu-id="69a08-112">Der Lizenzerwerb ist möglich *erweise entweder* unbeaufsichtigt oder *nicht* automatisch.</span><span class="sxs-lookup"><span data-stu-id="69a08-112">License acquisition may be either *silent* or *non-silent*.</span></span> <span data-ttu-id="69a08-113">Der automatische Erwerb erfordert keine Interaktion mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="69a08-113">Silent acquisition does not require any interaction with the user.</span></span> <span data-ttu-id="69a08-114">Nicht automatische Käufe erfordert, dass die Anwendung ein Browserfenster öffnet und eine Webseite für den Benutzer anzeigt.</span><span class="sxs-lookup"><span data-stu-id="69a08-114">Non-silent acquisition requires the application to open a browser window and display a web page to the user.</span></span> <span data-ttu-id="69a08-115">An diesem Punkt muss der Benutzer möglicherweise einige Informationen für den Inhaltsanbieter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69a08-115">At that point, the user might need to provide some kind of information to the content provider.</span></span> <span data-ttu-id="69a08-116">Für beide Arten von Lizenz Käufen ist es jedoch erforderlich, dass der Client eine HTTP-Anforderung an einen Lizenzserver sendet.</span><span class="sxs-lookup"><span data-stu-id="69a08-116">However, both types of license acquisition require the client to submit an HTTP request to a license server.</span></span>

### <a name="drm-versions"></a><span data-ttu-id="69a08-117">DRM-Versionen</span><span class="sxs-lookup"><span data-stu-id="69a08-117">DRM Versions</span></span>

<span data-ttu-id="69a08-118">Es sind mehrere Versionen von Windows Media DRM vorhanden.</span><span class="sxs-lookup"><span data-stu-id="69a08-118">Several versions of Windows Media DRM exist.</span></span> <span data-ttu-id="69a08-119">Aus Sicht einer Client Anwendung können Sie in zwei Kategorien unterteilt werden: DRM-Version 1 und DRM-Version 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="69a08-119">From the perspective of a client application, they can be grouped into two categories: DRM version 1, and DRM version 7 or later.</span></span> <span data-ttu-id="69a08-120">(Die zweite Kategorie umfasst DRM-Versionen 9 und 10 sowie Version 7.) Der Grund für die Kategorisierung von DRM-Versionen auf diese Weise ist, dass die Lizenzen der Version 1 etwas anders behandelt werden als Version 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="69a08-120">(The second category includes DRM versions 9 and 10, as well as version 7.) The reason for categorizing DRM versions this way is that version 1 licenses are handled somewhat differently than version 7 or later licenses.</span></span> <span data-ttu-id="69a08-121">In dieser Dokumentation bedeutet der Begriff *Version 7 der Lizenz* Version 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="69a08-121">In this documentation, the term *version 7 license* means version 7 or later.</span></span>

<span data-ttu-id="69a08-122">Es ist auch wichtig, die DRM-Verpackung von der DRM-Lizenz zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="69a08-122">It is also important to distinguish the DRM packaging from the DRM license.</span></span> <span data-ttu-id="69a08-123">Wenn die Datei mit Windows Media Rights Manager Version 7 oder höher verpackt ist, kann der DRM-Header zusätzlich zur Lizenz-URL der Version 7 eine Lizenz-URL der Version 1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="69a08-123">If the file is packaged using Windows Media Rights Manager version 7 or later, the DRM header can contain a version 1 license URL in addition to the version 7 license URL.</span></span> <span data-ttu-id="69a08-124">Mit der Lizenz-URL der Version 1 können ältere Spieler, die Version 7 nicht unterstützen, eine Lizenz für den Inhalt erhalten.</span><span class="sxs-lookup"><span data-stu-id="69a08-124">The version 1 license URL enables older players that do not support version 7 to obtain a license for the content.</span></span> <span data-ttu-id="69a08-125">Die Konversation ist jedoch nicht wahr, sodass eine Datei mit der Paketversion 1 keine Lizenz-URL der Version 7 aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="69a08-125">However, the converse is not true, so a file with version 1 packaging cannot have a version 7 license URL.</span></span>

### <a name="application-security-level"></a><span data-ttu-id="69a08-126">Anwendungs Sicherheitsstufe</span><span class="sxs-lookup"><span data-stu-id="69a08-126">Application Security Level</span></span>

<span data-ttu-id="69a08-127">Zum Abspielen von DRM-geschützten Dateien muss die Client Anwendung mit einer statischen Bibliothek verknüpft werden, die von Microsoft in binärer Form bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="69a08-127">To play DRM-protected files, the client application must be linked to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="69a08-128">Diese Bibliothek, die die Anwendung eindeutig identifiziert, wird manchmal als stubbibliothek bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="69a08-128">This library, which uniquely identifies the application, is sometimes called the stub library.</span></span> <span data-ttu-id="69a08-129">Der Stub-Bibliothek ist eine Sicherheitsstufe zugewiesen, deren Wert durch den Lizenzvertrag bestimmt wird, den Sie beim Erwerb der stubbibliothek signiert haben.</span><span class="sxs-lookup"><span data-stu-id="69a08-129">The stub library has an assigned security level, the value of which is determined by the license agreement that you signed when you obtained the stub library.</span></span>

<span data-ttu-id="69a08-130">Der Inhaltsanbieter legt eine minimal erforderliche Sicherheitsstufe fest, um die Lizenz zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="69a08-130">The content provider sets a minimum security level needed to acquire the license.</span></span> <span data-ttu-id="69a08-131">Wenn die Sicherheitsstufe ihrer Stub-Bibliothek niedriger ist als die vom Lizenzserver benötigte mindestsicherheitsstufe, kann die Anwendung die Lizenz nicht abrufen.</span><span class="sxs-lookup"><span data-stu-id="69a08-131">If the security level of your stub library is less than the minimum security level required by the license server, the application cannot obtain the license.</span></span>

### <a name="individualization"></a><span data-ttu-id="69a08-132">Individualisierung</span><span class="sxs-lookup"><span data-stu-id="69a08-132">Individualization</span></span>

<span data-ttu-id="69a08-133">Um die Sicherheit zu erhöhen, kann eine Anwendung die DRM-Komponenten auf dem Client Computer aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="69a08-133">To increase security, an application may update the DRM components on the client's computer.</span></span> <span data-ttu-id="69a08-134">Dieses Update, das als "Individual alization" bezeichnet wird, unterscheidet die Kopie der Anwendung des Benutzers von allen anderen Kopien der gleichen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="69a08-134">This update, called individualization, differentiates the user's copy of the application from all other copies of the same application.</span></span> <span data-ttu-id="69a08-135">Der DRM-Header einer geschützten Datei kann angeben, dass eine minimale Individualisierungs Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="69a08-135">The DRM header of a protected file may specify may specify a minimum individualization level.</span></span> <span data-ttu-id="69a08-136">(Weitere Informationen finden Sie in der Dokumentation zu WMRMHeader. IndividualizedVersion im Windows Media Rights Manager SDK.)</span><span class="sxs-lookup"><span data-stu-id="69a08-136">(For more information, see the documentation for WMRMHeader.IndividualizedVersion in the Windows Media Rights Manager SDK.)</span></span>

<span data-ttu-id="69a08-137">Da der Microsoft Individual alization Service Informationen vom Benutzer verarbeitet, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der Microsoft-Website angeben, bevor Ihre Anwendung die folgenden Schritte durchführt: <https://go.microsoft.com/fwlink/p/?linkid=10240> .</span><span class="sxs-lookup"><span data-stu-id="69a08-137">Because the Microsoft Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft website before your application individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240>.</span></span>

## <a name="provide-the-software-certificate"></a><span data-ttu-id="69a08-138">Angeben des Software Zertifikats</span><span class="sxs-lookup"><span data-stu-id="69a08-138">Provide the Software Certificate</span></span>

<span data-ttu-id="69a08-139">Um der Anwendung die Verwendung der DRM-Lizenz zu ermöglichen, muss die Anwendung ein Software Zertifikat oder einen *Schlüssel* für den Filter Graph-Manager bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69a08-139">To enable the application to use the DRM license, the application must provide a software certificate or *key* to the Filter Graph Manager.</span></span> <span data-ttu-id="69a08-140">Dieser Schlüssel ist in einer statischen Bibliothek enthalten, die für die Anwendung individuell ist.</span><span class="sxs-lookup"><span data-stu-id="69a08-140">This key is contained in a static library that is individualized for the application.</span></span> <span data-ttu-id="69a08-141">Weitere Informationen zum Abrufen der individuellen Bibliothek finden Sie unter Abrufen [der erforderlichen DRM-Bibliothek](../wmformat/obtaining-the-required-drm-library.md) in der Dokumentation zum Windows Media-Format SDK.</span><span class="sxs-lookup"><span data-stu-id="69a08-141">For information about obtaining the individualized library, see [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="69a08-142">Führen Sie die folgenden Schritte aus, um den Software Schlüssel anzugeben:</span><span class="sxs-lookup"><span data-stu-id="69a08-142">To provide the software key, perform the following steps:</span></span>

1.  <span data-ttu-id="69a08-143">Verknüpfung mit der statischen Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="69a08-143">Link to the static library.</span></span>
2.  <span data-ttu-id="69a08-144">Implementieren Sie die **IServiceProvider** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="69a08-144">Implement the **IServiceProvider** interface.</span></span>
3.  <span data-ttu-id="69a08-145">Fragen Sie den Filter Graph-Manager nach der [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="69a08-145">Query the Filter Graph Manager for the [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) interface.</span></span>
4.  <span data-ttu-id="69a08-146">Aufrufen von [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) mit einem Zeiger auf die Implementierung von **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="69a08-146">Call [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) with a pointer to your implementation of **IServiceProvider**.</span></span>
5.  <span data-ttu-id="69a08-147">Der Filter Graph-Manager ruft **IServiceProvider:: QueryService** auf und gibt **IID \_ iwmreader** für den Dienst Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="69a08-147">The Filter Graph Manager will call **IServiceProvider::QueryService**, specifying **IID\_IWMReader** for the service identifier.</span></span>
6.  <span data-ttu-id="69a08-148">Rufen Sie in ihrer Implementierung von **QueryService** [**wmkreatecertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) auf, um den Software Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69a08-148">In your implementation of **QueryService**, call [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) to create the software key.</span></span>

<span data-ttu-id="69a08-149">Der folgende Code zeigt, wie die **QueryService** -Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="69a08-149">The following code shows how to implement the **QueryService** method:</span></span>


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



<span data-ttu-id="69a08-150">Der folgende Code zeigt, wie Sie [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) im Filter Graph-Manager aufrufen:</span><span class="sxs-lookup"><span data-stu-id="69a08-150">The following code shows how to call [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) on the Filter Graph Manager:</span></span>


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





## <a name="building-the-playback-graph"></a><span data-ttu-id="69a08-151">Aufbauen des Wiedergabe Diagramms</span><span class="sxs-lookup"><span data-stu-id="69a08-151">Building the Playback Graph</span></span>

<span data-ttu-id="69a08-152">Führen Sie die folgenden Schritte aus, um eine DRM-geschützte DRM-Datei wiederzugeben:</span><span class="sxs-lookup"><span data-stu-id="69a08-152">To play a DRM-protected ASF file, perform the following steps:</span></span>

1.  <span data-ttu-id="69a08-153">Erstellen Sie den [Filter Graph-Manager](filter-graph-manager.md) , und verwenden Sie die [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle, um Graph-Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="69a08-153">Create the [Filter Graph Manager](filter-graph-manager.md) and use the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to register for graph events.</span></span>
2.  <span data-ttu-id="69a08-154">Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine neue Instanz des WM-- [ASF-Lesefilter](wm-asf-reader-filter.md) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69a08-154">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>
3.  <span data-ttu-id="69a08-155">Wenden Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) an, um den Filter dem Filter Diagramm hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="69a08-155">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph.</span></span>
4.  <span data-ttu-id="69a08-156">Fragen Sie den Filter nach der [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="69a08-156">Query the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface.</span></span>
5.  <span data-ttu-id="69a08-157">Nennen Sie [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) mit der URL der Datei.</span><span class="sxs-lookup"><span data-stu-id="69a08-157">Call [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) with the URL of the file.</span></span>
6.  <span data-ttu-id="69a08-158">Behandeln von Ereignissen des [**EC \_ WMT- \_ Ereignisses**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="69a08-158">Handle [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>
7.  <span data-ttu-id="69a08-159">Fragen Sie auf dem ersten [**\_ WMT- \_ Ereignis**](ec-wmt-event.md) Ereignis den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter nach der **IServiceProvider** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="69a08-159">On the first [**EC\_WMT\_EVENT**](ec-wmt-event.md) event, query the [WM ASF Reader](wm-asf-reader-filter.md) filter for the **IServiceProvider** interface.</span></span>
8.  <span data-ttu-id="69a08-160">Aufrufen von **IServiceProvider:: QueryService** , um einen Zeiger auf die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="69a08-160">Call **IServiceProvider::QueryService** to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
9.  <span data-ttu-id="69a08-161">Ruft [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) auf, um die Ausgabe Pins für den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter zu rendernen.</span><span class="sxs-lookup"><span data-stu-id="69a08-161">Call [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="69a08-162">Wenn Sie eine DRM-geschützte Datei öffnen, rufen Sie nicht [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) auf, um das Filter Diagramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="69a08-162">When opening a DRM-protected file, do not call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) to create the filter graph.</span></span> <span data-ttu-id="69a08-163">Der WM-ASF-Lesefilter kann erst dann eine Verbindung mit anderen Filtern herstellen, wenn die DRM-Lizenz abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="69a08-163">The WM ASF Reader filter cannot connect to any other filters until the DRM license is acquired.</span></span> <span data-ttu-id="69a08-164">Dieser Schritt erfordert, dass die Anwendung die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle verwendet, die vom Filter abgerufen werden muss, wie in den Schritten 7 – 8 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69a08-164">This step requires the application to use the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface, which must be obtained from the filter, as described in steps 7–8.</span></span> <span data-ttu-id="69a08-165">Daher müssen Sie den Filter erstellen und dem Diagramm hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69a08-165">Therefore, you must create the filter and add it to the graph</span></span>

 

> [!Note]  
> <span data-ttu-id="69a08-166">Es ist wichtig, sich für Graph-Ereignisse (Schritt 1) zu registrieren, bevor Sie dem Diagramm den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter hinzufügen (Schritt 3), da die Anwendung die Ereignisse des [**EC \_ WMT- \_ Ereignisses**](ec-wmt-event.md) verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="69a08-166">It is important to register for graph events (step 1) before adding the [WM ASF Reader](wm-asf-reader-filter.md) filter to the graph (step 3), because the application must handle the [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span> <span data-ttu-id="69a08-167">Die Ereignisse werden gesendet, wenn [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) aufgerufen wird (Schritt 5).</span><span class="sxs-lookup"><span data-stu-id="69a08-167">The events are sent when [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) is called (step 5).</span></span>

 

<span data-ttu-id="69a08-168">Der folgende Code zeigt, wie das Diagramm erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="69a08-168">The following code shows how to build the graph:</span></span>


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
<th><span data-ttu-id="69a08-169">C++</span><span class="sxs-lookup"><span data-stu-id="69a08-169">C++</span></span></th>
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



<span data-ttu-id="69a08-170">Im vorherigen Code `RenderOutputPins` Listet die Funktion die Ausgabe Pins für den WM-ASF- [Reader](wm-asf-reader-filter.md) -Filter auf und ruft [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) für jede PIN auf.</span><span class="sxs-lookup"><span data-stu-id="69a08-170">In the previous code, the `RenderOutputPins` function enumerates the output pins on the [WM ASF Reader](wm-asf-reader-filter.md) filter and calls [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) for each pin.</span></span>


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



<span data-ttu-id="69a08-171">Der folgende Code zeigt, wie Sie einen Zeiger auf die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle vom [WM-ASF-Reader](wm-asf-reader-filter.md)erhalten:</span><span class="sxs-lookup"><span data-stu-id="69a08-171">The following code shows how to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md):</span></span>


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





## <a name="related-topics"></a><span data-ttu-id="69a08-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69a08-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a08-173">Lesen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="69a08-173">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
