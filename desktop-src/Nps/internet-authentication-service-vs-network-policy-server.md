---
title: Internet Authentifizierungsdienst & Netzwerk Richtlinien Server
description: Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104039757"
---
# <a name="internet-authentication-service--network-policy-server"></a>Internet Authentifizierungsdienst & Netzwerk Richtlinien Server

Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS).

## <a name="internet-authentication-service"></a>Internetauthentifizierungsdienst

Der Internet Authentifizierungsdienst ist die Microsoft-Implementierung eines RADIUS-Servers und-Proxys.

Der Internet Authentifizierungsdienst unterstützt zwei API-Sätze: API- [Erweiterungen für Netzwerk Richtlinien Server](ias-extensions.md) und [Server Data Objects-API](server-data-objects.md).

Weitere Informationen zu IAS finden Sie unter [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .

## <a name="network-policy-server"></a>Netzwerkrichtlinienserver

Der Netzwerk Richtlinien Server ist die Microsoft-Implementierung eines RADIUS-Servers und-Proxys und ist ab Windows Server 2008 auf Windows-Servern verfügbar.

NPS unterstützt die gleichen zwei API-Sätze wie die IAS: API für [Netzwerk Richtlinien Server-Erweiterungen](ias-extensions.md) und [Server Data Objects-API](server-data-objects.md).

Außerdem enthält NPS eine Reihe neuer Features, mit denen die IAS-Funktionen erweitert werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Neues für NPS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/NAP/network-access-protection-start-page">Netzwerk Zugriffsschutz (Network Access Protection, NAP)</a><br/></td>
<td>NPS ist der zentrale Server für den Netzwerk Zugriffsschutz.<br/> NPS unterstützt das Erstellen von Richtlinien unter Verwendung der folgenden zusätzlichen Bedingungen:<br/>
<ul>
<li>Ablauf der Richtlinie.</li>
<li>Betriebssystemversion.</li>
<li>Zugriffs Client-IP-Adresse.</li>
<li>Integritäts Richtlinien</li>
<li>Zulässige EAP-Typen.</li>
<li>HCAP.</li>
</ul>
NPS unterstützt die Richtlinien Erstellung mithilfe der folgenden zusätzlichen Einstellungen:<br/>
<ul>
<li>Mend.</li>
<li>Eingeschränkter Zugriff.</li>
<li>Erweiterter Status für eingeschränkten Zugriff.</li>
</ul>
NPS über NAP interagiert mit Cisco NAC.<br/> IAS unterstützt NAP nicht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/eap/eap-start-page">EAP</a> Unterstützung von Richtlinien und <a href="/windows/win32/eaphost/portal">EAPHost</a><br/></td>
<td>NPS verwendet EAPHost für die Erweiterbarkeit von EAP-Methoden. Darüber hinaus können Administratoren die Netzwerk Zugriffs Richtlinie für EAP konfigurieren.<br/> IAS unterstützt keine EAPHost-Integration oder EAP-Typfilter Bedingungen für Richtlinien.<br/></td>
</tr>
<tr class="odd">
<td>IPv6-Unterstützung<br/></td>
<td>NPS unterstützt die Bereitstellung in IPv6-Umgebungen.<br/> IAS unterstützt keine IPv6-Netzwerkadressen.<br/></td>
</tr>
<tr class="even">
<td>XML-Konfiguration<br/></td>
<td>Die NPS-Konfiguration kann im XML-Format importiert und exportiert werden.<br/> IAS verwendet eine Jet-Datenbank zum Speichern der Dienst Konfiguration.<br/></td>
</tr>
<tr class="odd">
<td><a href="https://www.niap-ccevs.org/cc-scheme/">Allgemeine Kriterien</a> Förder<br/></td>
<td>NPS wurde aktualisiert, um die Bereitstellung in Umgebungen zu unterstützen, die die Common Criteria-Sicherheitsstandards erfüllen müssen.<br/></td>
</tr>
<tr class="even">
<td><a href="ias-extensions.md">NPS-Erweiterungs-API</a><br/></td>
<td>Die NPS-Erweiterungs-DLLs werden in einem separaten Prozess als der NPS-Dienst ausgeführt. Wenn eine Erweiterungs-DLL abstürzen soll, wird NPS weiterhin ausgeführt, und zukünftige Anforderungen werden abgelehnt.<br/> Die IAS-Erweiterungs-DLLs werden in demselben Prozess wie der IAS-Dienst ausgeführt und können sich negativ auf den Dienst auswirken.<br/></td>
</tr>
<tr class="odd">
<td>Verwaltungs Benutzeroberfläche<br/></td>
<td>Die NPS-Verwaltungskonsole (NPS. msc) verfügt über ein neues Erscheinungsbild, eine verbesserte Benutzerfreundlichkeit und deckt alle neuen Funktionen ab, die NPS hinzugefügt werden.<br/> IAS verwendet die IAS. msc-Verwaltungskonsole.<br/></td>
</tr>
<tr class="even">
<td>Rollen Verwaltungs Tool und Server-Manager Integration<br/></td>
<td>NPS ist in die Server-Manager und das Rollen Verwaltungs Tool integriert. Durch diese Integration wird die Konfiguration und Verwaltung von NPS und verwandten Szenarien vereinfacht.<br/> Server-Manager ist auf Computern, auf denen IAS ausgeführt wird, nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>Aktualisierte Befehlszeilen Skripts mit <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.<br/></td>
<td>NPS unterstützt die &quot; netsh NPS- &quot; Befehlszeilenschnittstelle. &quot;Netsh NPS &quot; enthält neue Befehle, mit denen NPS vollständig konfiguriert werden kann, einschließlich NAP-Features.<br/> IAS unterstützt die &quot; Netsh AAAA- &quot; Befehlszeilenschnittstelle.<br/></td>
</tr>
<tr class="even">
<td>Richtlinien Isolation<br/></td>
<td>NPS ermöglicht die Implementierung der Richtlinien Isolation durch Festlegen der Netzwerk Richtlinien Quelle. Richtlinien können so konfiguriert werden, dass Sie nur auf einen vordefinierten NAS-Typ anwendbar sind.<br/> IAS unterstützt keine Richtlinien Isolation.<br/></td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu NPS finden Sie unter [TechNet: Netzwerk Richtlinien Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[RADIUS-Authentifizierung,-Autorisierung und-Kontoführung](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Protokollierung mit dem Netzwerk Richtlinien Server](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Arbeiten mit einem Zustands Server](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

