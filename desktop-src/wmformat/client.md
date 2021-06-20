---
title: Clientprotokollierung (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über die Clientprotokollierung für das Windows Media Format 11 SDK. Die Protokollierung bietet dem Medienserver die Möglichkeit, die Aktivität der Clients nachverfolgungen, die eine Verbindung mit ihm herstellen.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, Clientprotokollierung
- Windows Media Format SDK, Protokollierung
- Advanced Systems Format (ASF), Clientprotokollierung
- ASF (Advanced Systems Format), Clientprotokollierung
- Advanced Systems Format (ASF), Protokollierung
- ASF (Advanced Systems Format), Protokollierung
- Clientprotokollierung
- Protokollieren von Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095e01fcf0730fdec8d06a931a9a988ca79ea77f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406263"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="c7a47-112">Clientprotokollierung (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="c7a47-112">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="c7a47-113">Wenn das Readerobjekt Daten von einem Server liest, sendet es Protokollierungsinformationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="c7a47-113">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="c7a47-114">Inhaltsanbieter verwenden diese Informationen in der Regel, um die Dienstqualität zu messen, Abrechnungsinformationen zu generieren oder Werbung nachverfolgungen.</span><span class="sxs-lookup"><span data-stu-id="c7a47-114">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="c7a47-115">Die Protokollierungsinformationen enthalten keine personenbezogenen Daten.</span><span class="sxs-lookup"><span data-stu-id="c7a47-115">The logging information contains no personal data.</span></span>

<span data-ttu-id="c7a47-116">Die Anwendung kann einige der protokollierten Informationen angeben, indem sie die [**IWMReaderAdvanced::SetClientInfo-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) für das Readerobjekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="c7a47-116">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="c7a47-117">Sie können z. B. die Benutzer-Agent-Zeichenfolge, den Namen der Playeranwendung oder die Webseite angeben, die den Player hostet.</span><span class="sxs-lookup"><span data-stu-id="c7a47-117">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="c7a47-118">Die Protokollierungsinformationen enthalten eine GUID, die die Sitzung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c7a47-118">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="c7a47-119">Standardmäßig generiert der Leser eine anonyme Sitzungs-ID.</span><span class="sxs-lookup"><span data-stu-id="c7a47-119">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="c7a47-120">Optional kann der Leser stattdessen eine ID senden, die den aktuellen Benutzer eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c7a47-120">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="c7a47-121">Um dieses Feature zu aktivieren, rufen Sie [**die IWMReaderAdvanced2::SetLogClientID-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) mit dem Wert **TRUE auf.**</span><span class="sxs-lookup"><span data-stu-id="c7a47-121">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="c7a47-122">Sie können das Readerobjekt so konfigurieren, dass die Protokollierungsinformationen zusätzlich zum Ursprungsserver an einen anderen Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7a47-122">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="c7a47-123">Rufen Sie dazu die [**IWMReaderNetworkConfig::AddLoggingUrl-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) mit der URL des Servers auf.</span><span class="sxs-lookup"><span data-stu-id="c7a47-123">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="c7a47-124">Diese URL sollte auf ein Skript oder eine ausführbare Datei verweisen, die HTTP GET- und POST-Anforderungen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="c7a47-124">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="c7a47-125">Sie können den Multicast- und Protokollierungsanmelde-Agent (wmsiislog.dll) verwenden oder ein benutzerdefiniertes ASP- oder CGI-Skript schreiben, um die Protokolldaten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c7a47-125">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="c7a47-126">Sie können die gleiche Funktionalität erhalten, indem Sie eine serverseitige Wiedergabeliste mit einem **logURL-Attribut** erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7a47-126">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="c7a47-127">Wenn das Readerobjekt das Protokoll sendet, führt es Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="c7a47-127">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="c7a47-128">Sendet eine leere GET-Anforderung an den Server.</span><span class="sxs-lookup"><span data-stu-id="c7a47-128">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="c7a47-129">Analysiert die Serverantwort für eine der folgenden Zeichenfolgen:</span><span class="sxs-lookup"><span data-stu-id="c7a47-129">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="c7a47-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` wobei "0.0.0.0" eine beliebige gültige Versionsnummer ist.</span><span class="sxs-lookup"><span data-stu-id="c7a47-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="c7a47-131">Sendet eine POST-Anforderung mit den Protokollinformationen.</span><span class="sxs-lookup"><span data-stu-id="c7a47-131">Sends a POST request with the log information.</span></span>

<span data-ttu-id="c7a47-132">Der folgende Code zeigt ein ASP-Beispielskript, das die Protokollierungsinformationen empfängt und in eine Datei schreibt:</span><span class="sxs-lookup"><span data-stu-id="c7a47-132">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



<span data-ttu-id="c7a47-133">Sie können mehrere Server angeben, um Protokollierungsinformationen zu empfangen. Rufen Sie **addLoggingUrl einfach einmal** mit jeder URL auf.</span><span class="sxs-lookup"><span data-stu-id="c7a47-133">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="c7a47-134">Um die Liste der Server zu löschen, die Protokolle empfangen, rufen Sie [**die IWMReaderNetworkConfig::ResetLoggingUrlList-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) auf.</span><span class="sxs-lookup"><span data-stu-id="c7a47-134">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7a47-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7a47-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7a47-136">**Implementieren von Netzwerkfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c7a47-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="c7a47-137">**IWMReaderAdvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c7a47-137">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="c7a47-138">**IWMReaderAdvanced2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c7a47-138">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




