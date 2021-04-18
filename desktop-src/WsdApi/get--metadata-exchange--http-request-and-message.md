---
description: Eine WS-Transfer Meldung, die zum Anfordern von Metadaten verwendet wird.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: Get-http-Anforderung und-Nachricht (Metadatenaustausch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ad240a51fdbabf4184b8769f4e3cca6daa4244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343815"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>Get-http-Anforderung und-Nachricht (Metadatenaustausch)

Eine GET-Nachricht ist eine WS-Transfer Nachricht, die zum Anfordern von Metadaten verwendet wird. Weitere Informationen zu Get-Nachrichten finden Sie im Abschnitt 3,1 der [WS-Transfer-Spezifikation](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf). Da der Metadatenaustausch über HTTP erfolgt, ist eine GET-Nachricht die Nutzlast einer HTTP-Anforderung.

DPWS-Clients senden Get-Nachrichten. Funktions Ermittlungs Clients, WSDAPI-Clients, die [**wsdcreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)aufrufen, und WSDAPI-Clients, die [**wsdcreatedeviceproxyadvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) aufrufen, senden diese Nachricht.

> [!Note]  
> Dieses Thema zeigt eine DPWS-Beispiel Nachricht, die von WSDAPI-Clients und-Hosts generiert wurde. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die nicht diesem Beispiel entsprechen. Verwenden Sie dieses Beispiel nicht zum Überprüfen der DPWS-Interoperabilität. Verwenden Sie stattdessen das [WSDAPI-grundlegende Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Das folgende Beispiel zeigt eine HTTP-Beispiel Anforderung.

``` syntax
POST /37f86d35-e6ac-4241-964f-1d9ae46fb366
HTTP/1.1
Content-Type: application/soap+xml
User-Agent: WSDAPI
Host: 192.168.0.2:5357
Content-Length: 658
Connection: Keep-Alive
Cache-Control: no-cache
Pragma: no-cache
```

Eine get http-Anforderung weist die folgenden Schwerpunkt Punkte auf.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Fokuspunkt</th>
<th>Kopfzeile</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>URL-Pfad</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>Der URL-Pfad, an den die HTTP-Anforderung Get gesendet wurde.</td>
</tr>
<tr class="even">
<td>Host und Port</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>Der Host und der Port, an den die HTTP-Anforderung Get weitergeleitet wurde.</td>
</tr>
</tbody>
</table>



 

Die folgende SOAP-Nachricht zeigt eine Beispiel Nachricht für das Get-Beispiel.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing">
<soap:Header>
    <wsa:To>
        urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:MessageID>
    <wsa:ReplyTo>
        <wsa:Address>
            https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        </wsa:Address>
    </wsa:ReplyTo>
    <wsa:From>
        <wsa:Address>
            urn:uuid:49e131df-351a-4ece-9a6f-6a862d31cffa
        </wsa:Address>
    </wsa:From>
</soap:Header>
<soap:Body>
</soap:Body>
```

Eine GET-Nachricht weist die folgenden Schwerpunkt Punkte auf.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Fokuspunkt</th>
<th>XML</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>An</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:To>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:To></code></pre></td>
<td>Der Bezeichner des Geräts, das nach Metadaten angefordert wird.</td>
</tr>
<tr class="even">
<td>Herunterladen</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>Mit der Get SOAP-Aktion wird die Nachricht als GET-Nachricht identifiziert.</td>
</tr>
<tr class="odd">
<td>Meldungs-ID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Enthält den Nachrichten Bezeichner, auf den in einer <a href="getresponse--metadata-exchange--message.md">GetResponse</a> -Meldung verwiesen wird.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs-und metadatenaustauschnachrichten](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[GetResponse-Nachricht](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



