---
description: Eine WS-Discovery Nachricht, die von einem Client verwendet wird, um nach Diensten im Netzwerk nach Diensttyp zu suchen.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Testmeldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f186de4f68faceca096ddaa231b57d1112bc1e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879844"
---
# <a name="probe-message"></a>Testmeldung

Eine Testnachricht ist eine WS-Discovery Nachricht, die von einem Client verwendet wird, um nach Diensten im Netzwerk nach Diensttyp zu suchen. Weitere Informationen zu Testmeldungen finden Sie in Abschnitt 5.2 der [WS-Discovery-Spezifikation.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Eine Testnachricht wird von UDP Multicast an Port 3702 gesendet. Unicasttestnachrichten werden nicht unterstützt.

DPWS-Clients senden Testnachrichten. Die folgende Liste zeigt Szenarien, in denen WSDAPI eine Testnachricht sendet.

-   Funktionsermittlungsclients senden Testnachrichten.
-   WSDAPI-Clients, die [**IWSDiscoveryProvider::SearchByAddress aufrufen,**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) senden Testnachrichten.
-   WSDAPI-Clients, die [**IWSDiscoveryProvider::SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) aufrufen, senden Testnachrichten.
-   Anwendungen, die die gerichtete Ermittlung verwenden, senden Testnachrichten über HTTP oder HTTPS.

> [!Note]  
> In diesem Thema wird eine DPWS-Beispielnachricht gezeigt, die von WSDAPI-Clients und -Hosts generiert wird. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die diesem Beispiel nicht entsprechen. Verwenden Sie dieses Beispiel nicht, um die DPWS-Interoperabilität zu überprüfen. Verwenden Sie stattdessen das [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Die folgende SOAP-Nachricht zeigt eine Beispieltestmeldung.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Probe>
        <wsd:Types>wsdp:Device</wsd:Types>
    </wsd:Probe>
</soap:Body>
```

Eine Testmeldung weist die folgenden Fokuspunkte auf.



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
<td>Test</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
&lt;/wsa:Action&gt;</code></pre></td>
<td>Die SOAP-Aktion Probe identifiziert die Nachricht als Testnachricht.</td>
</tr>
<tr class="even">
<td>Meldungs-ID</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:MessageID&gt;
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
&lt;/wsa:MessageID&gt;</code></pre></td>
<td>Enthält den Nachrichtenbezeichner, auf den das RelatesTo-Element in einer <a href="probematches-message.md">ProbeMatches-Nachricht</a> verweist.</td>
</tr>
<tr class="odd">
<td>Typen</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:Types&gt;wsdp:Device</wsd:Types></code></pre></td>
<td>Enthält die WS-Discovery Typen, nach denen der Client sucht. Dieses Element darf nicht leer sein.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs- und Metadaten-Exchange-Meldungen](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[ProbeMatches-Nachricht](probematches-message.md)
</dt> </dl>

 

 



