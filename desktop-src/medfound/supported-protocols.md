---
description: Unterstützte Protokolle
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Unterstützte Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753840"
---
# <a name="supported-protocols"></a><span data-ttu-id="1a631-103">Unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="1a631-103">Supported Protocols</span></span>

<span data-ttu-id="1a631-104">Media Foundation unterstützt die folgenden Protokolle:</span><span class="sxs-lookup"><span data-stu-id="1a631-104">Media Foundation supports the following protocols:</span></span>

-   <span data-ttu-id="1a631-105">Real-Time Streaming Protocol (RTSP)</span><span class="sxs-lookup"><span data-stu-id="1a631-105">Real Time Streaming Protocol (RTSP)</span></span>

    <span data-ttu-id="1a631-106">RTSP wird hauptsächlich zum Streamen von Medieninhalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a631-106">RTSP is mainly used for streaming media content.</span></span> <span data-ttu-id="1a631-107">Sie kann UDP oder TCP als Transportprotokolle verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a631-107">It can use UDP or TCP as transport protocols.</span></span> <span data-ttu-id="1a631-108">UDP ist die effizienteste für die Inhalts Übermittlung, da der Bandbreiten Aufwand kleiner ist als bei TCP-basierten Protokollen.</span><span class="sxs-lookup"><span data-stu-id="1a631-108">UDP is the most efficient for content delivery because the bandwidth overhead is less than with TCP-based protocols.</span></span> <span data-ttu-id="1a631-109">Obwohl das TCP-Protokoll eine zuverlässige Paket Bereitstellung gewährleistet, eignet sich TCP nicht gut für digitale Medienströme, bei denen die effiziente Nutzung der Bandbreite wichtiger als gelegentliche verlorene Pakete ist.</span><span class="sxs-lookup"><span data-stu-id="1a631-109">Even though the TCP protocol ensures reliable packet delivery, TCP is not well suited for digital media streams, where efficient use of bandwidth is more important than occasional lost packets.</span></span>

-   <span data-ttu-id="1a631-110">Hypertext Transfer-Protokoll (HTTP)</span><span class="sxs-lookup"><span data-stu-id="1a631-110">Hypertext Transfer Protocol (HTTP)</span></span>

    <span data-ttu-id="1a631-111">HTTP verwendet TCP und wird von Webservern verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a631-111">HTTP uses TCP and is used by web servers.</span></span> <span data-ttu-id="1a631-112">Das Schema "httpd://" gibt an, dass die Quelle von einem Webserver heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a631-112">The "httpd://" scheme indicates that the source is downloadable from a web server.</span></span> <span data-ttu-id="1a631-113">Http wird auch bei Firewalls verwendet, die in der Regel so konfiguriert werden, dass HTTP-Anforderungen akzeptiert werden, und die in der Regel andere Streamingprotokolle ablehnen.</span><span class="sxs-lookup"><span data-stu-id="1a631-113">HTTP is also used in case of firewalls, which are usually configured to accept HTTP requests and typically reject other streaming protocols.</span></span>

