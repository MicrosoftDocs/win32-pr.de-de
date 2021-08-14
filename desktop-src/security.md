---
description: Entwickeln Sie sicherere Desktop-Apps mit Windows APIs und Diensten.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Sicherheit und Identität
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ff19c113340af314177b821bfd8294036d752d90218a5255eb6a429e9b6312ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226335"
---
# <a name="security-and-identity"></a>Sicherheit und Identität

Entwickeln Sie sicherere Desktop-Apps mit Windows APIs und Diensten. Diese APIs bieten:

- Authentifizierung
- Authorization
- Kryptografie
- Verzeichnis-, Identitäts- und Zugriffsdienste
- Jugendschutz
- Rights Management

Dieser Abschnitt enthält auch bewährte Methoden und andere Sicherheitsartikel.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
| ----- | ----------- |
| [Antischadsoftware-Scanschnittstelle](./amsi/antimalware-scan-interface-portal.md) | Die Antimalware Scan Interface (AMSI) ist ein generischer Schnittstellenstandard, mit dem Anwendungen und Dienste in jedes Antischadsoftwareprodukt integriert werden können, das auf einem Computer vorhanden ist. Es bietet einen verbesserten Schutz vor Schadsoftware für Benutzer und ihre Daten, Anwendungen und Workloads. |
| [Authentifizierung](./secauthn/authentication-portal.md) | Die Authentifizierung ist der Prozess, mit dem das System die Anmeldeinformationen eines Benutzers überprüft. Der Name und das Kennwort eines Benutzers werden mit einer autorisierten Liste verglichen. Wenn das System eine Übereinstimmung erkennt, wird der Zugriff in dem Umfang gewährt, der in der Berechtigungsliste für diesen Benutzer angegeben ist. |
| [Autorisierung](./secauthz/authorization-portal.md) | Autorisierung ist das Recht, das einer Person erteilt wird, das System und die darauf gespeicherten Daten zu verwenden. Die Autorisierung wird in der Regel von einem Systemadministrator eingerichtet und vom Computer anhand einer Form der Benutzeridentifikation überprüft, z. B. einer Codenummer oder eines Kennworts. |
| [Bewährte Methoden für die Sicherheits-APIs](./secbp/best-practices-for-the-security-apis.md) | Enthält bewährte Methoden für die Entwicklung sichererer Anwendungen. |
| [Certificate Enrollment API (Zertifikatregistrierungs-API, in englischer Sprache)](./seccertenroll/certenroll-portal.md) | Die Zertifikatregistrierungs-API kann verwendet werden, um eine Clientanwendung zum Anfordern eines Zertifikats und Installieren einer Zertifikatantwort zu erstellen. |
| [Ablaufsteuerungsschutz (CFG, Control Flow Guard) ](./secbp/control-flow-guard.md) | Control Flow Guard (CFG) ist ein hochoptimiertes Plattformsicherheitsfeature, das erstellt wurde, um Sicherheitsrisiken durch Speicherbeschädigungen zu beseitigen. |
| [Kryptografie](./seccrypto/cryptography-portal.md) | Kryptografie ist die Verwendung von Codes zum Konvertieren von Daten, sodass nur ein bestimmter Empfänger sie mithilfe eines Schlüssels lesen kann. Mit CryptoAPI können Benutzer Dokumente und andere Daten in einer sicheren Umgebung erstellen und austauschen, insbesondere über unsichere Medien wie das Internet. |
| [Kryptografie-API: Nächste Generation](./seccng/cng-portal.md) | Kryptografie-API: Mit der nächsten Generation (CNG) können Benutzer Dokumente und andere Daten in einer sicheren Umgebung erstellen und austauschen, insbesondere über unsichere Medien wie das Internet. |
| [Erweiterbarkeit Access Control dynamischen Entwicklern](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | Das DAC-Szenario (Dynamic Access Control), das in Windows Server 2012 bereitgestellt wird, verfügt über eine Vielzahl von Erweiterungspunkten für Entwickler, die Anpassungsmöglichkeiten für die Entwicklung Ihrer Anwendungen bieten. |
| [Verzeichnis, Identität und Access Services](./srvnodes/directory--identity--and-access-services.md) | Netzwerkadministratoren können Verzeichnisdienste verwenden, um allgemeine Verwaltungsaufgaben wie das Hinzufügen von Benutzern und Gruppen, das Verwalten von Druckern und das Festlegen von Berechtigungen für Netzwerkressourcen zu automatisieren.<br/> Unabhängige Softwarehersteller und Endbenutzerentwickler können Verzeichnisdienste verwenden, um ihre Produkte und Anwendungen in Verzeichnissen zu aktivieren. Dienste können sich selbst in einem Verzeichnis veröffentlichen, Clients können das Verzeichnis verwenden, um Dienste zu suchen, und beide können das Verzeichnis verwenden, um andere Objekte zu suchen und zu bearbeiten.<br/> Forefront Identity Manager (FIM) bietet eine integrierte und umfassende Lösung für die Verwaltung des gesamten Lebenszyklus von Benutzeridentitäten und der zugehörigen Anmeldeinformationen.<br/> Identity Lifecycle Manager (ILM) ermöglicht IT-Organisationen, die Kosten für die Verwaltung des Identitäts- und Zugriffslebenszyklus zu senken, indem sie eine einzige Ansicht der Identität eines Benutzers im heterogenen Unternehmen und durch die Automatisierung gängiger Aufgaben bereitstellen.<br/> Active Directory Verbunddienst (AD FS) ermöglicht die Verbundidentitäts- und Zugriffsverwaltung, indem digitale Identitäten und Berechtigungsrechte über Sicherheits- und Unternehmensgrenzen hinweg sicher gemeinsam verwendet werden. |
| [Extensible Authentication-Protokoll](./eap/extensible-authentication-protocol-reference.md) | Das Extensible Authentication Protocol (EAP) ist ein Standard, der von mehreren Systemkomponenten unterstützt wird. EAP ist entscheidend für den Schutz der Sicherheit von drahtlos (802.1X) und kabelgebundenen LANs, DFÜ- und virtuellen privaten Netzwerken (VPNs). |
| [Erweiterbarer Authentifizierungsprotokollhost](./eaphost/about-eap-host.md) | EAPHost ist eine Microsoft Windows-Netzwerkkomponente, die eine EAP-Infrastruktur (Extensible Authentication Protocol) für die Authentifizierung von "supplicant"-Protokollimplementierungen wie 802.1X und Point-to-Point (AUTH) bietet. |
| [MS-CHAP-Kennwort Verwaltungs-API](/previous-versions/windows/desktop/mschap/portal) | Sie können das MS-CHAP-Kennwort-Verwaltungs-API, um Anwendungen zum Ändern der Kennwörter von Netzwerkbenutzern auf Remotearbeitsstationen zu erstellen. |
| [Netzwerkzugriffsschutz](./nap/network-access-protection-start-page.md) | Network Access Protection (NAP) ist ein Satz von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen. Die NAP-Plattform bietet eine integrierte Möglichkeit, den Systemstatus eines Netzwerkclients zu bewerten, der versucht, eine Verbindung mit einem Netzwerk herzustellen oder in einem Netzwerk zu kommunizieren, und den Zugriff des Netzwerkclients so lange zu beschränken, bis die Anforderungen an die Integritätsrichtlinie erfüllt sind. |
| [Netzwerkrichtlinienserver](./nps/portal.md) | Der Netzwerkrichtlinienserver (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und eines Proxys. Es ist der Nachfolger des Internetauthentifizierungsdiensts (Internet Authentication Service, IAS). |
| [Jugendschutz](./parcon/parental-controls-portal.md) | Die Technologie für die Jugendkontrolle in Windows soll dafür sorgen, dass eltern- oder wächterschaftsberechtigte Personen nach Alter oder Reifegrad auf geeignete Materialien zugreifen können. Zusätzlich zu den integrierten Funktionen bietet sie eine erweiterbare Infrastruktur. |
| [Rights Management](./srvnodes/rights-management.md) | Drei Generationen von Rights Management SDK sind jetzt verfügbar sowie eine roadmap für von Microsoft bereitgestellte RMS-Codebeispiele und Entwicklertools für alle unterstützten Betriebssysteme. Android, iOS/OS X, Windows Phone und Windows Desktop. |
| [Security Development Lifecycle (SDL) – Prozessleitfaden](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft Security Development Lifecycle (SDL) ist ein branchenführender Softwaresicherheits-Assurance-Prozess. Eine microsoftweite Initiative und eine obligatorische Richtlinie seit 2004, hat der SDL eine wichtige Rolle beim Einbetten von Sicherheit und Datenschutz in Microsoft-Software und -Kultur spielt. Durch die Kombination eines ganzheitlichen und praktischen Ansatzes führt SDL Sicherheit und Datenschutz frühzeitig und in allen Phasen des Entwicklungsprozesses ein. |
| [Sicherheitsverwaltung](./secmgmt/management-portal.md) | Die Sicherheitsverwaltungstechnologien können verwendet werden, um die Richtlinie der lokalen Sicherheitsstelle (Local Security Authority, LSA) und die Kennwortfilterrichtlinie zu verwalten, die Fähigkeit von Programmen aus externen Quellen abfragen und Dienstanlagen zu verwenden, die die Funktionalität des Sicherheitskonfigurationstools erweitern. |
| [WMI-Sicherheitsanbieter](./secprov/secprov-portal.md) | Die Sicherheits-WMI-Anbieter ermöglichen Es Administratoren und Programmierern, BitLocker-Laufwerkverschlüsselung (BDE) und das Trusted Platform Module (TPM) mithilfe der Windows Management Instrumentation (WMI) zu konfigurieren. |
| [Sicherheitsglossar](./secgloss/security-glossary.md) | Enthält ein Glossar mit Sicherheitsbegriffen. |
| [TPM-Basisdienste](./tbs/tpm-base-services-portal.md) | Das feature Trusted Platform Module (TPM) Base Services (TBS) zentralisiert den TPM-Zugriff anwendungsübergreifend. Das TBS-Feature verwendet Prioritäten, die durch aufrufende Anwendungen angegeben werden, um den TPM-Zugriff kooperativ zu planen. |
| [Windows-Biometrieframework-API](./secbiomet/biometric-service-api-portal.md) | Sie können die Windows Biometrieframework-API verwenden, um Clientanwendungen zu erstellen, die biometrische Informationen von Endbenutzern sicher erfassen, speichern und vergleichen. |
| [Technische Artikel zur Sicherheit](https://msdn.microsoft.com/library/hh322936.aspx) | Artikel zu Sicherheit und Kryptografie. |



 

 

 