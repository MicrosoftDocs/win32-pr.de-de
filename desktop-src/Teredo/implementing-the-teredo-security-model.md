---
title: Implementieren des Teredo-Sicherheitsmodells
description: Das Teredo-Sicherheitsmodell basiert auf der in Windows Vista integrierten WFP-Technologie (Windows Filtering Platform). Daher wird empfohlen, dass Firewalls von Drittanbietern WFP verwenden, um das Teredo-Sicherheitsmodell zu erzwingen.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cad78b7c1512e0f1c632ecd27d0bb9580ac3796d6d36001a1cd19fb72c7b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001748"
---
# <a name="implementing-the-teredo-security-model"></a>Implementieren des Teredo-Sicherheitsmodells

Das Teredo-Sicherheitsmodell basiert auf der in Windows Vista [integrierten WFP-Technologie (Windows Filtering Platform).](/windows/desktop/FWP/windows-filtering-platform-start-page) Daher wird empfohlen, dass Firewalls von Drittanbietern WFP verwenden, um das [Teredo-Sicherheitsmodell](about-teredo.md) zu erzwingen.

Die allgemeine Implementierung des [Teredo-Sicherheitsmodells](the-teredo-security-model.md) erfordert Folgendes:

-   Eine IPv6-fähige Hostfirewall muss bei Windows-Sicherheit Center (WSC) auf dem Computer registriert werden. Wenn keine hostbasierte Firewall oder WSC selbst vorhanden ist, ist die Teredo-Schnittstelle nicht für die Verwendung verfügbar. Dies ist die einzige Anforderung, um angeforderten Datenverkehr aus dem Internet über die Teredo-Schnittstelle zu empfangen.
-   Jede Anwendung, die nicht angeforderten Datenverkehr aus dem Internet über die Teredo-Schnittstelle empfängt, muss sich bei einer IPv6-fähigen Firewall wie [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page)registrieren, bevor der nicht angeforderte Datenverkehr empfangen wird.

Eine Teredo-Adresse wird ruhend, wenn der Datenverkehr eine Stunde lang nicht über die Teredo-Schnittstelle gesendet oder empfangen wurde und Anwendungen, die die erforderlichen Sicherheitskriterien für nicht angeforderten Datenverkehr erfüllen, nicht ausgeführt werden oder keine Lauschsockets geöffnet sind.

Nach dem Neustart eines Computers oder wenn die Teredo-Adresse ihre Qualifikationen verliert, qualifiziert Windows Vista die Adresse automatisch und macht sie zur Verwendung verfügbar, sobald eine Anwendung an IPv6-fähige Sockets gebunden wird. Es ist wichtig zu beachten, dass die von einer Anwendung festgelegte Option "Edgedurchlauf" der Windows Firewall, um nicht angeforderten Datenverkehr über Teredo zuzulassen, bei Neustarts persistent ist.

## <a name="firewall-requirements-for-teredo"></a>Firewallanforderungen für Teredo

Firewallanbieter können teredo-Unterstützung problemlos in ihre Produkte integrieren und ihre Benutzer mithilfe der Funktionen der Windows Filterplattform schützen. Dies kann erreicht werden, indem die IPv6-fähige Firewall beim Windows-Sicherheit Center registriert wird, der WFP-Teredo-Unterschicht entsprechende Regeln hinzugefügt und integrierte APIs in Windows verwendet werden, um Anwendungen aufzuzählen, die möglicherweise auf unerwünschten Datenverkehr über Teredo lauschen. In Situationen, in denen eine Anwendung nicht auf angeforderten Datenverkehr über Teredo lauschen muss, erfordern Firewalls keine zusätzlichen Regeln, die dem WFP hinzugefügt werden. Eine IPv6-fähige Firewallregistrierung bei Windows-Sicherheit Center ist jedoch weiterhin eine Anforderung, um die Teredo-Adresse für die Verwendung verfügbar zu machen.

Um dieses Szenario zu unterstützen, muss die Firewall IPv6-fähig sein und beim Windows-Sicherheit Center registriert sein. Darüber hinaus darf die Firewall den Ausführungs- oder Startstatus des Windows-Sicherheit Center-Diensts (wscsvc) nicht ändern, da Teredo von den Zustandsinformationen abhängig ist, die über die WSC-APIs bereitgestellt werden.

Die API, die zum Registrieren einer Firewall beim WSC verwendet wird, können Sie erhalten, indem Sie sich unter an Microsoft wscisv@microsoft.com wenden. Für die Offenlegung dieser API ist aus Sicherheitsgründen eine Vertraulichkeitsvereinbarung (Non-Disclosure Agreement, NDA) erforderlich.

In der folgenden Dokumentation werden die Filter und Ausnahmen ausführlich beschrieben, die verwendet werden, um eine optimale Kompatibilität mit Teredo sicherzustellen:

-   [Implementieren von Firewallfiltern für Teredo](implementing-firewall-filters-for-teredo.md)
-   [Erforderliche Firewall-Ausnahmen für Teredo](required-firewall-exceptions-for-teredo.md)
-   [Erforderliche Windows Filtern von Plattform ausnahmen für Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Firewallanforderungen für andere IPv6-Übergangstechnologien

Um andere IPv6-Übergangstechnologien (z. B. 6to4 und ISATAP) zu unterstützen, muss das Produkt der Hostfirewall IPv6-Datenverkehr verarbeiten können. Das IP-Protokoll 41 gibt an, wenn ein IPv6-Header einem IPv4-Header folgt. Wenn eine Hostfirewall auf Protokoll 41 trifft, muss sie erkennen, dass es sich bei dem Paket um ein IPv6-gekapseltes Paket handelt. Daher muss das Paket entsprechend verarbeitet werden und die Annahme-/Verweigerungsentscheidungen basierend auf den IPv6-Regeln in der Richtlinie getroffen werden.

 

 