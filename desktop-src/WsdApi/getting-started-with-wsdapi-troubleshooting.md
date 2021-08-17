---
description: Es gibt zwei Möglichkeiten, die zu verwendende Diagnoseprozedur zu bestimmen.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Erste Schritte mit WSDAPI – Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 413146288e6c7fc6e513f994fbe24d6ee9940897f22bcd5a715ae41f77f83c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738616"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Erste Schritte mit WSDAPI – Problembehandlung

Dieser Leitfaden zur Problembehandlung enthält eine Reihe von [Diagnoseverfahren,](wsdapi-diagnostic-procedures.md) die verwendet werden können, um die Ursache von Anwendungsproblemen zu identifizieren. Nachdem die Ursache des Problems erfolgreich identifiziert wurde, können die vorgeschlagenen Lösungen im Diagnoseverfahren angewendet werden, um das Problem zu beheben.

Es gibt zwei Möglichkeiten, die zu verwendende Diagnoseprozedur zu bestimmen. Eine Möglichkeit besteht im Wechseln zur Problembehandlungsseite für den Clienttyp, um eine schritt-für-Schritt-Liste der Diagnoseverfahren anzuzeigen, die für die Problembehandlung des Clients verwendet werden. Die andere Möglichkeit besteht in der folgenden Kurzübersicht zur Problembehandlung, um Zusammenfassungstabellen mit häufigen Problemen mit WSDAPI-Anwendungen und den Verfahren zur Diagnose der Probleme zu sehen.

## <a name="troubleshooting-by-type-of-client"></a>Problembehandlung nach Clienttyp

In den folgenden Themen werden die relevanten Diagnoseverfahren nach Clienttyp gezeigt. In diesen Themen werden auch die Nachrichtenmuster gezeigt, die dem Clienttyp zugeordnet sind.

