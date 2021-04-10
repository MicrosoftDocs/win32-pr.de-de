---
description: Es gibt zwei Möglichkeiten, das zu verwendende Diagnoseverfahren zu bestimmen.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Ersten Schritte mit der WSDAPI-Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12396ea656423772d35dbd4ca237c7c536dcdaf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215431"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Ersten Schritte mit der WSDAPI-Problembehandlung

Dieses Handbuch zur Problembehandlung enthält eine Reihe von [Diagnose Prozeduren](wsdapi-diagnostic-procedures.md) , die verwendet werden können, um die Ursache von Anwendungsproblemen zu identifizieren. Wenn die Ursache des Problems erfolgreich identifiziert wurde, können die vorgeschlagenen Lösungen in der Diagnose Prozedur angewendet werden, um das Problem zu beheben.

Es gibt zwei Möglichkeiten, das zu verwendende Diagnoseverfahren zu bestimmen. Eine Möglichkeit besteht darin, auf der Seite zur Problembehandlung für den Clienttyp eine Schritt-für-Schritt-Liste der Diagnose Prozeduren anzuzeigen, die für die Problembehandlung des Clients verwendet werden sollen. Die andere Möglichkeit besteht darin, zur Problembehandlung der folgenden Kurzübersicht zu wechseln, um zusammenfassende Tabellen anzuzeigen, die häufige Probleme mit WSDAPI-Anwendungen sowie die Verfahren zum Diagnostizieren der Probleme anzeigen.

## <a name="troubleshooting-by-type-of-client"></a>Problembehandlung nach Clienttyp

In den folgenden Themen werden die relevanten Diagnose Prozeduren nach dem Typ des Clients erläutert. Diese Themen zeigen auch die Nachrichten Muster, die dem Clienttyp zugeordnet sind.

