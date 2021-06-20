---
description: Erfahren Sie mehr über die Clientprotokollierung für Microsoft Media Foundation. Die Protokollierung bietet dem Medienserver die Möglichkeit, die Aktivität der Clients nachverfolgungen, die eine Verbindung mit ihm herstellen.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Clientprotokollierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d994531ff16466054ca0645a35082a4845e4aa4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409933"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="ae95f-104">Clientprotokollierung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="ae95f-104">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="ae95f-105">Die Netzwerkquelle unterstützt die Clientprotokollierung, wodurch der Medienserver die Aktivität der Clients nachverfolgen kann, die eine Verbindung damit herstellen.</span><span class="sxs-lookup"><span data-stu-id="ae95f-105">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="ae95f-106">Clientprotokolle ermöglichen einem Server das Aufzeichnen von Verbindungs-, Rendering- und Streamingstatistiken.</span><span class="sxs-lookup"><span data-stu-id="ae95f-106">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="ae95f-107">Diese Protokolle können von Inhaltsanbietern in verschiedenen Szenarien verwendet werden, z. B. zum Nachverfolgen der Nutzung von Medienservern und Generieren von Abrechnungen oder zur Bereitstellung geeigneter Inhalte in Abhängigkeit von der Geschwindigkeit des Clientnetzwerks.</span><span class="sxs-lookup"><span data-stu-id="ae95f-107">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="ae95f-108">Eine Protokolldatei enthält mehrere Clientereigniseinträge.</span><span class="sxs-lookup"><span data-stu-id="ae95f-108">A log file contains several client event entries.</span></span> <span data-ttu-id="ae95f-109">Jeder Protokolleintrag enthält eine Reihe von durch Leerzeichen getrennten Feldern.</span><span class="sxs-lookup"><span data-stu-id="ae95f-109">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="ae95f-110">Es gibt zwei Arten von Clientprotokollen: *Rendering* (Wiedergabe) und *Streaming* (Empfangen).</span><span class="sxs-lookup"><span data-stu-id="ae95f-110">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="ae95f-111">Da Inhalte gleichzeitig abgespielt und gestreamt werden können, kann der Client eine Kombination aus beiden Protokolldatentypen senden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-111">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="ae95f-112">In bestimmten Fällen können zwei Protokolleinträge für dieselbe Sitzung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ae95f-112">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="ae95f-113">Wenn beispielsweise Fast Cache aktiviert ist, kann der Client den Empfang des gestreamten Inhalts beenden, bevor er das Rendern abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="ae95f-113">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="ae95f-114">In diesem Fall werden die Streamingprotokolldaten vor den Renderingprotokolldaten gesendet.</span><span class="sxs-lookup"><span data-stu-id="ae95f-114">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="ae95f-115">Der Client sendet Renderingprotokolldaten an den Server, wenn sich der Client von einem wiedergabebasierten Zustand (Wiedergabe, schnelles Vorwärts- oder Zurücksingen) in einen Nichtwiedergabezustand (Beenden, Anhalten, Ende des Streams und Anfang des Streams) ändert.</span><span class="sxs-lookup"><span data-stu-id="ae95f-115">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="ae95f-116">Wenn Daten für ein Renderingprotokoll übermittelt werden, wird eine Verbindung direkt mit dem Medienserver oder einem konfigurierten Proxyserver hergestellt.</span><span class="sxs-lookup"><span data-stu-id="ae95f-116">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="ae95f-117">Wenn der Inhalt in einer temporären lokalen Cachedatei auf dem Computer gespeichert wird, auf dem der Client ausgeführt wird, kann der Client eine Datei aus seinem lokalen Cache lesen und die Renderingprotokolldaten übermitteln, um anzugeben, dass der Inhalt abgespielt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae95f-117">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="ae95f-118">In diesem Fall liest der Client eine Datei aus seinem lokalen Cache, der Eintrag des Renderingprotokolls enthält keine Netzwerkstatistiken, und das Protokoll ist auf Cache festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ae95f-118">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="ae95f-119">Der Client sendet Streamingprotokolldaten an den Server, um anzugeben, wie der Client den Inhalt empfangen hat, aber nicht wie er gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="ae95f-119">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="ae95f-120">Der Client kann das Streamingprotokoll lange senden, bevor der Client das Rendern des Inhalts abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="ae95f-120">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="ae95f-121">Dieses Thema enthält keine Informationen zu allen Protokollfeldern.</span><span class="sxs-lookup"><span data-stu-id="ae95f-121">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="ae95f-122">Eine vollständige Referenz finden Sie unter [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="ae95f-122">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="ae95f-123">Konfigurieren von Protokollfeldern</span><span class="sxs-lookup"><span data-stu-id="ae95f-123">Configuring Log Fields</span></span>

