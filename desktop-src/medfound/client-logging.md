---
description: Client Protokollierung
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Client Protokollierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214338"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="52247-103">Client Protokollierung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="52247-103">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="52247-104">Die Netzwerkquelle unterstützt die Client Protokollierung, die es dem Medienserver ermöglicht, die Aktivität der Clients zu verfolgen, die eine Verbindung mit ihm herstellen.</span><span class="sxs-lookup"><span data-stu-id="52247-104">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="52247-105">Client Protokolle ermöglichen einem Server das Aufzeichnen von Verbindungs-, Rendering-und streamingstatistiken.</span><span class="sxs-lookup"><span data-stu-id="52247-105">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="52247-106">Diese Protokolle können von Inhaltsanbietern in verschiedenen Szenarien (z. b.) verwendet werden, um die Nutzung von Medienservern zu verfolgen und eine Abrechnung zu generieren, oder um entsprechend der Geschwindigkeit des Client Netzwerks geeignete Inhalte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52247-106">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="52247-107">Eine Protokolldatei enthält mehrere Client Ereignis Einträge.</span><span class="sxs-lookup"><span data-stu-id="52247-107">A log file contains several client event entries.</span></span> <span data-ttu-id="52247-108">Jeder Protokolleintrag enthält eine Reihe von Feldern, die durch Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="52247-108">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="52247-109">Es gibt zwei Arten von Client Protokollen: *Rendering* (Wiedergabe) und *Streaming* (empfangen).</span><span class="sxs-lookup"><span data-stu-id="52247-109">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="52247-110">Da Inhalte gleichzeitig abgespielt und gestreamt werden können, kann der Client eine Kombination beider Protokolldaten Typen senden.</span><span class="sxs-lookup"><span data-stu-id="52247-110">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="52247-111">In bestimmten Fällen können für dieselbe Sitzung zwei Protokolleinträge vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="52247-111">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="52247-112">Wenn z. b. der schnelle Cache aktiviert ist, kann der Client den gestreamten Inhalt abschließen, bevor er das Rendering abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="52247-112">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="52247-113">In diesem Fall werden die streamingprotokolllierdaten vor den renderingprotokollierung gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-113">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="52247-114">Der Client sendet renderingprotokolllierungsdaten an den Server, wenn sich der Client von einem beliebigen Wiedergabe Zustand ("Wiedergabe", "schnell vorwärts" oder "Zurückspulen") in einen nicht Wiedergabe-Zustand ändert (beenden, anhalten, Ende des Streams und Anfang des Streams).</span><span class="sxs-lookup"><span data-stu-id="52247-114">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="52247-115">Wenn Daten für ein renderingprotokoll übermittelt werden, wird eine Verbindung direkt mit dem Medienserver oder einem konfigurierten Proxy Server hergestellt.</span><span class="sxs-lookup"><span data-stu-id="52247-115">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="52247-116">Wenn der Inhalt in einer temporären lokalen Cachedatei auf dem Computer gespeichert ist, auf dem der-Client ausgeführt wird, kann der Client eine Datei aus dem lokalen Cache lesen und die renderingprotokolllierdaten übermitteln, um anzugeben, dass der Inhalt wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="52247-116">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="52247-117">In diesem Fall liest der Client eine Datei aus dem lokalen Cache, der renderingprotokolleintrag enthält keine Netzwerk Statistiken, und das Protokoll ist auf Cache festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52247-117">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="52247-118">Der Client sendet streamingprotokolllierdaten an den Server, um anzugeben, wie der Client den Inhalt empfangen hat, aber nicht, wie er gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="52247-118">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="52247-119">Der Client kann das Streamingprotokoll lange senden, bevor der Client das Rendern des Inhalts abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="52247-119">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="52247-120">Dieses Thema enthält keine Informationen über alle Protokoll Felder.</span><span class="sxs-lookup"><span data-stu-id="52247-120">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="52247-121">Eine umfassende Referenz finden Sie unter [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="52247-121">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="52247-122">Konfigurieren von Protokoll Feldern</span><span class="sxs-lookup"><span data-stu-id="52247-122">Configuring Log Fields</span></span>

<span data-ttu-id="52247-123">Media Foundation ermöglicht es dem Client, die Netzwerkquelle mithilfe von Eigenschaften zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="52247-123">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="52247-124">Die Anwendung muss die entsprechenden Eigenschaften in einem Eigenschafts Speicher festlegen und an eine der Quell Konflikt Löser-Methoden übergeben.</span><span class="sxs-lookup"><span data-stu-id="52247-124">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="52247-125">Der Quell Löser erstellt die Netzwerkquelle wie angefordert und öffnet eine Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="52247-125">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="52247-126">Wenn die Verbindung erfolgreich hergestellt wurde, sendet der Client Informationen über sich selbst.</span><span class="sxs-lookup"><span data-stu-id="52247-126">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="52247-127">In der folgenden Tabelle werden die Protokoll Felder und die entsprechenden Eigenschaften beschrieben, die von einer Anwendung über den quellresolver festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="52247-127">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="52247-128">Diese Informationen werden während der Sitzung nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="52247-128">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="52247-129">Protokollierungs Feld</span><span class="sxs-lookup"><span data-stu-id="52247-129">Logging field</span></span></th>
<th><span data-ttu-id="52247-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52247-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52247-131">c-playerid</span><span class="sxs-lookup"><span data-stu-id="52247-131">c-playerid</span></span></td>
<td><span data-ttu-id="52247-132">Eindeutige Identifikation des Players.</span><span class="sxs-lookup"><span data-stu-id="52247-132">Unique identification of the player.</span></span> <span data-ttu-id="52247-133">Diese Informationen werden am Anfang der Verbindung gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-133">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="52247-134">In der Regel handelt es sich hierbei um eine GUID des Clients.</span><span class="sxs-lookup"><span data-stu-id="52247-134">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="52247-135">Der Client kann diese Informationen in der <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> -Eigenschaft an den-Server senden.</span><span class="sxs-lookup"><span data-stu-id="52247-135">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="52247-136">Diese Informationen werden vom Client am Anfang der Verbindung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-136">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="52247-137">Beispiel Wert: &quot; {c579d042-CECC-11d1-BB31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="52247-137">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52247-138">c-Playerversion</span><span class="sxs-lookup"><span data-stu-id="52247-138">c-playerversion</span></span></td>
<td><span data-ttu-id="52247-139">Die Versionsnummer des Players, der am Anfang der Verbindung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="52247-139">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="52247-140">Der Client kann diese Informationen in der <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> -Eigenschaft an den-Server senden.</span><span class="sxs-lookup"><span data-stu-id="52247-140">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="52247-141">Diese Informationen werden vom Client am Anfang der Verbindung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-141">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52247-142">CS (Benutzer-Agent)</span><span class="sxs-lookup"><span data-stu-id="52247-142">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="52247-143">Der Browsertyp, der verwendet wird, wenn der Player in einen Browser eingebettet wurde.</span><span class="sxs-lookup"><span data-stu-id="52247-143">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="52247-144">Dieser Wert kann vom Client in der <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="52247-144">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="52247-145">Wenn der Spieler nicht eingebettet war, verweist dieses Feld auf den Benutzer-Agent des Clients, der das Protokoll generiert hat.</span><span class="sxs-lookup"><span data-stu-id="52247-145">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="52247-146">In diesem Fall muss der Client die <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="52247-146">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="52247-147">Diese Informationen werden vom Client am Anfang der Verbindung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-147">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="52247-148">Beispiel Wert: &quot; Mozilla/4.0 _ (kompatibel; _MSIE_4.01; _Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="52247-148">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52247-149">CS (Referer)</span><span class="sxs-lookup"><span data-stu-id="52247-149">cs(Referer)</span></span></td>
<td><span data-ttu-id="52247-150">Die URL der Webseite, in die der Player eingebettet wurde (wenn Sie eingebettet wurde).</span><span class="sxs-lookup"><span data-stu-id="52247-150">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="52247-151">Der Client kann diese Informationen in der <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> -Eigenschaft an den-Server senden.</span><span class="sxs-lookup"><span data-stu-id="52247-151">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="52247-152">Diese Informationen werden vom Client am Ende der Verbindung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-152">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="52247-153">Beispiel Wert: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="52247-153">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52247-154">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="52247-154">c-hostexe</span></span></td>
<td><span data-ttu-id="52247-155">Für Player-Protokolleinträge das Host Programm (. exe), das ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="52247-155">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="52247-156">Beispielsweise eine Webseite in einem Browser, ein Microsoft Visual Basic Applet oder ein eigenständiger Player.</span><span class="sxs-lookup"><span data-stu-id="52247-156">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="52247-157">Der Client kann diese Informationen in der <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> -Eigenschaft an den-Server senden.</span><span class="sxs-lookup"><span data-stu-id="52247-157">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="52247-158">Diese Informationen werden vom Client am Ende der Verbindung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-158">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="52247-159">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="52247-159">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="52247-160">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="52247-160">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="52247-161">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="52247-161">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52247-162">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="52247-162">c-hostexever</span></span></td>
<td><span data-ttu-id="52247-163">Die Versionsnummer des Host Programms (. exe).</span><span class="sxs-lookup"><span data-stu-id="52247-163">Host program (.exe) version number.</span></span> <span data-ttu-id="52247-164">Der Client kann diese Informationen in der <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> -Eigenschaft an den-Server senden.</span><span class="sxs-lookup"><span data-stu-id="52247-164">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="52247-165">Diese Informationen werden vom Client am Ende der Verbindung an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="52247-165">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="52247-166">Das folgende Codebeispiel zeigt, wie eine Client Anwendung die Netzwerkquelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="52247-166">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="52247-167">In diesem Beispiel wird das Protokollfeld "c-hostexe" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52247-167">This example sets the "c-hostexe" log field.</span></span>


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



## <a name="retrieving-network-statistics"></a><span data-ttu-id="52247-168">Netzwerk Statistiken werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="52247-168">Retrieving Network Statistics</span></span>

<span data-ttu-id="52247-169">Wenn die Anwendung eine der Quell Konflikt Löser-Methoden aufruft, wird die Netzwerkquelle erstellt, die im Eigenschaften Speicher angegebenen Eigenschaften festgelegt und eine Sitzung mit dem Medienserver geöffnet.</span><span class="sxs-lookup"><span data-stu-id="52247-169">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="52247-170">Zusätzlich zu den konfigurierbaren Informationen, die im vorherigen Abschnitt beschrieben wurden, werden zusätzliche Daten zwischen dem Server und dem Client am Anfang der Sitzung, während des Streamings und beim Schließen der Sitzung übertragen.</span><span class="sxs-lookup"><span data-stu-id="52247-170">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="52247-171">Die Anwendung kann Netzwerk Statistiken mithilfe des Dienst Bezeichners für den **mfnetsource- \_ Statistik \_ Dienst** abrufen.</span><span class="sxs-lookup"><span data-stu-id="52247-171">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="52247-172">Um diesen Dienst zu verwenden, kann die Anwendung die [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) -Funktion aufrufen, um den Eigenschaften Speicher zu erhalten, der Netzwerk Statistiken in der [**mfnetsource- \_ Statistik**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="52247-172">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="52247-173">Bestimmte Werte können abgerufen werden, indem der entsprechende Bezeichner bereitgestellt wird, der in der **mfnetsource \_ Statistics \_ IDs** -Enumeration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="52247-173">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="52247-174">Im folgenden Codebeispiel wird gezeigt, wie der-Dienst verwendet wird, um die Anzahl der vom Client empfangenen Pakete zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="52247-174">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


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



<span data-ttu-id="52247-175">In der folgenden Liste werden einige der in [**MF-Quell \_ Statistik- \_ IDs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)definierten Netzwerk Statistik-IDs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="52247-175">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="52247-176">Netzwerk Statistik Bezeichner</span><span class="sxs-lookup"><span data-stu-id="52247-176">Network statistics identifier</span></span>              | <span data-ttu-id="52247-177">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52247-177">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52247-178">**MF-Quell- \_ ID avgbandwidthbit/s \_**</span><span class="sxs-lookup"><span data-stu-id="52247-178">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="52247-179">Die durchschnittliche Bandbreite (in Bits pro Sekunde), an der der Client mit dem Server verbunden war.</span><span class="sxs-lookup"><span data-stu-id="52247-179">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="52247-180">Der Wert wird über die gesamte Dauer der Verbindung berechnet.</span><span class="sxs-lookup"><span data-stu-id="52247-180">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="52247-181">**MF-Quell- \_ bufferingcount- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-181">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="52247-182">Gibt an, wie oft der Client während der Wiedergabe des Streams gepuffert hat.</span><span class="sxs-lookup"><span data-stu-id="52247-182">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="52247-183">**MF-Quell- \_ ID (bytesempfangene) \_**</span><span class="sxs-lookup"><span data-stu-id="52247-183">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="52247-184">Anzahl von Bytes, die vom Client vom Server empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="52247-184">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="52247-185">Der Wert umfasst keinen Aufwand, der vom Netzwerk Stapel hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="52247-185">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="52247-186">Derselbe Inhalt, der mithilfe verschiedener Protokolle gestreamt wird, kann zu unterschiedlichen Werten führen.</span><span class="sxs-lookup"><span data-stu-id="52247-186">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="52247-187">**MF NetSource \_ linkbandwidth- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-187">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="52247-188">Maximale verfügbare Bandbreite des Clients in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="52247-188">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="52247-189">**MF NetSource- \_ lostpakete- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-189">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="52247-190">Die Anzahl der vom Server gesendeten Pakete, die während der Übertragung verloren gegangen sind und nie vom Client abgespielt wurden.</span><span class="sxs-lookup"><span data-stu-id="52247-190">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="52247-191">Der Wert enthält keine TCP-oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="52247-191">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="52247-192">**mfnetsource- \_ recvpakete- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-192">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="52247-193">Anzahl der vom Server empfangenen Pakete. der Wert enthält keine TCP-oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="52247-193">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="52247-194">**MF-Quell \_ Wiederherstellungstyp- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-194">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="52247-195">Im Netzwerk verlorene Pakete, die auf der Client Ebene repariert und wieder hergestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="52247-195">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="52247-196">Dieser Wert enthält keine TCP-oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="52247-196">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="52247-197">**MF-Quell- \_ ID resendsangeforderten \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-197">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="52247-198">Die Anzahl der Anforderungen, die vom Client zum Empfangen neuer Pakete gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="52247-198">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="52247-199">Dieser Wert enthält keine TCP-oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="52247-199">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="52247-200">**ID des MF-Quell \_ Wiederherstellung. \_**</span><span class="sxs-lookup"><span data-stu-id="52247-200">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="52247-201">Anzahl der wiederhergestellten Pakete, weil Sie über UDP erneut gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="52247-201">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="52247-202">Dieser Wert enthält keine TCP-oder UDP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="52247-202">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="52247-203">Dieses Feld enthält eine NULL, es sei denn, der Client verwendet UDP Resend.</span><span class="sxs-lookup"><span data-stu-id="52247-203">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="52247-204">**MF-Quell- \_ bufferprogress- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-204">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="52247-205">Der Prozentsatz des bei der Pufferung gefüllten Broadcasts-Puffers.</span><span class="sxs-lookup"><span data-stu-id="52247-205">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="52247-206">**MF-Quell \_ Protokoll- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-206">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="52247-207">Protokoll, das für den Zugriff auf den Stream verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52247-207">Protocol used to access the stream.</span></span> <span data-ttu-id="52247-208">Dies kann sich von dem vom Client angeforderten Protokoll unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="52247-208">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="52247-209">**MF-Quell- \_ Transport- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="52247-209">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="52247-210">Transport Protokoll, das zum Übermitteln des Streams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52247-210">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="52247-211">Dabei muss es sich entweder um UDP oder TCP handeln.</span><span class="sxs-lookup"><span data-stu-id="52247-211">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="52247-212">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52247-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52247-213">Netzwerk Quell Features</span><span class="sxs-lookup"><span data-stu-id="52247-213">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="52247-214">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52247-214">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

