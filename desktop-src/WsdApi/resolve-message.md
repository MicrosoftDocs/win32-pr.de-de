---
description: Eine WS-Discovery Nachricht, die von einem Client verwendet wird, um nach dem Namen nach Diensten im Netzwerk zu suchen.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Meldung auflösen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355632"
---
# <a name="resolve-message"></a>Meldung auflösen

Eine Auflösungs Meldung ist eine WS-Discovery Nachricht, die von einem Client verwendet wird, um nach dem Namen nach Diensten im Netzwerk zu suchen. Ein Client sendet nur dann eine Auflösungs Nachricht, wenn eine HTTP-Nachricht (z. b. eine [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Anforderung oder eine Dienst Nachricht) gesendet wird. Weitere Informationen zum Auflösen von Nachrichten finden Sie im Abschnitt 6,1 der [WS-Discovery-Spezifikation](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Eine Auflösungs Meldung wird von UDP-Multicast an Port 3702 gesendet. Unicast-Auflösungs Nachrichten werden nicht unterstützt.

DPWS-Clients senden Auflösungs Nachrichten. In der folgenden Liste sind Szenarien aufgeführt, in denen WSDAPI eine Resolve-Nachricht sendet.

-   Ein Funktions Ermittlungs Client sendet eine Resolve-Nachricht, wenn keine xaddrs in eine [Probe Matches](probematches-message.md) -Nachricht eingeschlossen werden.
-   Ein Client, der die [**iwsdiscoveryprovider:: searchbyid**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) -Methode aufrufen, sendet eine Resolve-Nachricht.
-   Ein Client, der [**wsdcreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) anruft, kann eine Auflösungs Nachricht senden, wenn eine logische Geräteadresse an *pszdeviceid* übergeben wird.
-   Ein Client, der [**wsdcreatedeviceproxyadvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) aufruft, sendet eine Resolve-Nachricht, wenn die Funktion mit dem pdeviceaddress-Parameter auf **null** festgelegt wird.

> [!Note]  
> Dieses Thema zeigt eine DPWS-Beispiel Nachricht, die von WSDAPI-Clients und-Hosts generiert wurde. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die nicht diesem Beispiel entsprechen. Verwenden Sie dieses Beispiel nicht zum Überprüfen der DPWS-Interoperabilität. Verwenden Sie stattdessen das [WSDAPI-grundlegende Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Die folgende SOAP-Nachricht zeigt eine Beispiel Auflösungs Meldung an.

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

Eine Resolve-Nachricht weist die folgenden Schwerpunkt Punkte auf.



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
<td>Beheben</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>Die Aktion SOAP auflösen identifiziert die Nachricht als Auflösungs Nachricht.</td>
</tr>
<tr class="even">
<td>Meldungs-ID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Enthält die Nachrichten-ID, auf die in einer <a href="resolvematches-message.md">resolvematches</a> -Meldung verwiesen wird.</td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Enthält die Adresse des zu lösenden Endpunkts.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs-und metadatenaustauschnachrichten](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Resolvematches-Nachricht](resolvematches-message.md)
</dt> </dl>

 

 