-   [Problembehandlung bei WSDAPI-Anwendungen mithilfe der gesteuerten Ermittlung](troubleshooting-applications-using-directed-discovery.md)
-   [Problembehandlung bei Funktions Ermittlungs Clients](troubleshooting-function-discovery-clients.md)
-   [Problembehandlung bei Personen in meiner Umgebung/Besprechungen](troubleshooting-people-near-me-meetings-near-me.md)
-   [Problembehandlung beim Hinzufügen von Drucker](troubleshooting-the-add-printer-wizard.md)
-   [Problembehandlung für den Netzwerk-Explorer](troubleshooting-the-network-explorer.md)
-   [Problembehandlung beim Projektor-Assistenten](troubleshooting-the-projector-wizard.md)
-   [Problembehandlung bei anderen WSDAPI-Anwendungen](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Kurzübersicht zur Problembehandlung

In den folgenden Tabellen sind einige Probleme aufgeführt, mit denen verhindert werden kann, dass WSDAPI-Clients und-Hosts einander im Netzwerk sehen und Geräte Metadaten austauschen können. Die Tabellen zeigen außerdem die auszulöserdiagnose Prozeduren und die Kriterien, anhand derer bewertet werden soll, ob die Anwendung von einem bestimmten Problem ausgeht.

### <a name="network-environment-problems"></a>Probleme mit der Netzwerkumgebung



| Problem                                                                                                                                                                                              | Diagnose Prozedur                                                                                                                                                                                                                             | Problem Identifikation                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Firewall blockiert den Datenverkehr der Netzwerk Ermittlung.                                                                                                                                                       | [Überprüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Wenn Sie die Netzwerk Ermittlungs Ausnahme auf der Firewall aktivieren, wird das Problem gelöst.                                                                                                                      |
| Firewallausnahmen, die für die Anwendung spezifisch sind, blockieren Nachrichten.                                                                                                                               | [Überprüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Durch das Deaktivieren der Firewall wird das Problem gelöst. WF. msc zeigt anwendungsspezifische Firewallregeln.                                                                                                      |
| Das Gerät antwortet nicht auf UDP-Anforderungen, indem er eine [Probe Matches](probematches-message.md) -oder [resolvematches](resolvematches-message.md) -Nachricht rechtzeitig (weniger als 4 Sekunden) sendet. | [Überprüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Durch das Deaktivieren der Firewall wird das Problem gelöst, und ein generischer Host, der in weniger als 4 Sekunden antwortet, funktioniert erfolgreich.                                                                            |
| Der Sicherheitskontext der Anwendung ist falsch (d. h., der Client und der Host verfügen nicht über die erforderlichen Berechtigungen für das Netzwerk).                                                                 | [Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) oder [Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md) | Die Geräteadresse wird in der WSD-debugclientausgabe nicht angezeigt. Wenn Sie die Anwendung als Administrator ausführen, wird das Problem gelöst.                                                                          |
| Eine IPSec-Richtlinie blockiert Nachrichten.                                                                                                                                                                | [Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) oder [Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md) | Die Geräteadresse wird in der WSD-debugclientausgabe nicht angezeigt. Das Problem wird nicht gelöst, indem die Firewall deaktiviert wird. Das Problem kann nicht auf einem Computer reproduziert werden, der keine IPSec-Richtlinien unterliegt. |



 

### <a name="discovery-traffic-problems"></a>Probleme beim Ermittlungs Datenverkehr



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problem</th>
<th>Diagnose Prozedur</th>
<th>Problem Identifikation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="hello-message.md">Hello</a>- <a href="probe-message.md">, Test</a>-oder <a href="resolve-message.md">Resolve</a> -Nachrichten werden nicht im Netzwerk übertragen, da die Multicast-Netzwerkschnittstellen von der Anwendung nicht ordnungsgemäß aufgelistet werden.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Überprüfen von Multicast Datenverkehr mithilfe des WSD-Debugclients</a></td>
<td>Die Meldungen Hello, Probe oder Resolve werden nicht in der WSD-debugclientausgabe angezeigt. Die Pakete werden nicht im Netzwerk angezeigt. Pakete werden nicht für die Loopback-Schnittstelle oder für andere Schnittstellen generiert.</td>
</tr>
<tr class="even">
<td>Test <a href="probe-message.md">Nachrichten werden</a> von UDP-Multicast nicht an Port 3702 gesendet (für Anwendungen, die keine gesteuerte Ermittlung verwenden).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a></td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass Sie an den falschen Port gesendet wurde.</td>
</tr>
<tr class="odd">
<td>Die <a href="probe-message.md">Testnachricht enthält</a> kein <strong>types</strong> -Element, oder das <strong>types</strong> -Element ist leer.</td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass das <strong>types</strong> -Element nicht vorhanden oder leer ist.</td>
</tr>
<tr class="even">
<td>Das <strong>types</strong> - <a href="probe-message.md">Element einer Testnachricht enthält</a> nicht die Typen, auf die ein Host antwortet.</td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass das <strong>types</strong> -Element einen falsch formatierten oder falschen Wert enthält.</td>
</tr>
<tr class="odd">
<td>Eine <a href="probematches-message.md">Probe Matches</a> -Nachricht wurde nicht an den UDP-Port gesendet, von dem aus der Test <a href="probe-message.md">gesendet wurde.</a></td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Bei der Überprüfung der Ausgabe wird angezeigt, dass keine <a href="probematches-message.md">Probe Matches</a>-Nachricht gesendet wurde oder dass die Nachricht an den falschen Port gesendet wurde.
<blockquote>
[!Note]<br />
Für Anwendungen, die die gesteuerte Ermittlung verwenden, müssen die <a href="probematches-message.md">Probe Matches</a> als Antwort auf die <a href="probe-message.md">Testnachricht über</a> http oder HTTPS gesendet werden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Die <a href="probematches-message.md">Probe Matches</a> -Nachricht enthält kein <strong>RelatesTo</strong> -Element, oder das <strong>RelatesTo</strong> -Element ist leer.</td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass das <strong>RelatesTo</strong> -Element nicht vorhanden oder leer ist.</td>
</tr>
<tr class="odd">
<td>Der Wert des <strong>RelatesTo</strong> -Elements in einer <a href="probematches-message.md">Probe Matches</a> -Nachricht stimmt nicht mit dem Wert des <strong>MessageId</strong> -Elements aus der <a href="probe-message.md">entsprechenden Test</a> Nachricht überein.</td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>RelatesTo</strong> -Element einen falsch formatierten oder falschen Wert enthält.</td>
</tr>
<tr class="even">
<td>Das <strong>xaddrs</strong> -Element, das in einer <a href="probematches-message.md">Probe Matches</a> -Nachricht enthalten ist, entspricht nicht den <a href="xaddr-validation-rules.md">xaddr-Validierungsregeln</a>.</td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass die <strong>xaddrs</strong> ungültig sind.</td>
</tr>
<tr class="odd">
<td>Das <a href="resolve-message.md">Auflösen</a> von Nachrichten wird nicht von UDP-Multicast an Port 3702 gesendet (für Anwendungen, die keine gesteuerte Ermittlung verwenden).</td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Die Überprüfung der Ausgabe zeigt, dass die <a href="resolve-message.md">Auflösungs</a> Meldung an den falschen Port gesendet wurde.</td>
</tr>
<tr class="even">
<td>Eine <a href="resolvematches-message.md">resolvematches</a> -Nachricht wurde nicht an den UDP-Port gesendet, von dem eine <a href="resolve-message.md">Resolve</a> -Nachricht gesendet wurde.</td>
<td>Überprüfen <a href="inspecting-network-traces-for-udp-ws-discovery.md">von Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery</a> oder <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen mithilfe der gesteuerten</a> Ermittlung</td>
<td>Bei der Überprüfung der Ausgabe wird angezeigt, dass keine <a href="resolvematches-message.md">resolvematches</a> -Nachricht gesendet wurde oder dass die Nachricht an den falschen Port gesendet wurde.</td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a>Probleme beim Austauschen von Metadaten



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problem</th>
<th>Diagnose Prozedur</th>
<th>Problem Identifikation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Die vom Host angekündigte Transport Adresse ist falsch.</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch</a></td>
<td>Bei der Überprüfung der xaddrs in der WSD-debugclientausgabe wird angezeigt, dass die Transport Adresse falsch oder fehlerhaft ist.</td>
</tr>
<tr class="even">
<td>Für den Metadatenaustausch konnte keine TCP-Verbindung hergestellt werden.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Die Ausgabe der Paket Analyse zeigt nicht den folgenden Paket Austausch:
<ul>
<li>Ein vom Client gesendeter TCP-SYN-Paket.</li>
<li>Ein vom Host gesendeter TCP-SYN/ACK-Paket.</li>
<li>Ein vom Client gesendeter TCP-ACK-Paket.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Der Client hat keine gültige HTTP GET-Anforderung gesendet.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Es gibt keine HTTP GET-Anforderung in der Paket Analyse Ausgabe, oder die Anforderung ist falsch formatiert.</td>
</tr>
<tr class="even">
<td>Der Client hat keine gültige WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> -Nachricht gesendet.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Es gibt keine WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> -Nachricht in der Paket Analyse Ausgabe, oder die Nachricht ist falsch formatiert.</td>
</tr>
<tr class="odd">
<td>Der Host lauscht nicht an dem URL-Pfad, der in der HTTP GET-Anforderung angegeben ist.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>In der Paket Analyse Ausgabe ist keine HTTP-Antwort vorhanden.</td>
</tr>
<tr class="even">
<td>Die WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> -Nachricht enthält kein <strong>to</strong> -Element, oder das <strong>to</strong> -Element ist leer.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass das <strong>to</strong> -Element nicht vorhanden oder leer ist.</td>
</tr>
<tr class="odd">
<td>Der Wert des <strong>to</strong> -Elements einer WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> -Nachricht stimmt nicht mit einer der Endpunkt Adressen des Hosts.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass der Wert des <strong>to</strong> -Elements nicht mit einer der Endpunkt Adressen übereinstimmt, die in der <a href="probematches-message.md">probematches</a> -oder <a href="resolvematches-message.md">resolvematches</a> -Nachricht des Hosts angekündigt werden.</td>
</tr>
<tr class="even">
<td>Der Host hat keinen gültigen HTTP-Antwortheader gesendet.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Es gibt keine HTTP-Antwort in der Paket Analyse Ausgabe, oder die Anforderung ist falsch formatiert.</td>
</tr>
<tr class="odd">
<td>Der vom Host gesendete HTTP-Antwortheader gibt an, dass die Anforderung nicht abgeschlossen werden kann.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Der Antwortheader weist einen anderen Statuscode als HTTP/1.1 200 auf.</td>
</tr>
<tr class="even">
<td>Der Host hat keine gültige <a href="getresponse--metadata-exchange--message.md">GetResponse</a> -Nachricht gesendet.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Die Paket Analyse-Ausgabe enthält keine <a href="getresponse--metadata-exchange--message.md">GetResponse</a> -Nachricht, oder die Nachricht ist falsch formatiert.</td>
</tr>
<tr class="odd">
<td>Die <a href="getresponse--metadata-exchange--message.md">GetResponse</a> -Nachricht enthält kein <strong>RelatesTo</strong> -Element, oder das <strong>RelatesTo</strong> -Element ist leer.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Bei der Überprüfung der Meldung wird angezeigt, dass das <strong>RelatesTo</strong> -Element nicht vorhanden oder leer ist.</td>
</tr>
<tr class="even">
<td>Der Wert des <strong>RelatesTo</strong> -Elements in einer <a href="getresponse--metadata-exchange--message.md">GetResponse</a> -Nachricht stimmt nicht mit dem Wert des <strong>MessageId</strong> -Elements aus der entsprechenden <a href="get--metadata-exchange--http-request-and-message.md">Get</a> -Nachricht überein.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>RelatesTo</strong> -Element einen falsch formatierten oder falschen Wert enthält.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Handbuch zur Problembehandlung](wsdapi-troubleshooting-guide.md)
</dt> </dl>
