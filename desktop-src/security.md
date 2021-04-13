---
description: Entwickeln Sie mithilfe von Windows-APIs und-Diensten sicherere Desktop-Apps.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Sicherheit und Identität
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5b8fccc4039794fe76dabb34d88fa6d475a3b22a
ms.sourcegitcommit: 7f0c005e444c17f69b5ead403c43814f3bbe047a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "104391277"
---
# <a name="security-and-identity"></a>Sicherheit und Identität

Entwickeln Sie mithilfe von Windows-APIs und-Diensten sicherere Desktop-Apps. Diese APIs bieten Folgendes:

- Authentifizierung
- Autorisierung
- Kryptografie
- Verzeichnis-, Identitäts-und Zugriffs Dienste
- Eltern Steuerelemente
- Rights Management

In diesem Abschnitt werden auch bewährte Methoden und andere Artikel zur Sicherheit beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
| ----- | ----------- |
| [Antimalware-Scan Schnittstelle](./amsi/antimalware-scan-interface-portal.md) | Die Antischadsoftware Scan Interface (AMSI) ist ein generischer Schnittstellenstandard, mit dem Anwendungen und Dienste in jedes antischadsoftwareprodukt integriert werden können, das auf einem Computer vorhanden ist. Es bietet erweiterten Malware Schutz für Benutzer und Ihre Daten, Anwendungen und Workloads. |
| [Authentifizierung](./secauthn/authentication-portal.md) | Die Authentifizierung ist der Prozess, mit dem das System die Anmelde Informationen eines Benutzers überprüft. Der Name und das Kennwort eines Benutzers werden mit einer autorisierten Liste verglichen, und wenn das System eine Entsprechung erkennt, wird der Zugriff auf den in der Berechtigungs Liste für diesen Benutzer angegebenen Wert gewährt. |
| [Autorisierung](./secauthz/authorization-portal.md) | Die Autorisierung ist das Recht, dem eine Person die Verwendung des Systems und der darin gespeicherten Daten gewährt wurde. Die Autorisierung wird in der Regel von einem Systemadministrator eingerichtet und auf der Grundlage einer Art von Benutzeridentifikation (z. b. einer Codenummer oder eines Kennworts) vom Computer überprüft. |
| [Bewährte Methoden für die Sicherheits-APIs](./secbp/best-practices-for-the-security-apis.md) | Bietet bewährte Methoden für die Entwicklung sicherer Anwendungen. |
| [Certificate Enrollment API (Zertifikatregistrierungs-API, in englischer Sprache)](./seccertenroll/certenroll-portal.md) | Die Zertifikatregistrierungs-API kann verwendet werden, um eine Client Anwendung zum Anfordern eines Zertifikats und zum Installieren einer Zertifikats Antwort zu erstellen. |
| [Ablaufsteuerungsschutz (CFG, Control Flow Guard) ](./secbp/control-flow-guard.md) | Der Steuerungs Schutz (Control Flow Guard, cfg) ist ein hochoptimiertes Platt Form Sicherheits Feature, das erstellt wurde, um Sicherheitslücken im Speicher zu beheben. |
| [Kryptografie](./seccrypto/cryptography-portal.md) | Kryptografie ist die Verwendung von Codes zum Konvertieren von Daten, sodass nur ein bestimmter Empfänger ihn mit einem Schlüssel lesen kann. CryptoAPI ermöglicht Benutzern das Erstellen und Austauschen von Dokumenten und anderen Daten in einer sicheren Umgebung, insbesondere über nicht sichere Medien wie das Internet. |
| [Kryptografieapi: nächste Generation](./seccng/cng-portal.md) | Cryptography API: Next Generation (CNG) ermöglichen Benutzern das Erstellen und Austauschen von Dokumenten und anderen Daten in einer sicheren Umgebung, insbesondere über nicht sichere Medien wie das Internet. |
| [Dynamische Access Control Developer-Erweiterbarkeit](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | Das (Dynamic Access Control) Szenario, das in Windows Server 2012 bereitgestellt wurde, verfügt über eine Vielzahl von Erweiterbarkeits Punkten für Entwickler, die das Anpassungs Potenzial für die Entwicklung ihrer Anwendungen erhöhen. |
| [Verzeichnis-, Identitäts-und Zugriffs Dienste](./srvnodes/directory--identity--and-access-services.md) | Netzwerkadministratoren können mithilfe von Verzeichnisdiensten Häufige Verwaltungsaufgaben automatisieren, wie z. b. das Hinzufügen von Benutzern und Gruppen, das Verwalten von Druckern und das Festlegen von Berechtigungen für Netzwerkressourcen.<br/> Unabhängige Software Hersteller und Entwickler von Endbenutzern können Verzeichnisdienste verwenden, um Ihre Produkte und Anwendungen in einem Verzeichnis zu aktivieren. Dienste können sich selbst in einem Verzeichnis veröffentlichen, Clients können das Verzeichnis für die Suche nach Diensten verwenden, und beide können das Verzeichnis verwenden, um andere Objekte zu suchen und zu bearbeiten.<br/> Forefront Identity Manager (FIM) stellt eine integrierte und umfassende Lösung für die Verwaltung des gesamten Lebenszyklus von Benutzer Identitäten und der zugehörigen Anmelde Informationen bereit.<br/> Identity Lifecycle Manager (ILM) ermöglicht IT-Unternehmen, die Kosten für die Verwaltung der Identität und des Zugriffs Lebenszyklus zu verringern, indem eine einzelne Ansicht der Identität eines Benutzers im heterogenen Unternehmen und durch die Automatisierung gängiger Aufgaben bereitgestellt wird.<br/> Active Directory Verbunddienst (AD FS) ermöglicht die Verbund Identitäts-und Zugriffs Verwaltung durch sicheres Freigeben von digitaler Identität und Berechtigungs rechten in Sicherheits-und Unternehmensgrenzen. |
| [Extensible Authentication-Protokoll](./eap/extensible-authentication-protocol-reference.md) | Das Extensible Authentication-Protokoll (EAP) ist ein Standard, der von mehreren Systemkomponenten unterstützt wird. EAP ist für den Schutz der Sicherheit von drahtlosen (802.1 x) und verkabelten LANs, Einwähl-und VPNs (Virtual Private Networks) entscheidend. |
| [Extensible Authentication-Protokoll Host](./eaphost/about-eap-host.md) | EAPHost ist eine Microsoft Windows-Netzwerkkomponente, die eine EAP-Infrastruktur (Extensible Authentication Protocol) für die Authentifizierung von "Supplicant"-Protokollimplementierungen wie 802.1 x und Point-to-Point (PPP) bereitstellt. |
| [MS-CHAP-Kenn Wort Verwaltungs-API](/previous-versions/windows/desktop/mschap/portal) | Mit der MS-CHAP-Kenn Wort Verwaltungs-API können Sie Anwendungen erstellen, um die Kenn Wörter von Netzwerk Benutzern auf Remote Arbeitsstationen zu ändern. |
| [Netzwerk Zugriffsschutz](./nap/network-access-protection-start-page.md) | Der Netzwerk Zugriffsschutz (Network Access Protection, NAP) ist ein Satz von Betriebssystemkomponenten, die eine Plattform für den geschützten Zugriff auf private Netzwerke bereitstellen. Die NAP-Plattform bietet eine integrierte Möglichkeit, den System Integritäts Status eines Netzwerk Clients auszuwerten, der versucht, eine Verbindung mit einem Netzwerk herzustellen oder in einem Netzwerk zu kommunizieren und den Zugriff auf den Netzwerkclient einzuschränken, bis die Integritäts Richtlinien Anforderungen erfüllt sind. |
| [Netzwerkrichtlinienserver](./nps/portal.md) | Der Netzwerk Richtlinien Server (Network Policy Server, NPS) ist die Microsoft-Implementierung eines RADIUS-Servers (Remote Authentication Dial-in User Service) und-Proxys. Es ist der Nachfolger von Internet Authentication Service (IAS). |
| [Eltern Steuerelemente](./parcon/parental-controls-portal.md) | Die Jugend Steuerungs Technologie in Windows soll sorgfältigen Eltern oder Erziehungsberechtigten dabei helfen, den Zugriff auf die entsprechenden Materialien nach Alters-oder Reife Grad für die Benutzer zu gewährleisten. Es bietet zusätzlich zu den integrierten Funktionen eine erweiterbare Infrastruktur. |
| [Rights Management](./srvnodes/rights-management.md) | Drei Generationen Rights Management SDK sind jetzt verfügbar sowie eine gesamte Roadmap von Microsoft, die RMS-Codebeispiele und Entwicklertools für alle unterstützten Betriebssysteme bereitgestellt haben. Android, IOS/OS X, Windows Phone und Windows Desktop. |
| [Security Development Lifecycle (SDL)-Prozess Leit Faden](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft Security Development Lifecycle (SDL) ist ein branchenführender Software Sicherheits Assurance-Prozess. Eine Microsoft-weite Initiative und eine obligatorische Richtlinie seit 2004 hat das SDL beim Einbetten von Sicherheit und Datenschutz in Microsoft-Software und-Kultur eine entscheidende Rolle spielen. Durch die Kombination eines ganzheitlichen und praktischen Ansatzes führt SDL die Sicherheit und den Datenschutz frühzeitig und in allen Phasen des Entwicklungsprozesses ein. |
| [Sicherheitsverwaltung](./secmgmt/management-portal.md) | Die Sicherheits Verwaltungs Technologien können verwendet werden, um die Richtlinie für die lokale Sicherheits Autorität (LSA) und die Kenn Wortfilter Richtlinie zu verwalten, die Fähigkeit von Programmen aus externen Quellen abzufragen und Dienst Anlagen, die die Funktionalität des Sicherheits Konfigurationstools erweitern. |
| [WMI-Anbieter für Sicherheit](./secprov/secprov-portal.md) | Die WMI-Anbieter für Sicherheit ermöglichen es Administratoren und Programmierern, BitLocker-Laufwerkverschlüsselung (BDE) und Trusted Platform Module (TPM) mithilfe von Windows-Verwaltungsinstrumentation (WMI) zu konfigurieren. |
| [Sicherheits Glossar](./secgloss/security-glossary.md) | Stellt ein Glossar der Sicherheits Begriffe bereit. |
| [TPM-Basisdienste](./tbs/tpm-base-services-portal.md) | Die TPM-Funktion (Trusted Platform Module) zentralisiert den TPM-Zugriff auf Anwendungen. Das TSB-Feature verwendet Prioritäten, die durch den Aufruf von Anwendungen festgelegt werden, um den TPM-Zugriff zusammen |
| [Windows-Biometrieframework-API](./secbiomet/biometric-service-api-portal.md) | Sie können die Windows-Biometrieframework-API verwenden, um Client Anwendungen zu erstellen, die Endbenutzer-biometrische Informationen sicher erfassen, speichern und vergleichen. |
| [Technische Artikel zu Sicherheit](https://msdn.microsoft.com/library/hh322936.aspx) | Artikel zu Sicherheit und Kryptographie. |



 

 

 