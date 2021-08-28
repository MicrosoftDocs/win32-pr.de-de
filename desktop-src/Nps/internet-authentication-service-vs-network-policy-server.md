---
title: Internetauthentifizierungsdienst & Netzwerkrichtlinienserver
description: Erfahren Sie mehr über den Internetauthentifizierungsdienst und den Netzwerkrichtlinienserver. Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt.
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36751c66b525749afce0d5546f61fa35c1cbb856
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483046"
---
# <a name="internet-authentication-service--network-policy-server"></a>Internetauthentifizierungsdienst & Netzwerkrichtlinienserver

Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt.

## <a name="internet-authentication-service"></a>Internetauthentifizierungsdienst

Der Internetauthentifizierungsdienst ist die Microsoft-Implementierung eines RADIUS-Servers und -Proxys.

Der Internetauthentifizierungsdienst unterstützt zwei API-Sätze: Die Api für [Netzwerkrichtlinienservererweiterungen](ias-extensions.md) und [die Serverdatenobjekt-API.](server-data-objects.md)

Weitere Informationen zu IAS finden Sie unter [TechNet: Internet Authentication Service.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))

## <a name="network-policy-server"></a>Netzwerkrichtlinienserver

Netzwerkrichtlinienserver ist die Microsoft-Implementierung eines RADIUS-Servers und -Proxys und ab Windows Server 2008 auf Windows Servern verfügbar.

NPS unterstützt die gleichen beiden API-Sätze wie IAS: [Network Policy Server Extensions API](ias-extensions.md) und Server Data Objects [API](server-data-objects.md).

Darüber hinaus enthält NPS eine Reihe neuer Features, die die IAS-Funktionen erweitern.




| Funktion | Neuerungen bei NPS | 
|---------|--------------------|
| <a href="/windows/desktop/NAP/network-access-protection-start-page">Netzwerkzugriffsschutz (NAP)</a><br /> | NPS ist der zentrale Server des Netzwerkzugriffsschutzes.<br /> NPS unterstützt die Richtlinienerstellung mit den folgenden zusätzlichen Bedingungen:<br /><ul><li>Ablauf der Richtlinie.</li><li>Betriebssystemversion.</li><li>Zugreifen auf die Client-IP-Adresse.</li><li>Integritätsrichtlinien.</li><li>Zulässige EAP-Typen.</li><li>HCAP.</li></ul>NPS unterstützt die Richtlinienerstellung mit den folgenden zusätzlichen Einstellungen:<br /><ul><li>Bewährung.</li><li>Eingeschränkter Zugriff.</li><li>Erweiterter Zustand für eingeschränkten Zugriff.</li></ul>NPS interoperiert über NAP mit CISCO NAC.<br /> NAP wird von IAS nicht unterstützt.<br /> | 
| <a href="/windows/win32/eap/eap-start-page">EAP</a> Richtlinien- und <a href="/windows/win32/eaphost/portal">EAPHost-Unterstützung</a><br /> | NPS verwendet EAPHost für die Erweiterbarkeit von EAP-Methoden. Darüber hinaus können Administratoren die Netzwerkzugriffsrichtlinie für EAP konfigurieren.<br /> IAS unterstützt keine EAPHost-Integration oder EAP-Typfilterbedingungen für Richtlinien.<br /> | 
| IPv6-Unterstützung<br /> | NPS unterstützt die Bereitstellung in IPv6-Umgebungen.<br /> IAS unterstützt keine IPv6-Netzwerkadressen.<br /> | 
| XML-Konfiguration<br /> | Die NPS-Konfiguration kann im XML-Format importiert und exportiert werden.<br /> IAS verwendet eine Jet-Datenbank zum Speichern der Dienstkonfiguration.<br /> | 
| <a href="https://www.niap-ccevs.org/cc-scheme/">Allgemeine Kriterien</a> Unterstützung<br /> | NPS wurde aktualisiert, um die Bereitstellung in Umgebungen zu unterstützen, die die Common Criteria-Sicherheitsstandards erfüllen müssen.<br /> | 
| <a href="ias-extensions.md">NPS-Erweiterungs-API</a><br /> | Die NPS-Erweiterungs-DLLs werden in einem separaten Prozess vom NPS-Dienst ausgeführt. Wenn eine Erweiterungs-DLL abstürzt, wird NPS weiterhin ausgeführt, und zukünftige Anforderungen werden abgelehnt.<br /> Die DLLs der IAS-Erweiterung werden im gleichen Prozess wie der IAS-Dienst ausgeführt und können sich negativ auf den Dienst auswirken.<br /> | 
| Verwaltungs-Benutzeroberfläche<br /> | Die NPS-Verwaltungskonsole (nps.msc) verfügt über ein neues Aussehen, verbesserte Benutzerfreundlichkeit und deckt alle neuen Funktionen ab, die NPS hinzugefügt wurden.<br /> IAS verwendet die Verwaltungskonsole "ias.msc".<br /> | 
| Rollenverwaltungstool und Server-Manager Integration<br /> | NPS ist in die Server-Manager und das Rollenverwaltungstool integriert. Diese Integration erleichtert die Konfiguration und Verwaltung von NPS und zugehörigen Szenarien.<br /> Server-Manager ist auf Computern mit IAS nicht verfügbar.<br /> | 
| Befehlszeilenskripterstellung mit <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>aktualisiert.<br /> | NPS unterstützt die Befehlszeilenschnittstelle "Netsh nps". "Netsh nps" enthält neue Befehle, die die vollständige Konfiguration von NPS ermöglichen, einschließlich NAP-Features.<br /> IAS unterstützt die Befehlszeilenschnittstelle "Netsh aaaa".<br /> | 
| Richtlinienisolation<br /> | NPS ermöglicht die Implementierung der Richtlinienisolation, indem die Netzwerkrichtlinienquelle festgelegt wird. Richtlinien können konfiguriert werden, die nur für einen vordefinierten NAS-Typ gelten.<br /> IAS unterstützt keine Richtlinienisolation.<br /> | 




 

Weitere Informationen zu NPS finden Sie unter [TechNet: Netzwerkrichtlinienserver.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[RADIUS-Authentifizierung, -Autorisierung und -Buchhaltung](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Protokollierung mit Netzwerkrichtlinienserver](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Arbeiten mit einem Zustandsserver](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

