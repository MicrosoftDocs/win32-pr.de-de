---
description: Wenn der generische Host und der Client erfolgreich sind, aber der tatsächliche Host und Client weiterhin fehlschlagen, ist es möglich, dass die metadatenanforderung nicht initiiert wird. Die WinHTTP-Protokollierung kann verwendet werden, um zu überprüfen, ob ausgehende Nachrichten generiert und ordnungsgemäß gesendet werden.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Verwenden der WinHTTP-Protokollierung zum Überprüfen von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e4a127baf90a64291cbd14477c424270b332d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216160"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a><span data-ttu-id="bba05-104">Verwenden der WinHTTP-Protokollierung zum Überprüfen von Daten</span><span class="sxs-lookup"><span data-stu-id="bba05-104">Using WinHTTP Logging to Verify Get Traffic</span></span>

<span data-ttu-id="bba05-105">Wenn der generische Host und der Client erfolgreich sind, aber der tatsächliche Host und Client weiterhin fehlschlagen, ist es möglich, dass die metadatenanforderung nicht initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="bba05-105">If the generic host and client succeed but the actual host and client still fail, it is possible that the metadata request is not being initiated.</span></span> <span data-ttu-id="bba05-106">Die [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) -Protokollierung kann verwendet werden, um zu überprüfen, ob ausgehende Nachrichten generiert und ordnungsgemäß gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bba05-106">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging can be used to verify that outbound messages are being generated and sent correctly.</span></span>

<span data-ttu-id="bba05-107">WSDAPI-basierte Client Anwendungen verwenden [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) zum Herstellen einer Verbindung mit Geräten.</span><span class="sxs-lookup"><span data-stu-id="bba05-107">WSDAPI-based client applications use [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) to connect to devices.</span></span> <span data-ttu-id="bba05-108">Auf WSDAPI basierenden Geräte Hosts wird WinHTTP nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bba05-108">WSDAPI-based device hosts do not use WinHTTP.</span></span> <span data-ttu-id="bba05-109">Außerdem verwenden einige Proxys von Drittanbietern nicht WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="bba05-109">Also, some third-party proxies do not use WinHTTP.</span></span> <span data-ttu-id="bba05-110">Überspringen Sie bei der Problembehandlung eines Hosts oder Proxys, der nicht WinHTTP verwendet, dieses Diagnoseverfahren, und setzen Sie die Problembehandlung fort, indem Sie die Verfahren unter Überprüfen von Netzwerk Ablauf Verfolgungen [für http](inspecting-network-traces-for-http-metadata-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="bba05-110">When troubleshooting a host or proxy that does not use WinHTTP, skip this diagnostic procedure and continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="bba05-111">Die [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) -Protokollierung zeigt nicht den gesamten Datenverkehr auf TCP-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="bba05-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging does not show all TCP-level traffic.</span></span> <span data-ttu-id="bba05-112">Überprüfen Sie die Netzwerk Ablauf Verfolgungen [für den HTTP-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md) , wenn der Datenverkehr neben dem HTTP-Datenverkehr von Interesse ist</span><span class="sxs-lookup"><span data-stu-id="bba05-112">Skip to [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) if traffic besides the HTTP traffic is of interest.</span></span>

<span data-ttu-id="bba05-113">**So verwenden Sie die WinHTTP-Protokollierung, um den Datenverkehr**</span><span class="sxs-lookup"><span data-stu-id="bba05-113">**To use WinHTTP logging to verify Get traffic**</span></span>

1.  [<span data-ttu-id="bba05-114">Erfassen Sie die WinHTTP-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="bba05-114">Capture the WinHTTP logs.</span></span>](capturing-winhttp-logs.md)
2.  <span data-ttu-id="bba05-115">Starten Sie Notepad oder einen anderen Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="bba05-115">Start Notepad or another text editor.</span></span> <span data-ttu-id="bba05-116">Der Text-Editor muss als Administrator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bba05-116">The text editor must be run as Administrator.</span></span>
3.  <span data-ttu-id="bba05-117">Öffnen Sie die WinHTTP-Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="bba05-117">Open the WinHTTP log file.</span></span>
4.  <span data-ttu-id="bba05-118">Vergewissern Sie sich, dass die erforderlichen HTTP-Anforderungen und metadatennachrichten gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="bba05-118">Verify that the required HTTP requests and metadata messages were sent.</span></span>