-   [Problembehandlung bei WSDAPI-Anwendungen mithilfe der gerichteten Ermittlung](troubleshooting-applications-using-directed-discovery.md)
-   [Problembehandlung bei Funktionsermittlungsclients](troubleshooting-function-discovery-clients.md)
-   [Problembehandlung Personen in meiner Umgebung/Besprechungen in meiner Nähe](troubleshooting-people-near-me-meetings-near-me.md)
-   [Problembehandlung beim Assistenten zum Hinzufügen von Druckern](troubleshooting-the-add-printer-wizard.md)
-   [Problembehandlung für den Netzwerk-Explorer](troubleshooting-the-network-explorer.md)
-   [Problembehandlung beim Projektor-Assistenten](troubleshooting-the-projector-wizard.md)
-   [Problembehandlung für andere WSDAPI-Anwendungen](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Kurzreferenz zur Problembehandlung

Die folgenden Tabellen zeigen einige Probleme, die verhindern können, dass WSDAPI-Clients und -Hosts sich im Netzwerk gegenseitig sehen und Gerätemetadaten austauschen. Die Tabellen zeigen auch die durchzuführenden Diagnoseverfahren und die Kriterien, anhand derer ausgewertet werden kann, ob die Anwendung ein bestimmtes Problem auft.

### <a name="network-environment-problems"></a>Probleme mit der Netzwerkumgebung



| Problem                                                                                                                                                                                              | Diagnoseprozedur                                                                                                                                                                                                                             | Problemidentifikation                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Firewall blockiert den Netzwerkermittlungs-Datenverkehr.                                                                                                                                                       | [Überprüfen von Adapter- und Firewall-Einstellungen](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Das Aktivieren der Netzwerkermittlungsausnahme in der Firewall löst das Problem.                                                                                                                      |
| Firewallausnahmen, die für die Anwendung spezifisch sind, blockieren Nachrichten.                                                                                                                               | [Überprüfen von Adapter- und Firewall-Einstellungen](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Das Deaktivieren der Firewall löst das Problem. WF.msc zeigt anwendungsspezifische Firewallregeln an.                                                                                                      |
| Das Gerät reagiert nicht rechtzeitig auf UDP-Anforderungen, indem es eine [ProbeMatches-](probematches-message.md) oder [ResolveMatches-Nachricht](resolvematches-message.md) sendet (weniger als 4 Sekunden). | [Überprüfen von Adapter- und Firewall-Einstellungen](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | Das Deaktivieren der Firewall löst das Problem, und ein generischer Host, der in weniger als 4 Sekunden antwortet, funktioniert erfolgreich.                                                                            |
| Der Sicherheitskontext der Anwendung ist falsch (d. h., der Client und der Host verfügen nicht über die erforderlichen Berechtigungen für das Netzwerk).                                                                 | [Verwenden eines generischen Hosts und Clients für die UDP-WS-Ermittlung](using-a-generic-host-and-client-for-udp-ws-discovery.md) oder verwenden eines generischen Hosts und Clients [für HTTP-Metadaten Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | Die Geräteadresse wird in der Ausgabe des WSD-Debugclients nicht angezeigt. Wenn Sie die Anwendung als Administrator ausführen, wird das Problem gelöst.                                                                          |
| Eine IPSec-Richtlinie blockiert Nachrichten.                                                                                                                                                                | [Verwenden eines generischen Hosts und Clients für die UDP-WS-Ermittlung](using-a-generic-host-and-client-for-udp-ws-discovery.md) oder verwenden eines generischen Hosts und Clients [für HTTP-Metadaten Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | Die Geräteadresse wird in der Ausgabe des WSD-Debugclients nicht angezeigt. Das Problem wird nicht gelöst, indem die Firewall deaktiviert wird. Das Problem kann nicht auf einem Computer reproduziert werden, der keinen IPSec-Richtlinien unterliegt. |



 

### <a name="discovery-traffic-problems"></a>Ermittlung von Datenverkehrsproblemen



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problem</th>
<th>Diagnoseprozedur</th>
<th>Problemidentifikation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="hello-message.md">Hello-,</a> <a href="probe-message.md">Test-</a>oder <a href="resolve-message.md">Resolve-Nachrichten</a> werden nicht im Netzwerk übertragen, da die Anwendung die Multicastnetzwerkschnittstellen nicht ordnungsgemäß aufzählt.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Verwenden des WSD-Debugclients zum Überprüfen des Multicastdatenverkehrs</a></td>
<td>Die Meldungen Hello, Probe oder Resolve werden in der Ausgabe des WSD-Debugclients nicht angezeigt. Die Pakete werden nicht im Netzwerk angezeigt. Pakete werden nicht für die Loopbackschnittstelle oder für andere Schnittstellen generiert.</td>
</tr>
<tr class="even">
<td><a href="probe-message.md">Testnachrichten</a> werden nicht von UDP-Multicast an Port 3702 gesendet (für Anwendungen, die keine gerichtete Ermittlung verwenden).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Überprüfen von Netzwerkverfolgungen für die UDP-WS-Ermittlung</a></td>
<td>Die Überprüfung der Nachricht zeigt, dass sie an den falschen Port gesendet wurde.</td>
</tr>
<tr class="odd">
<td>Die <a href="probe-message.md">Testmeldung</a> enthält kein <strong>Types-Element,</strong> oder das <strong>Types-Element</strong> ist leer.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>Types-Element</strong> nicht vorhanden oder leer ist.</td>
</tr>
<tr class="even">
<td>Das <strong>Types-Element</strong> einer <a href="probe-message.md">Testmeldung</a> enthält nicht die Typen, auf die ein Host antwortet.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>Types-Element</strong> einen falsch formatierten oder falschen Wert enthält.</td>
</tr>
<tr class="odd">
<td>Eine <a href="probematches-message.md">ProbeMatches-Nachricht</a> wurde nicht an den UDP-Port gesendet, von dem der <a href="probe-message.md">Test</a> gesendet wurde.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Ausgabe zeigt, dass keine <a href="probematches-message.md">ProbeMatches</a>-Nachricht gesendet wurde oder dass die Nachricht an den falschen Port gesendet wurde.
<blockquote>
[!Note]<br />
Bei Anwendungen, die die gerichtete Ermittlung verwenden, müssen <a href="probematches-message.md">die ProbeMatches</a> als Antwort auf die Testnachricht über HTTP oder HTTPS <a href="probe-message.md">gesendet</a> werden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Die <a href="probematches-message.md">ProbeMatches-Nachricht</a> enthält kein <strong>RelatesTo-Element,</strong> oder das <strong>RelatesTo-Element</strong> ist leer.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>RelatesTo-Element</strong> nicht vorhanden oder leer ist.</td>
</tr>
<tr class="odd">
<td>Der Wert des <strong>RelatesTo-Elements</strong> in einer <a href="probematches-message.md">ProbeMatches-Nachricht</a> entspricht nicht dem Wert des <strong>MessageId-Elements</strong> aus der entsprechenden <a href="probe-message.md">Testnachricht.</a></td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>RelatesTo-Element</strong> einen falsch formatierten oder falschen Wert enthält.</td>
</tr>
<tr class="even">
<td>Das in einer <a href="probematches-message.md">ProbeMatches-Nachricht</a> enthaltene <strong>XAddrs-Element</strong> entspricht nicht den <a href="xaddr-validation-rules.md">XAddr-Validierungsregeln.</a></td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Meldung zeigt, dass <strong>die XAddrs</strong> ungültig sind.</td>
</tr>
<tr class="odd">
<td><a href="resolve-message.md">Auflösungsmeldungen</a> werden nicht von UDP-Multicast an Port 3702 gesendet (für Anwendungen, die keine gerichtete Ermittlung verwenden).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Ausgabe zeigt, dass die <a href="resolve-message.md">Auflösungsmeldung</a> an den falschen Port gesendet wurde.</td>
</tr>
<tr class="even">
<td>Eine <a href="resolvematches-message.md">ResolveMatches-Nachricht</a> wurde nicht an den UDP-Port gesendet, von dem eine <a href="resolve-message.md">Resolve-Nachricht</a> gesendet wurde.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Untersuchen von Netzwerkverfolgungen für die UDP-WS-Ermittlung oder</a> Überprüfen <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung</a></td>
<td>Die Überprüfung der Ausgabe zeigt, dass keine <a href="resolvematches-message.md">ResolveMatches-Nachricht</a> gesendet wurde oder dass die Nachricht an den falschen Port gesendet wurde.</td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a>Probleme beim Metadatenaustausch



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problem</th>
<th>Diagnoseprozedur</th>
<th>Problemidentifikation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Die vom Host angekündigte Transportadresse ist falsch.</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Verwenden eines generischen Hosts und Clients für HTTP-Exchange</a></td>
<td>Die Überprüfung der XAddrs in der Ausgabe des WSD-Debugclients zeigt, dass die Transportadresse falsch oder falsch formatiert ist.</td>
</tr>
<tr class="even">
<td>Für den Metadatenaustausch konnte keine TCP-Verbindung hergestellt werden.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Die Ausgabe der Paketanalyse zeigt nicht den folgenden Paketaustausch:
<ul>
<li>Ein vom Client gesendetes TCP SYN-Paket</li>
<li>Ein vom Host gesendetes TCP SYN/ACK-Paket</li>
<li>Ein vom Client gesendetes TCP-ACK-Paket</li>
</ul></td>
</tr>
<tr class="odd">
<td>Der Client hat keine gültige HTTP GET-Anforderung gesendet.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>In der Ausgabe des Paketanalyse-Pakets ist keine HTTP GET-Anforderung enthalten, oder die Anforderung ist falsch formatiert.</td>
</tr>
<tr class="even">
<td>Der Client hat keine gültige GetWS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">gesendet.</a></td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>In der Ausgabe WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Paketanalyse</a> ist keine Get-Nachricht enthalten, oder die Nachricht ist falsch formatiert.</td>
</tr>
<tr class="odd">
<td>Der Host lausst nicht auf den URL-Pfad, der in der HTTP GET-Anforderung angegeben ist.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Es gibt keine HTTP-Antwort in der Paketanalyseausgabe.</td>
</tr>
<tr class="even">
<td>Die WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get-Nachricht</a> enthält kein <strong>To-Element,</strong> oder das <strong>To-Element</strong> ist leer.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>To-Element</strong> nicht vorhanden oder leer ist.</td>
</tr>
<tr class="odd">
<td>Der Wert des <strong>To-Elements</strong> einer WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get-Nachricht</a> nicht mit einer der Endpunktadressen des Hosts.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Die Überprüfung der Nachricht zeigt, dass der Wert des To-Elements nicht mit einer der Endpunktadressen übereinstimmen, die in der <a href="probematches-message.md">ProbeMatches-</a> oder <a href="resolvematches-message.md">ResolveMatches-Nachricht</a> des Hosts angekündigt werden. <strong></strong></td>
</tr>
<tr class="even">
<td>Der Host hat keinen gültigen HTTP-Antwortheader gesendet.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Es gibt keine HTTP-Antwort in der Paketanalyseausgabe, oder die Anforderung ist falsch formatiert.</td>
</tr>
<tr class="odd">
<td>Der vom Host gesendete HTTP-Antwortheader gibt an, dass die Anforderung nicht abgeschlossen werden kann.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Der Antwortheader verfügt über einen anderen Statuscode als HTTP/1.1 200.</td>
</tr>
<tr class="even">
<td>Der Host hat keine gültige <a href="getresponse--metadata-exchange--message.md">GetResponse-Nachricht</a> gesendet.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Die Ausgabe <a href="getresponse--metadata-exchange--message.md">des Paketanalysediensts enthält keine GetResponse-Nachricht,</a> oder die Nachricht ist falsch formatiert.</td>
</tr>
<tr class="odd">
<td>Die <a href="getresponse--metadata-exchange--message.md">GetResponse-Nachricht</a> enthält kein <strong>RelatesTo-Element,</strong> oder das <strong>RelatesTo-Element</strong> ist leer.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>RelatesTo-Element</strong> nicht vorhanden oder leer ist.</td>
</tr>
<tr class="even">
<td>Der Wert des <strong>RelatesTo-Elements</strong> in einer <a href="getresponse--metadata-exchange--message.md">GetResponse-Nachricht</a> entspricht nicht dem Wert des <strong>MessageId-Elements</strong> aus der entsprechenden <a href="get--metadata-exchange--http-request-and-message.md">Get-Nachricht.</a></td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange</a></td>
<td>Die Überprüfung der Meldung zeigt, dass das <strong>RelatesTo-Element</strong> einen falsch formatierten oder falschen Wert enthält.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Handbuch zur WSDAPI-Problembehandlung](wsdapi-troubleshooting-guide.md)
</dt> </dl>
