---
title: Implementieren des Teredo-Sicherheitsmodells
description: Das Teredo-Sicherheitsmodell basiert auf der Windows-Filter Plattform (WFP)-Technologie, die in Windows Vista integriert ist. Daher wird empfohlen, dass Firewalls von Drittanbietern WFP verwenden, um das Teredo-Sicherheitsmodell zu erzwingen.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a39668f8e1c86e0cd5b12056df5eb9a5fd9cd3ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729049"
---
# <a name="implementing-the-teredo-security-model"></a>Implementieren des Teredo-Sicherheitsmodells

Das Teredo-Sicherheitsmodell basiert auf der [Windows-Filter Plattform](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP)-Technologie, die in Windows Vista integriert ist. Daher wird empfohlen, dass Firewalls von Drittanbietern WFP verwenden, um das [Teredo](about-teredo.md) -Sicherheitsmodell zu erzwingen.

Die allgemeine Implementierung des [Teredo-Sicherheitsmodells](the-teredo-security-model.md) erfordert Folgendes:

-   Eine IPv6-fähige Host Firewall muss bei Windows Security Center (WSC) auf dem Computer registriert werden. Wenn keine Host basierte Firewall oder WSC selbst vorhanden ist, kann die Teredo-Schnittstelle nicht verwendet werden. Dies ist die einzige Anforderung, um angeforderten Datenverkehr aus dem Internet über die Teredo-Schnittstelle zu empfangen.
-   Jede Anwendung, die nicht angeforderten Datenverkehr aus dem Internet über die Teredo-Schnittstelle empfängt, muss sich bei einer IPv6-fähigen Firewall wie der [Windows-Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page)registrieren, bevor der angeforderte Datenverkehr empfangen wird.

Eine Teredo-Adresse wird inaktiv, wenn der Datenverkehr für eine Stunde nicht über die Teredo-Schnittstelle gesendet oder empfangen wurde, und wenn Anwendungen, die die erforderlichen Sicherheitskriterien für nicht angeforderten Datenverkehr erfüllen, nicht ausgeführt werden oder keine Abhör Sockets geöffnet sind.

Nach dem Neustart eines Computers oder wenn die Teredo-Adresse seine Qualifikationen verliert, wird die Adresse automatisch von Windows Vista qualifiziert und zur Verwendung verfügbar, sobald eine Anwendung an IPv6-fähige Sockets gebunden ist. Beachten Sie, dass die Option "Edge Traversal" der Windows-Firewall, die von einer Anwendung festgelegt wird, um nicht angeforderten Datenverkehr über Teredo zuzulassen, über Neustarts hinweg persistent ist.

## <a name="firewall-requirements-for-teredo"></a>Firewallanforderungen für Teredo

Firewallhersteller können mithilfe der Funktionen der Windows-Filter Plattform problemlos Teredo-Unterstützung in Ihre Produkte integrieren und Ihre Benutzer schützen. Dies kann erreicht werden, indem die IPv6-fähige Firewall mit dem Windows-Security Center registriert wird, der WFP-Unterebene "Teredo" geeignete Regeln hinzugefügt werden und in Windows integrierte APIs zum Auflisten von Anwendungen verwendet werden, die möglicherweise auf nicht angeforderten Datenverkehr über Teredo lauschen. In Situationen, in denen eine Anwendung nicht auf den angeforderten Datenverkehr über Teredo lauschen muss, benötigen Firewalls keine zusätzlichen Regeln, die dem WFP hinzugefügt werden. Eine IPv6-fähige Firewall-Registrierung bei Windows Security Center ist jedoch weiterhin erforderlich, damit die Teredo-Adresse zur Verwendung verfügbar ist.

Um dieses Szenario zu unterstützen, muss die Firewall IPv6-fähig sein und beim Windows-Security Center registriert sein. Außerdem darf die Firewall nicht den Status "wird ausgeführt" oder "Start" des Windows Security Center-Dienstanbieter (wscsvc) ändern, da Teredo von den Zustandsinformationen abhängig ist, die über die WSC-APIs bereitgestellt werden.

Die API, die zum Registrieren einer Firewall bei WSC verwendet wird, kann durch kontaktieren von Microsoft unter abgerufen werden wscisv@microsoft.com . Für das Offenlegen dieser API ist aufgrund von Sicherheitsbedenken eine Vereinbarung zur nicht Offenlegung (NDA) erforderlich.

In der folgenden Dokumentation werden die Filter und Ausnahmen erläutert, die verwendet werden, um eine optimale Kompatibilität mit Teredo sicherzustellen

-   [Implementieren von Firewallfiltern für Teredo](implementing-firewall-filters-for-teredo.md)
-   [Erforderliche Firewallausnahmen für Teredo](required-firewall-exceptions-for-teredo.md)
-   [Erforderliche Ausnahmen für die Windows-Filter Plattform für Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Firewallanforderungen für andere IPv6-Übergangs Technologien

Um andere IPv6-Übergangs Technologien (z. b. IPv6-zu-IPv4 und ISATAP) zu unterstützen, muss das hostfirewallprodukt in der Lage sein, IPv6-Datenverkehr zu verarbeiten. Das IP-Protokoll 41 zeigt an, wenn ein IPv6-Header einem IPv4-Header folgt. Wenn eine Host Firewall auf das Protokoll 41 stößt, muss Sie erkennen, dass das Paket ein IPv6-gekapseltes Paket ist. Daher muss das Paket entsprechend verarbeitet werden, und die Annahme/Ablehnung der Entscheidungen auf Grundlage der IPv6-Regeln in der Richtlinie wird gewährleisten.

 

 