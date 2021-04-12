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
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>Verwenden der WinHTTP-Protokollierung zum Überprüfen von Daten

Wenn der generische Host und der Client erfolgreich sind, aber der tatsächliche Host und Client weiterhin fehlschlagen, ist es möglich, dass die metadatenanforderung nicht initiiert wird. Die [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) -Protokollierung kann verwendet werden, um zu überprüfen, ob ausgehende Nachrichten generiert und ordnungsgemäß gesendet werden.

WSDAPI-basierte Client Anwendungen verwenden [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) zum Herstellen einer Verbindung mit Geräten. Auf WSDAPI basierenden Geräte Hosts wird WinHTTP nicht verwendet. Außerdem verwenden einige Proxys von Drittanbietern nicht WinHTTP. Überspringen Sie bei der Problembehandlung eines Hosts oder Proxys, der nicht WinHTTP verwendet, dieses Diagnoseverfahren, und setzen Sie die Problembehandlung fort, indem Sie die Verfahren unter Überprüfen von Netzwerk Ablauf Verfolgungen [für http](inspecting-network-traces-for-http-metadata-exchange.md)

Die [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) -Protokollierung zeigt nicht den gesamten Datenverkehr auf TCP-Ebene an. Überprüfen Sie die Netzwerk Ablauf Verfolgungen [für den HTTP-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md) , wenn der Datenverkehr neben dem HTTP-Datenverkehr von Interesse ist

**So verwenden Sie die WinHTTP-Protokollierung, um den Datenverkehr**

1.  [Erfassen Sie die WinHTTP-Protokolle.](capturing-winhttp-logs.md)
2.  Starten Sie Notepad oder einen anderen Text-Editor. Der Text-Editor muss als Administrator ausgeführt werden.
3.  Öffnen Sie die WinHTTP-Protokolldatei.
4.  Vergewissern Sie sich, dass die erforderlichen HTTP-Anforderungen und metadatennachrichten gesendet wurden.

Wenn eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht für den Host in den WinHTTP-Protokollen gefunden wird, werden die Metadatenanforderungen erfolgreich an WinHTTP gesendet. Fahren Sie mit dem Verfahren unter Überprüfen von Netzwerk Ablauf Verfolgungen [für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)fort

Wenn eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht für den Host in den WinHTTP-Protokollen nicht gefunden werden kann, wird die metadatenanforderung nicht initiiert. Dies kann vorkommen, wenn der Host ungültige xaddrs veröffentlicht. Vergewissern Sie sich, dass die xaddrs auf dem Host den [xaddr-Validierungsregeln](xaddr-validation-rules.md)entsprechen.

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>Es wird überprüft, ob die erforderlichen HTTP-Anforderungen und metadatennachrichten gesendet wurden

Die folgenden Ereignisse müssen für einen erfolgreichen Metadatenaustausch auftreten:

-   Der WSDAPI-Client generiert eine ausgehende HTTP-Anforderung. Diese Anforderung wird an den WSDAPI-Host gesendet.
-   Der Client sendet eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht an den Host.

Diese Ereignisse werden in den WinHTTP-Protokollen aufgezeichnet.

Der folgende WinHTTP-Protokolldatei Ausschnitt zeigt eine ausgehende HTTP-Anforderung, die von einem WSDAPI-Client generiert wurde.

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

Der folgende WinHTTP-Protokolldatei Ausschnitt zeigt eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht. Diese Nachricht sollte direkt auf die HTTP-Anforderung folgen.

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

Das **Action** -Element ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifiziert die Nachricht als [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht. Überprüfen Sie, ob der Wert des **to** -Elements (z. b. `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) mit der Geräte-ID übereinstimmt, die vom Host in den ursprünglichen UDP-WS-Discovery Meldungen angekündigt wurde. Die vom Host angekündigte Geräte-ID kann mithilfe des WSD-debughosts geprüft werden. Weitere Informationen finden Sie unter [Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Außerdem befindet sich die Antwort des Hosts auf die metadatenanforderung in den WinHTTP-Protokollen des Clients. Der Host generiert eine [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht als Antwort auf die [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht des Clients.

Der folgende WinHTTP-Protokolldatei Ausschnitt zeigt eine eingehende [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht, die von einem WSDAPI-Client empfangen wurde.

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

Das **Action** -Element ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifiziert die Nachricht als [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht. Vergewissern Sie sich, dass der Wert des Elements **RelatesTo** der GetResponse-Nachricht mit dem Wert des **MessageId** -Elements der [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht übereinstimmt. In diesem Beispiel entspricht der Wert des **RelatesTo** -Elements ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) dem Wert des **MessageId** -Elements der GET-Nachricht ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Erfassen von WinHTTP-Protokollen](capturing-winhttp-logs.md)
</dt> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
