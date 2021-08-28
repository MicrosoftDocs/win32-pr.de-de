---
description: Eine WS-Discovery Meldung, die von einem Client verwendet wird, um anhand des Namens nach Diensten im Netzwerk zu suchen.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Auflösen einer Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed3ab1778fada267a72207309eb8cb515727d5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627766"
---
# <a name="resolve-message"></a>Auflösen einer Nachricht

Eine Resolve-Nachricht ist eine WS-Discovery Nachricht, die von einem Client verwendet wird, um anhand des Namens nach Diensten im Netzwerk zu suchen. Ein Client sendet nur dann eine Resolve-Nachricht, wenn eine HTTP-Nachricht (z. B. [eine](get--metadata-exchange--http-request-and-message.md) Get Metadata Exchange-Anforderung oder eine Dienstnachricht) gesendet wird. Weitere Informationen zum Auflösen von Nachrichten finden Sie in Abschnitt 6.1 der [WS-Ermittlungsspezifikation.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Eine Resolve-Nachricht wird von UDP Multicast an Port 3702 gesendet. Unicast-Auflösungsmeldungen werden nicht unterstützt.

DPWS-Clients senden Resolve-Nachrichten. Die folgende Liste zeigt Szenarien, in denen WSDAPI eine Resolve-Nachricht sendet.

-   Ein Funktionsermittlungsclient sendet eine Resolve-Nachricht, wenn keine XAddrs in einer [ProbeMatches-Nachricht](probematches-message.md) enthalten sind.
-   Ein Client, der die [**IWSDiscoveryProvider::SearchById-Methoden**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) aufruft, sendet eine Resolve-Nachricht.
-   Ein Client, der [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) aufruft, sendet möglicherweise eine Resolve-Nachricht, wenn eine logische Geräteadresse an *pszDeviceId* übergeben wird.
-   Ein Client, der [**WSDCreateDeviceProxyAdvanced aufruft,**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) sendet eine Resolve-Nachricht, wenn die Funktion mit dem pDeviceAddress-Parameter aufgerufen wird, der auf **NULL** festgelegt ist.

> [!Note]  
> In diesem Thema wird eine DPWS-Beispielnachricht gezeigt, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die diesem Beispiel nicht entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie stattdessen das [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Die folgende SOAP-Nachricht zeigt eine Beispielmeldung zum Auflösen.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

Eine Resolve-Nachricht weist die folgenden Fokuspunkte auf.



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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Beheben</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>Die Aktion SOAP auflösen identifiziert die Nachricht als Resolve-Nachricht.</td>
</tr>
<tr class="even">
<td>Meldungs-ID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Enthält den Nachrichtenbezeichner, auf den in einer <a href="resolvematches-message.md">ResolveMatches-Nachricht</a> verwiesen wird.</td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Adresse des Endpunkts, der aufgelöst wird.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange-Meldungen](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[ResolveMatches-Nachricht](resolvematches-message.md)
</dt> </dl>

 

 



