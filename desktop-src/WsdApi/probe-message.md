---
description: Eine WS-Discovery Nachricht, die von einem Client für die Suche nach Diensten im Netzwerk nach Diensttyp verwendet wird.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Testnachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913c163be8d82297a642b1a97a7d28e0c403ca08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131136"
---
# <a name="probe-message"></a>Testnachricht

Eine Testnachricht ist eine WS-Discovery Nachricht, die von einem Client für die Suche nach Diensten im Netzwerk nach Diensttyp verwendet wird. Weitere Informationen zu Testnachrichten finden Sie im Abschnitt 5,2 der [WS-Discovery-Spezifikation](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Eine Testnachricht wird von UDP-Multicast an Port 3702 gesendet. Unicasttestnachrichten werden nicht unterstützt.

DPWS-Clients senden Testnachrichten. In der folgenden Liste werden Szenarien angezeigt, in denen WSDAPI eine Testnachricht sendet.

-   Funktions Ermittlungs Clients senden Testnachrichten.
-   WSDAPI-Clients, die [**iwsdiscoveryprovider:: searchbyaddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) aufrufen, senden Testnachrichten.
-   WSDAPI-Clients, die [**iwsdiscoveryprovider:: searchbytype**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) aufrufen, senden Testnachrichten.
-   Anwendungen, die die gesteuerte Ermittlung verwenden, senden Testnachrichten über HTTP oder HTTPS.

> [!Note]  
> Dieses Thema zeigt eine DPWS-Beispiel Nachricht, die von WSDAPI-Clients und-Hosts generiert wurde. WSDAPI analysiert und akzeptiert andere DPWS-kompatible Nachrichten, die nicht diesem Beispiel entsprechen. Verwenden Sie dieses Beispiel nicht zum Überprüfen der DPWS-Interoperabilität. Verwenden Sie stattdessen das [WSDAPI-grundlegende Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Die folgende SOAP-Nachricht zeigt eine Beispiel Testnachricht an.

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

Eine Testnachricht weist die folgenden Schwerpunkt Punkte auf.



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
<td>Test</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
</wsa:Action></code></pre></td>
<td>Die Aktion SOAP testen identifiziert die Nachricht als Testnachricht.</td>
</tr>
<tr class="even">
<td>Meldungs-ID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:MessageID></code></pre></td>
<td>Enthält die Nachrichten-ID, auf die vom RelatesTo-Element in einer <a href="probematches-message.md">Probe Matches</a> -Meldung verwiesen wird.</td>
</tr>
<tr class="odd">
<td>Typen</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Enthält die WS-Discovery Typen, für die der Client sucht. Dieses Element darf nicht leer sein.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermittlungs-und metadatenaustauschnachrichten](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Probe Matches-Meldung](probematches-message.md)
</dt> </dl>

 

 