<span data-ttu-id="bba05-119">Wenn eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht für den Host in den WinHTTP-Protokollen gefunden wird, werden die Metadatenanforderungen erfolgreich an WinHTTP gesendet.</span><span class="sxs-lookup"><span data-stu-id="bba05-119">If a [Get](get--metadata-exchange--http-request-and-message.md) message for the host is found in the WinHTTP logs, then the metadata requests are being sent to WinHTTP successfully.</span></span> <span data-ttu-id="bba05-120">Fahren Sie mit dem Verfahren unter Überprüfen von Netzwerk Ablauf Verfolgungen [für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)fort</span><span class="sxs-lookup"><span data-stu-id="bba05-120">Continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="bba05-121">Wenn eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht für den Host in den WinHTTP-Protokollen nicht gefunden werden kann, wird die metadatenanforderung nicht initiiert.</span><span class="sxs-lookup"><span data-stu-id="bba05-121">If a [Get](get--metadata-exchange--http-request-and-message.md) message cannot be found for the host in the WinHTTP logs, then the metadata request is not being initiated.</span></span> <span data-ttu-id="bba05-122">Dies kann vorkommen, wenn der Host ungültige xaddrs veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="bba05-122">This can happen when the host publishes invalid XAddrs.</span></span> <span data-ttu-id="bba05-123">Vergewissern Sie sich, dass die xaddrs auf dem Host den [xaddr-Validierungsregeln](xaddr-validation-rules.md)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bba05-123">Verify that the XAddrs on the host conform to the [XAddr validation rules](xaddr-validation-rules.md).</span></span>

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a><span data-ttu-id="bba05-124">Es wird überprüft, ob die erforderlichen HTTP-Anforderungen und metadatennachrichten gesendet wurden</span><span class="sxs-lookup"><span data-stu-id="bba05-124">Verifying that the required HTTP requests and metadata messages were sent</span></span>

<span data-ttu-id="bba05-125">Die folgenden Ereignisse müssen für einen erfolgreichen Metadatenaustausch auftreten:</span><span class="sxs-lookup"><span data-stu-id="bba05-125">The following events must occur for successful metadata exchange:</span></span>

-   <span data-ttu-id="bba05-126">Der WSDAPI-Client generiert eine ausgehende HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bba05-126">The WSDAPI client generates an outbound HTTP request.</span></span> <span data-ttu-id="bba05-127">Diese Anforderung wird an den WSDAPI-Host gesendet.</span><span class="sxs-lookup"><span data-stu-id="bba05-127">This request is sent to the WSDAPI host.</span></span>
-   <span data-ttu-id="bba05-128">Der Client sendet eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht an den Host.</span><span class="sxs-lookup"><span data-stu-id="bba05-128">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to the host.</span></span>

<span data-ttu-id="bba05-129">Diese Ereignisse werden in den WinHTTP-Protokollen aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bba05-129">These events are captured in the WinHTTP logs.</span></span>

<span data-ttu-id="bba05-130">Der folgende WinHTTP-Protokolldatei Ausschnitt zeigt eine ausgehende HTTP-Anforderung, die von einem WSDAPI-Client generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bba05-130">The following WinHTTP log file snippet shows an outbound HTTP request generated by a WSDAPI client.</span></span>