<span data-ttu-id="ae95f-124">Media Foundation ermöglicht es dem Client, die Netzwerkquelle mithilfe von Eigenschaften zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ae95f-124">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="ae95f-125">Die Anwendung muss die entsprechenden Eigenschaften in einem Eigenschaftenspeicher festlegen und an eine der Quellre konfliktlösermethoden übergeben.</span><span class="sxs-lookup"><span data-stu-id="ae95f-125">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="ae95f-126">Der Quellre resolver erstellt die Netzwerkquelle wie angefordert und öffnet eine Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="ae95f-126">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="ae95f-127">Wenn die Verbindung erfolgreich hergestellt wurde, sendet der Client Informationen über sich selbst.</span><span class="sxs-lookup"><span data-stu-id="ae95f-127">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="ae95f-128">In der folgenden Tabelle werden die Protokollfelder und die entsprechenden Eigenschaften beschrieben, die eine Anwendung über den Quellre resolver festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="ae95f-128">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="ae95f-129">Diese Informationen ändern sich während der Sitzung nicht.</span><span class="sxs-lookup"><span data-stu-id="ae95f-129">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae95f-130">Protokollierungsfeld</span><span class="sxs-lookup"><span data-stu-id="ae95f-130">Logging field</span></span></th>
<th><span data-ttu-id="ae95f-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae95f-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae95f-132">c-playerid</span><span class="sxs-lookup"><span data-stu-id="ae95f-132">c-playerid</span></span></td>
<td><span data-ttu-id="ae95f-133">Eindeutige Identifikation des Players.</span><span class="sxs-lookup"><span data-stu-id="ae95f-133">Unique identification of the player.</span></span> <span data-ttu-id="ae95f-134">Diese Informationen werden am Anfang der Verbindung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ae95f-134">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="ae95f-135">In der Regel ist dies eine GUID des Clients.</span><span class="sxs-lookup"><span data-stu-id="ae95f-135">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="ae95f-136">Der Client kann diese Informationen an den Server in der <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> senden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-136">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="ae95f-137">Der Client sendet diese Informationen am Anfang der Verbindung an den Server.</span><span class="sxs-lookup"><span data-stu-id="ae95f-137">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="ae95f-138">Beispielwert: &quot; {c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="ae95f-138">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae95f-139">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="ae95f-139">c-playerversion</span></span></td>
<td><span data-ttu-id="ae95f-140">Die Versionsnummer des Players, der am Anfang der Verbindung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae95f-140">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="ae95f-141">Der Client kann diese Informationen an den Server in der MFNETSOURCE_PLAYERVERSION <a href="mfnetsource-playerversion-property.md"><strong>senden.</strong></a></span><span class="sxs-lookup"><span data-stu-id="ae95f-141">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="ae95f-142">Der Client sendet diese Informationen am Anfang der Verbindung an den Server.</span><span class="sxs-lookup"><span data-stu-id="ae95f-142">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae95f-143">cs(User-Agent)</span><span class="sxs-lookup"><span data-stu-id="ae95f-143">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="ae95f-144">Browsertyp, der verwendet wird, wenn der Player in einen Browser eingebettet wurde.</span><span class="sxs-lookup"><span data-stu-id="ae95f-144">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="ae95f-145">Dieser Wert kann vom Client in der Eigenschaft MFNETSOURCE_BROWSERUSERAGENT <a href="mfnetsource-browseruseragent-property.md"><strong>werden.</strong></a></span><span class="sxs-lookup"><span data-stu-id="ae95f-145">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="ae95f-146">Wenn der Player nicht eingebettet wurde, bezieht sich dieses Feld auf den Benutzer-Agent des Clients, der das Protokoll generiert hat.</span><span class="sxs-lookup"><span data-stu-id="ae95f-146">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="ae95f-147">In diesem Fall muss der Client die eigenschaft <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> festlegen.</span><span class="sxs-lookup"><span data-stu-id="ae95f-147">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="ae95f-148">Der Client sendet diese Informationen am Anfang der Verbindung an den Server.</span><span class="sxs-lookup"><span data-stu-id="ae95f-148">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="ae95f-149">Beispielwert: &quot; Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="ae95f-149">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae95f-150">cs(Referer)</span><span class="sxs-lookup"><span data-stu-id="ae95f-150">cs(Referer)</span></span></td>
<td><span data-ttu-id="ae95f-151">URL der Webseite, in die der Player eingebettet wurde (wenn er eingebettet wurde).</span><span class="sxs-lookup"><span data-stu-id="ae95f-151">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="ae95f-152">Der Client kann diese Informationen an den Server in der eigenschaft <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> senden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-152">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="ae95f-153">Der Client sendet diese Informationen am Ende der Verbindung an den Server.</span><span class="sxs-lookup"><span data-stu-id="ae95f-153">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="ae95f-154">Beispielwert: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="ae95f-154">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae95f-155">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="ae95f-155">c-hostexe</span></span></td>
<td><span data-ttu-id="ae95f-156">Bei Playerprotokolleinträgen wird das Hostprogramm (.exe), das ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae95f-156">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="ae95f-157">Beispielsweise eine Webseite in einem Browser, ein Microsoft Visual Basic Applet oder ein eigenständiger Player.</span><span class="sxs-lookup"><span data-stu-id="ae95f-157">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="ae95f-158">Der Client kann diese Informationen an den Server in der <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> senden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-158">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="ae95f-159">Der Client sendet diese Informationen am Ende der Verbindung an den Server.</span><span class="sxs-lookup"><span data-stu-id="ae95f-159">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="ae95f-160">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="ae95f-160">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="ae95f-161">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="ae95f-161">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="ae95f-162">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="ae95f-162">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae95f-163">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="ae95f-163">c-hostexever</span></span></td>
<td><span data-ttu-id="ae95f-164">Versionsnummer des Hostprogramms (.exe)</span><span class="sxs-lookup"><span data-stu-id="ae95f-164">Host program (.exe) version number.</span></span> <span data-ttu-id="ae95f-165">Der Client kann diese Informationen an den Server in der <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> senden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-165">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="ae95f-166">Der Client sendet diese Informationen am Ende der Verbindung an den Server.</span><span class="sxs-lookup"><span data-stu-id="ae95f-166">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ae95f-167">Das folgende Codebeispiel zeigt, wie eine Clientanwendung die Netzwerkquelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ae95f-167">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="ae95f-168">In diesem Beispiel wird das Protokollfeld "c-hostexe" definiert.</span><span class="sxs-lookup"><span data-stu-id="ae95f-168">This example sets the "c-hostexe" log field.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a><span data-ttu-id="ae95f-169">Abrufen von Netzwerkstatistiken</span><span class="sxs-lookup"><span data-stu-id="ae95f-169">Retrieving Network Statistics</span></span>

<span data-ttu-id="ae95f-170">Wenn die Anwendung eine der Quellre resolvermethoden aufruft, erstellt sie die Netzwerkquelle, legt die im Eigenschaftenspeicher angegebenen Eigenschaften fest und öffnet eine Sitzung mit dem Medienserver.</span><span class="sxs-lookup"><span data-stu-id="ae95f-170">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="ae95f-171">Zusätzlich zu den im vorherigen Abschnitt beschriebenen konfigurierbaren Informationen werden zu Beginn der Sitzung, während des Streamings und beim Schließen der Sitzung zusätzliche Daten zwischen dem Server und dem Client übertragen.</span><span class="sxs-lookup"><span data-stu-id="ae95f-171">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="ae95f-172">Die Anwendung kann Netzwerkstatistiken mithilfe des **Dienstbezeichners MFNETSOURCE \_ STATISTICS \_ SERVICE** abrufen.</span><span class="sxs-lookup"><span data-stu-id="ae95f-172">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="ae95f-173">Um diesen Dienst zu verwenden, kann die Anwendung die [**MFGetService-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen, um den Eigenschaftenspeicher zu erhalten, der Netzwerkstatistiken in der [**MFNETSOURCE \_ STATISTICS-Eigenschaft**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enthält.</span><span class="sxs-lookup"><span data-stu-id="ae95f-173">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="ae95f-174">Bestimmte Werte können abgerufen werden, indem der entsprechende Bezeichner angegeben wird, der in der **MFNETSOURCE \_ STATISTICS \_ IDS-Enumeration definiert** ist.</span><span class="sxs-lookup"><span data-stu-id="ae95f-174">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="ae95f-175">Das folgende Codebeispiel zeigt, wie sie den Dienst verwenden, um die Anzahl der vom Client empfangenen Pakete zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae95f-175">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



<span data-ttu-id="ae95f-176">In der folgenden Liste werden einige der in [**MFNETSOURCE STATISTICS IDS definierten Netzwerkstatistikbezeichner \_ \_ beschrieben.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)</span><span class="sxs-lookup"><span data-stu-id="ae95f-176">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="ae95f-177">Netzwerkstatistikbezeichner</span><span class="sxs-lookup"><span data-stu-id="ae95f-177">Network statistics identifier</span></span>              | <span data-ttu-id="ae95f-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae95f-178">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae95f-179">**MFNETSOURCE-ID \_ "AVGBANDWIDTHBPS" \_**</span><span class="sxs-lookup"><span data-stu-id="ae95f-179">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="ae95f-180">Durchschnittliche Bandbreite (in Bits pro Sekunde), bei der der Client mit dem Server verbunden war.</span><span class="sxs-lookup"><span data-stu-id="ae95f-180">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="ae95f-181">Der Wert wird für die gesamte Dauer der Verbindung berechnet.</span><span class="sxs-lookup"><span data-stu-id="ae95f-181">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="ae95f-182">**MFNETSOURCE \_ \_ BUFFERINGCOUNT-ID**</span><span class="sxs-lookup"><span data-stu-id="ae95f-182">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="ae95f-183">Gibt an, wie oft der Client während der Wiedergabe des Streams gepuffert hat.</span><span class="sxs-lookup"><span data-stu-id="ae95f-183">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="ae95f-184">**MFNETSOURCE \_ BYTESRECEIVED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ae95f-184">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="ae95f-185">Anzahl der vom Client vom Server empfangenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="ae95f-185">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="ae95f-186">Der Wert enthält keinen Mehraufwand, der durch den Netzwerkstapel hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ae95f-186">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="ae95f-187">Derselbe Inhalt, der mit verschiedenen Protokollen gestreamt wird, kann zu unterschiedlichen Werten führen.</span><span class="sxs-lookup"><span data-stu-id="ae95f-187">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="ae95f-188">**\_MFNETSOURCE-LINKBANDWIDTH-ID \_**</span><span class="sxs-lookup"><span data-stu-id="ae95f-188">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="ae95f-189">Maximale verfügbare Bandbreite des Clients in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="ae95f-189">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="ae95f-190">**MFNETSOURCE \_ LOSTPACKETS-ID \_**</span><span class="sxs-lookup"><span data-stu-id="ae95f-190">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="ae95f-191">Anzahl von Paketen, die vom Server gesendet wurden, aber während der Übertragung verloren gegangen sind und nie vom Client abgespielt wurden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-191">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="ae95f-192">Der Wert enthält keine TCP- oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="ae95f-192">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="ae95f-193">**MFNETSOURCE \_ RECVPACKETS-ID \_**</span><span class="sxs-lookup"><span data-stu-id="ae95f-193">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="ae95f-194">Anzahl der vom Server empfangenen Pakete Der Wert enthält keine TCP- oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="ae95f-194">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="ae95f-195">**MFNETSOURCE \_ RECOVEREDBYECCPACKETS-ID \_**</span><span class="sxs-lookup"><span data-stu-id="ae95f-195">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="ae95f-196">Verlorene Pakete im Netzwerk, die auf Clientebene repariert und wiederhergestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-196">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="ae95f-197">Dieser Wert enthält keine TCP- oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="ae95f-197">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="ae95f-198">**MFNETSOURCE \_ RESENDSREQUESTED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ae95f-198">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="ae95f-199">Die Anzahl der Anforderungen, die vom Client zum Empfangen neuer Pakete gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-199">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="ae95f-200">Dieser Wert enthält keine TCP- oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="ae95f-200">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="ae95f-201">**MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ae95f-201">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="ae95f-202">Anzahl der Pakete, die wiederhergestellt wurden, weil sie über UDP erneut gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-202">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="ae95f-203">Dieser Wert enthält keine TCP- oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="ae95f-203">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="ae95f-204">Dieses Feld enthält eine Null, es sei denn, der Client verwendet UDP erneut.</span><span class="sxs-lookup"><span data-stu-id="ae95f-204">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="ae95f-205">**MFNETSOURCE \_ \_ BUFFERPROGRESS-ID**</span><span class="sxs-lookup"><span data-stu-id="ae95f-205">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="ae95f-206">Der Prozentsatz des während der Pufferung gefüllten Playoutpuffers.</span><span class="sxs-lookup"><span data-stu-id="ae95f-206">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="ae95f-207">**\_MFNETSOURCE-PROTOKOLL-ID \_**</span><span class="sxs-lookup"><span data-stu-id="ae95f-207">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="ae95f-208">Protokoll, das für den Zugriff auf den Stream verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae95f-208">Protocol used to access the stream.</span></span> <span data-ttu-id="ae95f-209">Dies kann sich vom vom Client angeforderten Protokoll unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ae95f-209">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="ae95f-210">**\_MFNETSOURCE-TRANSPORT-ID \_**</span><span class="sxs-lookup"><span data-stu-id="ae95f-210">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="ae95f-211">Transportprotokoll, das zum Übermitteln des Streams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae95f-211">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="ae95f-212">Dies muss entweder UDP oder TCP sein.</span><span class="sxs-lookup"><span data-stu-id="ae95f-212">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="ae95f-213">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae95f-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae95f-214">Netzwerkquellfeatures</span><span class="sxs-lookup"><span data-stu-id="ae95f-214">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="ae95f-215">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae95f-215">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

