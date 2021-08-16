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

Entwickeln Sie sicherere Desktop-Apps mit Windows APIs und Diensten. Diese APIs bieten Folgendes:

- Authentifizierung
- Autorisierung
- Kryptografie
- Verzeichnis-, Identitäts- und Zugriffsdienste
- Jugendschutz
- Rights Management

Dieser Abschnitt enthält auch bewährte Methoden und andere Artikel zur Sicherheit.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
| ----- | ----------- |
| [Antischadsoftware-Scanschnittstelle](./amsi/antimalware-scan-interface-portal.md) | Die Antischadsoftware-Scanschnittstelle (Antimalware Scan Interface, AMSI) ist ein generischer Schnittstellenstandard, mit dem Anwendungen und Dienste in jedes antischadsoftware-Produkt integriert werden können, das auf einem Computer vorhanden ist. Sie bietet verbesserten Schutz vor Schadsoftware für Benutzer und deren Daten, Anwendungen und Workloads. |
| [Authentifizierung](./secauthn/authentication-portal.md) | Authentifizierung ist der Prozess, mit dem das System die Anmeldeinformationen eines Benutzers überprüft. Der Name und das Kennwort eines Benutzers werden mit einer autorisierten Liste verglichen. Wenn das System eine Übereinstimmung erkennt, wird der Zugriff in dem Umfang gewährt, der in der Berechtigungsliste für diesen Benutzer angegeben ist. |
| [Autorisierung](./secauthz/authorization-portal.md) | Autorisierung ist das Recht, das einer Person gewährt wird, das System und die darin gespeicherten Daten zu verwenden. Die Autorisierung wird in der Regel von einem Systemadministrator eingerichtet und vom Computer anhand einer Form der Benutzeridentifikation überprüft, z. B. einer Codenummer oder einem Kennwort. |
| [Bewährte Methoden für die Sicherheits-APIs](./secbp/best-practices-for-the-security-apis.md) | Stellt bewährte Methoden für die Entwicklung sichererer Anwendungen bereit. |
| [Certificate Enrollment API (Zertifikatregistrierungs-API, in englischer Sprache)](./seccertenroll/certenroll-portal.md) | Die Zertifikatregistrierungs-API kann zum Erstellen einer Clientanwendung verwendet werden, um ein Zertifikat anzufordern und eine Zertifikatantwort zu installieren. |
| [Ablaufsteuerungsschutz (CFG, Control Flow Guard) ](./secbp/control-flow-guard.md) | Control Flow Guard (CFG) ist ein hochgradig optimiertes Plattformsicherheitsfeature, das erstellt wurde, um Sicherheitsrisiken durch Speicherbeschädigung zu beheben. |
| [Kryptografie](./seccrypto/cryptography-portal.md) | Kryptografie ist die Verwendung von Codes zum Konvertieren von Daten, sodass nur ein bestimmter Empfänger sie mithilfe eines Schlüssels lesen kann. Mit CryptoAPI können Benutzer Dokumente und andere Daten in einer sicheren Umgebung erstellen und austauschen, insbesondere über unsichere Medien wie das Internet. |
| [Kryptografie-API: Nächste Generation](./seccng/cng-portal.md) | Kryptografie-API: Next Generation (CNG) ermöglicht Benutzern das Erstellen und Austauschen von Dokumenten und anderen Daten in einer sicheren Umgebung, insbesondere über unsichere Medien wie das Internet. |
| [Erweiterbarkeit dynamischer Access Control Entwickler](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | Das Szenario mit dynamischem Access Control (Dynamic Access Control, DAC), das in Windows Server 2012 bereitgestellt wird, verfügt über eine Vielzahl von Erweiterbarkeitspunkten für Entwickler, die Anpassungsmöglichkeiten für die Entwicklung Ihrer Anwendungen bieten. |
| [Verzeichnis, Identität und Access Services](./srvnodes/directory--identity--and-access-services.md) | Netzwerkadministratoren können Verzeichnisdienste verwenden, um allgemeine administrative Aufgaben zu automatisieren, z. B. das Hinzufügen von Benutzern und Gruppen, das Verwalten von Druckern und das Festlegen von Berechtigungen für Netzwerkressourcen.<br/> Unabhängige Softwarehersteller und Endbenutzerentwickler können Verzeichnisdienste verwenden, um ihre Produkte und Anwendungen verzeichnisfähig zu machen. Dienste können sich selbst in einem Verzeichnis veröffentlichen, Clients können das Verzeichnis verwenden, um Dienste zu suchen, und beide können das Verzeichnis verwenden, um andere Objekte zu suchen und zu bearbeiten.<br/> Forefront Identity Manager (FIM) bietet eine integrierte und umfassende Lösung zum Verwalten des gesamten Lebenszyklus von Benutzeridentitäten und der zugehörigen Anmeldeinformationen.<br/> Mit Identity Lifecycle Manager (ILM) können IT-Organisationen die Kosten für die Verwaltung des Identitäts- und Zugriffslebenszyklus reduzieren, indem sie eine einzelne Ansicht der Identität eines Benutzers im heterogenen Unternehmen und durch die Automatisierung allgemeiner Aufgaben bereitstellen.<br/> Active Directory Verbunddienst (AD FS) ermöglicht die Verbundidentitäts- und Zugriffsverwaltung, indem digitale Identitäten und Berechtigungsrechte sicher über Sicherheits- und Unternehmensgrenzen hinweg freigegeben werden. |
| [Extensible Authentication-Protokoll](./eap/extensible-authentication-protocol-reference.md) | Das Extensible Authentication Protocol (EAP) ist ein Standard, der von mehreren Systemkomponenten unterstützt wird. EAP ist entscheidend für den Schutz der Sicherheit von drahtlos (802.1X) und kabelgebundenen LANs, DFÜ und virtuellen privaten Netzwerken (VPNs). |
| [Erweiterbarer Authentifizierungsprotokollhost](./eaphost/about-eap-host.md) | EAPHost ist eine Microsoft Windows Networking-Komponente, die eine EAP-Infrastruktur (Extensible Authentication Protocol) für die Authentifizierung von "supplipliorientierten" Protokollimplementierungen wie 802.1X und Point-to-Point (MOUSE) bereitstellt. |
| [MS-CHAP-Kennwort Verwaltungs-API](/previous-versions/windows/desktop/mschap/portal) | Sie können das MS-CHAP-Kennwort Verwaltungs-API verwenden, um Anwendungen zum Ändern der Kennwörter von Netzwerkbenutzern auf Remotearbeitsstationen zu erstellen. |
| [Netzwerkzugriffsschutz](./nap/network-access-protection-start-page.md) | Network Access Protection (NAP) ist ein Satz von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen. Die NAP-Plattform bietet eine integrierte Möglichkeit, den Systemstatus eines Netzwerkclients auszuwerten, der versucht, eine Verbindung mit einem Netzwerk herzustellen oder in einem Netzwerk zu kommunizieren, und den Zugriff auf den Netzwerkclient einzuschränken, bis die Anforderungen der Integritätsrichtlinie erfüllt sind. |
| [Netzwerkrichtlinienserver](./nps/portal.md) | Netzwerkrichtlinienserver (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und proxys. Er ist der Nachfolger des Internetauthentifizierungsdiensts (INTERNET Authentication Service, IAS). |
| [Jugendschutz](./parcon/parental-controls-portal.md) | Die Technologie der Jugendschutzfunktionen in Windows ist dafür vorgesehen, eltern- oder wächter Personen bei der Sicherstellung des Zugriffs auf geeignete Materialien nach Alter oder Reifegrad für Diejenigen zu unterstützen, die unter ihrer Wächterschaft stehen. Sie bietet zusätzlich zu den integrierten Funktionen eine erweiterbare Infrastruktur. |
| [Rights Management](./srvnodes/rights-management.md) | Drei Generationen von Rights Management SDK sind jetzt verfügbar und eine gesamte Roadmap für von Microsoft bereitgestellte RMS-Codebeispiele und Entwicklertools für alle unterstützten Betriebssysteme. Android, iOS/OS X, Windows Phone und Windows Desktop. |
| [Security Development Lifecycle (SDL) – Prozessleitfaden](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft Security Development Lifecycle (SDL) ist ein branchenführender Softwaresicherheitsprozess. Der SDL ist seit 2004 eine microsoftweite Initiative und eine obligatorische Richtlinie und hat eine wichtige Rolle bei der Einbettung von Sicherheit und Datenschutz in Microsoft-Software und -Kultur spielen. Der SDL kombiniert einen ganzheitlichen und praktischen Ansatz und führt Sicherheit und Datenschutz frühzeitig und in allen Phasen des Entwicklungsprozesses ein. |
| [Sicherheitsverwaltung](./secmgmt/management-portal.md) | Die Sicherheitsverwaltungstechnologien können verwendet werden, um richtlinien- und Kennwortfilterrichtlinien für lokale Sicherheitsautoritäten (Local Security Authority, LSA) zu verwalten, die Fähigkeit von Programmen aus externen Quellen abzufragen und Dienstanlagen abzufragen, die die Funktionalität des Sicherheitskonfigurationstools erweitern. |
| [WMI-Sicherheitsanbieter](./secprov/secprov-portal.md) | Die WMI-Sicherheitsanbieter ermöglichen Es Administratoren und Programmierern, BitLocker-Laufwerkverschlüsselung (BDE) und die Trusted Platform Module (TPM) mithilfe der Windows Management Instrumentation (WMI) zu konfigurieren. |
| [Sicherheitsglossar](./secgloss/security-glossary.md) | Enthält ein Glossar mit Sicherheitsbegriffen. |
| [TPM-Basisdienste](./tbs/tpm-base-services-portal.md) | Das Feature Trusted Platform Module (TPM) Base Services (TBS) zentralisiert den TPM-Zugriff anwendungsübergreifend. Das TBS-Feature verwendet Prioritäten, die durch Aufrufen von Anwendungen angegeben werden, um den TPM-Zugriff kooperativ zu planen. |
| [Windows-Biometrieframework-API](./secbiomet/biometric-service-api-portal.md) | Sie können die Windows Biometrieframework-API verwenden, um Clientanwendungen zu erstellen, die biometrische Endbenutzerinformationen sicher erfassen, speichern und vergleichen. |
| [Technische Artikel zur Sicherheit](https://msdn.microsoft.com/library/hh322936.aspx) | Artikel zu Sicherheit und Kryptografie. |



 

 

 