---
title: Client Protokollierung (Windows Media-Format 11 SDK)
description: Client Protokollierung
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media-Format-SDK, Client Protokollierung
- Windows Media-Format-SDK, Protokollierung
- Advanced Systems Format (ASF), Client Protokollierung
- ASF (Advanced Systems Format), Client Protokollierung
- Advanced Systems Format (ASF), Protokollierung
- ASF (Advanced Systems Format), Protokollierung
- Client Protokollierung
- Protokollieren von Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102630"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="51462-111">Client Protokollierung (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="51462-111">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="51462-112">Wenn das Reader-Objektdaten von einem Server liest, werden Protokollierungs Informationen an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="51462-112">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="51462-113">Inhaltsanbieter verwenden diese Informationen in der Regel, um die Dienst Qualität zu messen, Abrechnungsinformationen zu generieren oder Werbung zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="51462-113">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="51462-114">Die Protokollierungs Informationen enthalten keine personenbezogenen Daten.</span><span class="sxs-lookup"><span data-stu-id="51462-114">The logging information contains no personal data.</span></span>

<span data-ttu-id="51462-115">Die Anwendung kann einige der protokollierten Informationen angeben, indem Sie die [**iwmreaderadvanced:: setClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) -Methode für das Reader-Objekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="51462-115">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="51462-116">Sie können z. b. die Benutzer-Agent-Zeichenfolge, den Namen der Player Anwendung oder die Webseite angeben, die den Player hostet.</span><span class="sxs-lookup"><span data-stu-id="51462-116">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="51462-117">Die Protokollierungs Informationen beinhalten eine GUID, die die Sitzung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51462-117">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="51462-118">Standardmäßig generiert der Reader eine anonyme Sitzungs-ID.</span><span class="sxs-lookup"><span data-stu-id="51462-118">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="51462-119">Optional kann der Reader stattdessen eine ID senden, die den aktuellen Benutzer eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51462-119">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="51462-120">Um dieses Feature zu aktivieren, müssen Sie die [**IWMReaderAdvanced2:: setlogclientid-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) Methode mit dem Wert " **true**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="51462-120">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="51462-121">Sie können das Reader-Objekt so konfigurieren, dass die Protokollierungs Informationen zusätzlich zum ursprünglichen Server an einen anderen Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="51462-121">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="51462-122">Um dies zu tun, wenden Sie die Methode [**iwmreadernetworkconfig:: addloggingurl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) mit der URL des Servers an.</span><span class="sxs-lookup"><span data-stu-id="51462-122">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="51462-123">Diese URL sollte auf ein Skript oder eine ausführbare Datei verweisen, die HTTP-Get-und Post-Anforderungen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="51462-123">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="51462-124">Sie können den Multicast-und Protokollierungs Ankündigungs-Agent (wmsiislog.dll) verwenden, oder Sie können ein benutzerdefiniertes ASP-oder CGI-Skript schreiben, um die Protokolldaten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="51462-124">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="51462-125">Sie können dieselbe Funktionalität erzielen, indem Sie eine serverseitige Wiedergabeliste mit einem **LogURL** -Attribut erstellen.</span><span class="sxs-lookup"><span data-stu-id="51462-125">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="51462-126">Wenn das Reader-Objekt das Protokoll sendet, erfolgt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="51462-126">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="51462-127">Sendet eine leere Get-Anforderung an den Server.</span><span class="sxs-lookup"><span data-stu-id="51462-127">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="51462-128">Analysiert die Serverantwort für eine der folgenden Zeichen folgen:</span><span class="sxs-lookup"><span data-stu-id="51462-128">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="51462-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` Dabei ist "0.0.0.0" eine beliebige gültige Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="51462-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="51462-130">Sendet eine Post-Anforderung mit den Protokollinformationen.</span><span class="sxs-lookup"><span data-stu-id="51462-130">Sends a POST request with the log information.</span></span>

<span data-ttu-id="51462-131">Der folgende Code zeigt ein ASP-Beispielskript, mit dem die Protokollierungs Informationen empfangen und in eine Datei geschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="51462-131">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


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



<span data-ttu-id="51462-132">Sie können mehrere Server angeben, um Protokollierungs Informationen zu empfangen. nennen Sie **addloggingurl** nur einmal mit jeder URL.</span><span class="sxs-lookup"><span data-stu-id="51462-132">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="51462-133">Um die Liste der Server zu löschen, die Protokolle empfangen, müssen Sie die [**iwmreadernetworkconfig:: resetloggingurllist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="51462-133">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51462-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51462-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51462-135">**Implementieren von Netzwerkfunktionen**</span><span class="sxs-lookup"><span data-stu-id="51462-135">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="51462-136">**Iwmreaderadvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="51462-136">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="51462-137">**IWMReaderAdvanced2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="51462-137">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