``` syntax
16:51:47.893 ::*0000004* :: WinHttpSendRequest(0x36aae0, "", 0, 0x0, 0, 658, 0)
16:51:47.893 ::*0000004* :: WinHttpSendRequest() returning TRUE
16:51:47.897 ::*0000004* :: sending data:
16:51:47.897 ::*0000004* :: 226 (0xe2) bytes
16:51:47.897 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.897 ::*0000004* :: POST /dbe17c74-3b21-4f52-addc-b84b444f73a0 HTTP/1.1
16:51:47.897 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.897 ::*0000004* :: User-Agent: WSDAPI
16:51:47.897 ::*0000004* :: Host: 192.168.0.1:5357
16:51:47.897 ::*0000004* :: Content-Length: 658
16:51:47.897 ::*0000004* :: Connection: Keep-Alive
16:51:47.897 ::*0000004* :: Cache-Control: no-cache
16:51:47.897 ::*0000004* :: Pragma: no-cache
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

<span data-ttu-id="bba05-131">Der folgende WinHTTP-Protokolldatei Ausschnitt zeigt eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bba05-131">The following WinHTTP log file snippet shows a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="bba05-132">Diese Nachricht sollte direkt auf die HTTP-Anforderung folgen.</span><span class="sxs-lookup"><span data-stu-id="bba05-132">This message should immediately follow the HTTP request.</span></span>

``` syntax
16:51:47.898 ::*0000004* :: WinHttpWriteData(0x36aae0, 0x11aa7c4, 658, 0x0)
16:51:47.899 ::*0000004* :: sending data:
16:51:47.899 ::*0000004* :: 658 (0x292) bytes
16:51:47.899 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.899 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"><soap:Header><wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action><wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID><wsa:ReplyTo><wsa:Address>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></wsa:ReplyTo><wsa:From><wsa:Address>urn:uuid:b32467b5-e7ee-4ae3-8a8e-f5aa417c23b6</wsa:Address></wsa:From></soap:Header><soap:Body></soap:Body></soap:Envelope>
16:51:47.899 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: WinHttpWriteData() returning TRUE
```

<span data-ttu-id="bba05-133">Das **Action** -Element ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifiziert die Nachricht als [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bba05-133">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) identifies the message as a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="bba05-134">Überprüfen Sie, ob der Wert des **to** -Elements (z. b. `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) mit der Geräte-ID übereinstimmt, die vom Host in den ursprünglichen UDP-WS-Discovery Meldungen angekündigt wurde.</span><span class="sxs-lookup"><span data-stu-id="bba05-134">Verify that the value of the **To** element (for example, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) matches the device ID advertised by the host in the original UDP WS-Discovery messages.</span></span> <span data-ttu-id="bba05-135">Die vom Host angekündigte Geräte-ID kann mithilfe des WSD-debughosts geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="bba05-135">The device ID advertised by the host can be checked by using the WSD Debug Host.</span></span> <span data-ttu-id="bba05-136">Weitere Informationen finden Sie unter [Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="bba05-136">For more information, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="bba05-137">Außerdem befindet sich die Antwort des Hosts auf die metadatenanforderung in den WinHTTP-Protokollen des Clients.</span><span class="sxs-lookup"><span data-stu-id="bba05-137">In addition, the host's response to the metadata request can be found in the client's WinHTTP logs.</span></span> <span data-ttu-id="bba05-138">Der Host generiert eine [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht als Antwort auf die [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht des Clients.</span><span class="sxs-lookup"><span data-stu-id="bba05-138">The host generates a [GetResponse](getresponse--metadata-exchange--message.md) message in response to the client's [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="bba05-139">Der folgende WinHTTP-Protokolldatei Ausschnitt zeigt eine eingehende [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht, die von einem WSDAPI-Client empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="bba05-139">The following WinHTTP log file snippet shows an inbound [GetResponse](getresponse--metadata-exchange--message.md) message received by a WSDAPI client.</span></span>

``` syntax
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse(0x36aae0, 0x0)
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse() returning TRUE
16:51:47.899 ::*Session* :: DllMain(0x73fc0000, DLL_THREAD_ATTACH, 0x0)
16:51:47.902 ::*0000004* :: received data:
16:51:47.902 ::*0000004* :: 1024 (0x400) bytes
16:51:47.902 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.902 ::*0000004* :: HTTP/1.1 200 
16:51:47.902 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.902 ::*0000004* :: Server: Microsoft-HTTPAPI/2.0
16:51:47.902 ::*0000004* :: Date: Fri, 15 Jun 2007 23:51:47 GMT
16:51:47.905 ::*0000004* :: Content-Length: 2228
16:51:47.905 ::*0000004* :: 
16:51:47.905 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.905 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof" xmlns:un0="http://schemas.microsoft.com/windows/pnpx/2005/10" xmlns:pub="http://schemas.microsoft.com/windows/pub/2005/07"><soap:Header><wsa:To>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action><wsa:MessageID>urn:uuid:2884cbcc-2848-4c35-9327-5ab5451a8729</wsa:MessageID><wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo></soap:Header><soap:Body><wsx:Metadata><wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice"><wsdp:ThisDevice><wsd
16:51:47.905 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

<span data-ttu-id="bba05-140">Das **Action** -Element ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifiziert die Nachricht als [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bba05-140">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) identifies the message as a [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span> <span data-ttu-id="bba05-141">Vergewissern Sie sich, dass der Wert des Elements **RelatesTo** der GetResponse-Nachricht mit dem Wert des **MessageId** -Elements der [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="bba05-141">Verify that the value of the **RelatesTo** element of the GetResponse message matches the value of the **MessageID** element of the [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="bba05-142">In diesem Beispiel entspricht der Wert des **RelatesTo** -Elements ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) dem Wert des **MessageId** -Elements der GET-Nachricht ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).</span><span class="sxs-lookup"><span data-stu-id="bba05-142">In this example, the value of the **RelatesTo** element (`<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>`) matches the value of the **MessageID** element of the Get message (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bba05-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bba05-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bba05-144">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="bba05-144">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="bba05-145">Erfassen von WinHTTP-Protokollen</span><span class="sxs-lookup"><span data-stu-id="bba05-145">Capturing WinHTTP Logs</span></span>](capturing-winhttp-logs.md)
</dt> <dt>

[<span data-ttu-id="bba05-146">WSDAPI-Diagnose Prozeduren</span><span class="sxs-lookup"><span data-stu-id="bba05-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="bba05-147">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="bba05-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