<span data-ttu-id="1a631-114">Die Anwendung kann die Protokolle, die von Media Foundation unterstützt werden, mithilfe der [**imvnetschemehandlerconfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) -Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a631-114">The application can get the protocols supported by Media Foundation by using the [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) interface.</span></span> <span data-ttu-id="1a631-115">Hierzu muss die Anwendung zunächst die Anzahl der Protokolle abrufen, indem Sie [**imfnetschemehandlerconfig:: getnumofsupportedprotokolls**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) aufrufen und dann den Protokolltyp basierend auf dem Index abrufen, indem Sie [**imfnetschemehandlerconfig:: getsupportedprotocoltype**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1a631-115">To do this, the application must first retrieve the number of protocols, by calling [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) and then get the protocol type based on the index by calling [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span></span> <span data-ttu-id="1a631-116">Diese Methode gibt einen der Werte zurück, die in der Enumeration des [**msnetsource- \_ Protokoll \_ Typs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1a631-116">This method returns one of the values defined in the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>

<span data-ttu-id="1a631-117">Die Anwendung kann auch die vom quellresolver unterstützten Schemas abrufen, indem Sie die Funktion [**mfgetsupportedschemas**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) aufruft.</span><span class="sxs-lookup"><span data-stu-id="1a631-117">The application can also get the schemes supported by the source resolver by calling the [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) function.</span></span>

## <a name="protocol-rollover"></a><span data-ttu-id="1a631-118">Protokollrollover</span><span class="sxs-lookup"><span data-stu-id="1a631-118">Protocol Rollover</span></span>

<span data-ttu-id="1a631-119">Wenn eine Anwendung "MMS://" als URL-Schema angibt, führt der Quell Konflikt Löser einen *protokollrollovervorgang* aus.</span><span class="sxs-lookup"><span data-stu-id="1a631-119">When an application specifies "mms://" as the URL scheme, the source resolver performs a *protocol rollover* operation.</span></span> <span data-ttu-id="1a631-120">In diesem Prozess bestimmt der quellresolver das beste Protokoll, das die Netzwerkquelle zum erhalten des Inhalts verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a631-120">In this process, the source resolver determines the best protocol for the network source to use for getting the content.</span></span> <span data-ttu-id="1a631-121">In der Regel ist RTSP mit UDP (RTSPU) für das Streaming von Medien effizienter als http.</span><span class="sxs-lookup"><span data-stu-id="1a631-121">Typically, for media steaming, RTSP with UDP (RTSPU) is more efficient than HTTP.</span></span> <span data-ttu-id="1a631-122">Wenn der Inhalt jedoch auf einem Webserver gehostet wird, ist http eine bessere Wahl.</span><span class="sxs-lookup"><span data-stu-id="1a631-122">However, if the content is hosted on a web server, HTTP is a better choice.</span></span>

<span data-ttu-id="1a631-123">Ein Protokollrollover kann auch auftreten, wenn der Versuch, das im URL-Schema angegebene Protokoll zu verwenden, fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1a631-123">Protocol rollover can also occur when an attempt to use the protocol specified in the URL scheme fails.</span></span> <span data-ttu-id="1a631-124">Beispielsweise kann ein Protokoll fehlschlagen, wenn UDP-Pakete von einer Firewall blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="1a631-124">For example, a protocol can fail when a firewall blocks UDP packets.</span></span> <span data-ttu-id="1a631-125">In diesem Fall wechselt der quellresolver zu http.</span><span class="sxs-lookup"><span data-stu-id="1a631-125">In this case, the source resolver switches to HTTP.</span></span>

<span data-ttu-id="1a631-126">Der Protokollrollover trifft nicht zu, wenn das URL-Schema ein bestimmtes Protokoll enthält, z. b. "rtspu://".</span><span class="sxs-lookup"><span data-stu-id="1a631-126">Protocol rollover does not apply if the URL scheme contains a specific protocol, such as "rtspu://".</span></span> <span data-ttu-id="1a631-127">Außerdem wird der Rollover nicht ausgeführt, wenn die Authentifizierung fehlschlägt oder der Server ein Limit von Clientverbindungen erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="1a631-127">Also, rollover is not performed if authentication fails or the server has reached a limit of client connections.</span></span> <span data-ttu-id="1a631-128">Es wird empfohlen, dass Anwendungen das Schema "MMS://" angeben und zulassen, dass der quellresolver das beste Protokoll für das Szenario auswählt.</span><span class="sxs-lookup"><span data-stu-id="1a631-128">It is recommended that applications specify the "mms://" scheme and allow the source resolver to select the best protocol for the scenario.</span></span>

<span data-ttu-id="1a631-129">In der folgenden Tabelle ist die rolloverreihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1a631-129">The following table lists the rollover order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a631-130">Zulässige Schemas</span><span class="sxs-lookup"><span data-stu-id="1a631-130">Schemes allowed</span></span></th>
<th><span data-ttu-id="1a631-131">Protokollrollover-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1a631-131">Protocol rollover order</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a631-132">MMS://oder RTSP://</span><span class="sxs-lookup"><span data-stu-id="1a631-132">mms:// or rtsp://</span></span></td>
<td><span data-ttu-id="1a631-133">Schneller Cache aktiviert:</span><span class="sxs-lookup"><span data-stu-id="1a631-133">Fast Cache enabled:</span></span><br/>
<ol>
<li><span data-ttu-id="1a631-134">RTSP mit TCP (RTSPT)</span><span class="sxs-lookup"><span data-stu-id="1a631-134">RTSP with TCP (RTSPT)</span></span><br/></li>
<li><span data-ttu-id="1a631-135">RTSP mit UDP (RTSPU)</span><span class="sxs-lookup"><span data-stu-id="1a631-135">RTSP with UDP (RTSPU)</span></span><br/></li>
<li><span data-ttu-id="1a631-136">HTTP-Streaming</span><span class="sxs-lookup"><span data-stu-id="1a631-136">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="1a631-137">HTTP-Download (httpd)</span><span class="sxs-lookup"><span data-stu-id="1a631-137">HTTP download (HTTPD)</span></span><br/></li>
</ol>
<span data-ttu-id="1a631-138">Schneller Cache deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="1a631-138">Fast Cache disabled:</span></span><br/>
<ol>
<li><span data-ttu-id="1a631-139">RTSPU</span><span class="sxs-lookup"><span data-stu-id="1a631-139">RTSPU</span></span><br/></li>
<li><span data-ttu-id="1a631-140">RTSPT</span><span class="sxs-lookup"><span data-stu-id="1a631-140">RTSPT</span></span><br/></li>
<li><span data-ttu-id="1a631-141">HTTP-Streaming</span><span class="sxs-lookup"><span data-stu-id="1a631-141">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="1a631-142">HTTP-Download</span><span class="sxs-lookup"><span data-stu-id="1a631-142">HTTP Download</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a631-143">rtspu://</span><span class="sxs-lookup"><span data-stu-id="1a631-143">rtspu://</span></span></td>
<td><span data-ttu-id="1a631-144">RTSPU</span><span class="sxs-lookup"><span data-stu-id="1a631-144">RTSPU</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a631-145">rtspt://</span><span class="sxs-lookup"><span data-stu-id="1a631-145">rtspt://</span></span></td>
<td><span data-ttu-id="1a631-146">RTSPT</span><span class="sxs-lookup"><span data-stu-id="1a631-146">RTSPT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a631-147"> https://</span><span class="sxs-lookup"><span data-stu-id="1a631-147">https://</span></span></td>
<td><ol>
<li><span data-ttu-id="1a631-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="1a631-148">HTTP</span></span><br/></li>
<li><span data-ttu-id="1a631-149">HTTPD</span><span class="sxs-lookup"><span data-stu-id="1a631-149">HTTPD</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a631-150">httpd://</span><span class="sxs-lookup"><span data-stu-id="1a631-150">httpd://</span></span></td>
<td><span data-ttu-id="1a631-151">HTTPD</span><span class="sxs-lookup"><span data-stu-id="1a631-151">HTTPD</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a><span data-ttu-id="1a631-152">Das aktuelle Protokoll wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1a631-152">Retrieving the Current Protocol</span></span>

<span data-ttu-id="1a631-153">Nach einem protokollrollovervorgang verwendet die Netzwerkquelle möglicherweise ein anderes Protokoll als das, das von der Anwendung im URL-Schema angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1a631-153">After a protocol rollover operation, the network source might use a protocol other than the one specified by the application in the URL scheme.</span></span> <span data-ttu-id="1a631-154">Das Ergebnis des Protokollrollovers steht der Anwendung zur Verfügung, nachdem die Netzwerkquelle die Verbindung mit dem Medienserver hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="1a631-154">The protocol rollover result is available to the application after the network source establishes the connection with the media server.</span></span>

<span data-ttu-id="1a631-155">Zum Abrufen des Protokolls und des Transports, die zum Abrufen des Inhalts verwendet werden, kann die Anwendung die Eigenschaftswerte für die [mfnetsource- \_ Protokoll](mfnetsource-protocol-property.md) Eigenschaft und die [mfnetsource- \_ Transport](mfnetsource-transport-property.md) Eigenschaft eines **IPropertyStore** -Objekts aus der Netzwerkquelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="1a631-155">To get the protocol and transport that are used for getting the content, the application can retrieve the property values for the [MFNETSOURCE\_PROTOCOL](mfnetsource-protocol-property.md) property and the [MFNETSOURCE\_TRANSPORT](mfnetsource-transport-property.md) property of an **IPropertyStore** object from the network source.</span></span>

<span data-ttu-id="1a631-156">Der folgende Code zeigt, wie Sie diese Werte erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a631-156">The following code shows how to get these values.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



<span data-ttu-id="1a631-157">Im vorherigen Beispielcode ruft **IPropertyStore:: GetValue** den mfnetsource- \_ Protokoll Wert ab, der ein Member der [**mfnetsource- \_ \_ Protokolltyp**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) -Enumeration ist.</span><span class="sxs-lookup"><span data-stu-id="1a631-157">In the preceding example code, **IPropertyStore::GetValue** retrieves the MFNETSOURCE\_PROTOCOL value, which is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span> <span data-ttu-id="1a631-158">Für den mfnetsource- \_ Transport ist der Wert ein Member der [**mfnetsource \_ - \_ Transporttyp**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="1a631-158">For MFNETSOURCE\_TRANSPORT, the value is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>

<span data-ttu-id="1a631-159">Alternativ kann die Anwendung dieselben Werte mithilfe des MF-Quell \_ Statistik \_ Dienst-Dienstanbieter erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a631-159">Alternately, the application can get the same values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span> <span data-ttu-id="1a631-160">Um diesen Dienst zu verwenden, kann die Anwendung die [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) -Funktion aufrufen, um den Eigenschaften Speicher aus der Netzwerkquelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1a631-160">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store from the network source.</span></span> <span data-ttu-id="1a631-161">Dieser Eigenschaften Speicher enthält Netzwerk Statistiken in der Eigenschaft " [MF-Quell \_ Statistik](mfnetsource-statistics-property.md) ".</span><span class="sxs-lookup"><span data-stu-id="1a631-161">This property store contains network statistics in the [MFNETSOURCE\_STATISTICS](mfnetsource-statistics-property.md) property.</span></span> <span data-ttu-id="1a631-162">Protokoll-und Transport Werte können abgerufen werden, indem die mfnetsource \_ -Protokoll- \_ ID und mfnetsource-Transport-ID – angegeben werden, \_ \_ die in der Enumeration der [**mfnetsource- \_ Statistik- \_ IDs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)</span><span class="sxs-lookup"><span data-stu-id="1a631-162">Protocol and transport values can be retrieved by specifying MFNETSOURCE\_PROTOCOL\_ID and MFNETSOURCE\_TRANSPORT\_ID—defined in the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration.</span></span> <span data-ttu-id="1a631-163">Der folgende Code zeigt, wie Sie die Protokoll-und Transport Werte mithilfe des mfnetsource- \_ Statistik \_ Dienst Dienstanbieter erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a631-163">The following code shows how to get the protocol and transport values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a><span data-ttu-id="1a631-164">Aktivieren und Deaktivieren von Protokollen</span><span class="sxs-lookup"><span data-stu-id="1a631-164">Enabling and Disabling Protocols</span></span>

<span data-ttu-id="1a631-165">Die Anwendung kann die Netzwerkquelle so konfigurieren, dass bestimmte Protokolle während des rolloverprozesses übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="1a631-165">The application can configure the network source so that certain protocols are skipped during the rollover process.</span></span> <span data-ttu-id="1a631-166">Zu diesem Zweck werden die Eigenschaften von Netzwerk Quellen verwendet, um bestimmte Protokolle zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1a631-166">To do this, network source properties are used to disable specific protocols.</span></span> <span data-ttu-id="1a631-167">In der folgenden Tabelle werden die Eigenschaften und die von Ihnen kontrollierten Protokolle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a631-167">The following table shows the properties and the protocols they control.</span></span>



| <span data-ttu-id="1a631-168">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1a631-168">Property</span></span>                                                                    | <span data-ttu-id="1a631-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a631-169">Description</span></span>                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="1a631-170">MF NetSource \_ \_ http aktivieren</span><span class="sxs-lookup"><span data-stu-id="1a631-170">MFNETSOURCE\_ENABLE\_HTTP</span></span>](mfnetsource-enable-http-property.md)           | <span data-ttu-id="1a631-171">Aktiviert oder deaktiviert http und httpd.</span><span class="sxs-lookup"><span data-stu-id="1a631-171">Enables or disables HTTP and HTTPD.</span></span>         |
| [<span data-ttu-id="1a631-172">MF NetSource \_ , \_ RTSP aktivieren</span><span class="sxs-lookup"><span data-stu-id="1a631-172">MFNETSOURCE\_ENABLE\_RTSP</span></span>](mfnetsource-enable-rtsp-property.md)           | <span data-ttu-id="1a631-173">Aktiviert oder deaktiviert RTSPU und RTSPT.</span><span class="sxs-lookup"><span data-stu-id="1a631-173">Enables or disables RTSPU and RTSPT.</span></span>        |
| [<span data-ttu-id="1a631-174">MF NetSource \_ \_ TCP aktivieren</span><span class="sxs-lookup"><span data-stu-id="1a631-174">MFNETSOURCE\_ENABLE\_TCP</span></span>](mfnetsource-enable-tcp-property.md)             | <span data-ttu-id="1a631-175">Aktiviert oder deaktiviert RTSPT.</span><span class="sxs-lookup"><span data-stu-id="1a631-175">Enables or disables RTSPT.</span></span>                  |
| [<span data-ttu-id="1a631-176">MF NetSource \_ Aktivieren von \_ UDP</span><span class="sxs-lookup"><span data-stu-id="1a631-176">MFNETSOURCE\_ENABLE\_UDP</span></span>](mfnetsource-enable-udp-property.md)             | <span data-ttu-id="1a631-177">Aktiviert oder deaktiviert RTSPU.</span><span class="sxs-lookup"><span data-stu-id="1a631-177">Enables or disables RTSPU.</span></span>                  |
| [<span data-ttu-id="1a631-178">MF-Quell \_ \_ Download aktivieren</span><span class="sxs-lookup"><span data-stu-id="1a631-178">MFNETSOURCE\_ENABLE\_DOWNLOAD</span></span>](mfnetsource-enable-download-property.md)   | <span data-ttu-id="1a631-179">Aktiviert oder deaktiviert httpd.</span><span class="sxs-lookup"><span data-stu-id="1a631-179">Enables or disables HTTPD.</span></span>                  |
| [<span data-ttu-id="1a631-180">MF-Quelle \_ Aktivieren des \_ Streamings</span><span class="sxs-lookup"><span data-stu-id="1a631-180">MFNETSOURCE\_ENABLE\_STREAMING</span></span>](mfnetsource-enable-streaming-property.md) | <span data-ttu-id="1a631-181">Aktiviert oder deaktiviert RTSPU, RTSPT und http.</span><span class="sxs-lookup"><span data-stu-id="1a631-181">Enables or disables RTSPU, RTSPT, and HTTP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1a631-182">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a631-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a631-183">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a631-183">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




