---
description: Eine WS-Transfer Meldung, die zum Anfordern von Metadaten verwendet wird.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: Get-HTTP-Anforderung und -Nachricht (Metadata Exchange)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e02b990dc87cf8551e215bc7eae94dbcf7852
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632068"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>Get-HTTP-Anforderung und -Nachricht (Metadata Exchange)

Eine Get-Nachricht ist eine WS-Transfer Nachricht, die zum Anfordern von Metadaten verwendet wird. Weitere Informationen zum Abrufen von Nachrichten finden Sie in Abschnitt 3.1 der [WS-Transfer-Spezifikation.](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) Da der Metadatenaustausch über HTTP erfolgt, ist eine Get-Nachricht die Nutzlast einer HTTP-Anforderung.

DPWS-Clients senden Get-Nachrichten. Funktionsermittlungsclients, WSDAPI-Clients, die [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)aufrufen, und WSDAPI-Clients, die [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) aufrufen, senden diese Nachricht.

> [!Note]  
> In diesem Thema wird eine DPWS-Beispielnachricht gezeigt, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die diesem Beispiel nicht entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie stattdessen das [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Das folgende Beispiel zeigt eine Get HTTP-Anforderung.

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

Eine GET-HTTP-Anforderung verfügt über die folgenden Fokuspunkte.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Fokuspunkt</th>
<th>Kopfzeile</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>URL-Pfad</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>Der URL-Pfad, unter dem die GET-HTTP-Anforderung gesendet wurde.</td>
</tr>
<tr class="even">
<td>Host und Port</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>Der Host und Port, an den die GET-HTTP-Anforderung weitergeleitet wurde.</td>
</tr>
</tbody>
</table>



 

Die folgende SOAP-Nachricht zeigt eine Get-Beispielnachricht.

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

Eine Get-Nachricht hat die folgenden Fokuspunkte.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Der Bezeichner des Geräts, das nach Metadaten gefragt wird.</td>
</tr>
<tr class="even">
<td>Herunterladen</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>Die Aktion SOAP abrufen identifiziert die Nachricht als Get-Nachricht.</td>
</tr>
<tr class="odd">
<td>Meldungs-ID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Enthält den Nachrichtenbezeichner, auf den in einer <a href="getresponse--metadata-exchange--message.md">GetResponse-Nachricht</a> verwiesen wird.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange-Meldungen](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[GetResponse-Nachricht](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



