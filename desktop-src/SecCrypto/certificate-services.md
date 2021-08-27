---
description: Zertifikatdienste, ein Dienst, der auf einem Windows-Serverbetriebssystem ausgeführt wird, empfangen Anforderungen für neue digitale Zertifikate über Transporte wie RPC oder HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Zertifikatdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaac2e1ee01b588beedbe2e632e52ef41459a885782a7975e460182f8a211bef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126850"
---
# <a name="certificate-services"></a>Zertifikatdienste

[*Zertifikatdienste*](../secgloss/c-gly.md), ein Dienst, der auf einem Windows-Serverbetriebssystem ausgeführt wird, empfangen Anforderungen für neue digitale Zertifikate über Transporte wie RPC oder HTTP. Es überprüft jede Anforderung mit benutzerdefinierten oder standortspezifischen Richtlinien, legt optionale Eigenschaften für ein ausgestelltes Zertifikat fest und stellt das Zertifikat aus. Zertifikatdienste ermöglichen Administratoren das Hinzufügen von Elementen zu einer Zertifikatsperrliste (Certificate [*Revocation List,*](../secgloss/c-gly.md) CRL) und das regelmäßige Veröffentlichen signierter CRLs.

Zertifikatdienste enthalten programmierbare Schnittstellen zum Erstellen von Unterstützung für zusätzliche Transporte, Richtlinien und Zertifikateigenschaften und -formate.

In Windows Server 2003 können Zertifikatdienste 2.0 über Systemsteuerung installiert **werden,** indem Sie auf Programme hinzufügen oder entfernen und dann auf **Windows-Komponenten hinzufügen/entfernen** klicken, um Zertifikatdienste zu installieren oder zu deinstallieren. 

Die Konzepte der Zertifikatdienste werden in den folgenden Abschnitten ausführlich beschrieben. Der Inhalt soll Sie bei der Entwicklung von Anwendungen unterstützen, die mit Zertifikatdiensten interagieren.



| Content                                                                                                                                                           | `Section`                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Beschreibung der Features von Zertifikatdiensten                                                                                                               | [Features von Zertifikatdiensten](certificate-services-features.md)         |
| Übersicht über die Architektur der Zertifikatdienste                                                                                                                     | [Architektur der Zertifikatdienste](certificate-services-architecture.md) |
| Beziehung zwischen einem Zertifikat, dem Zertifikatssubjekt und dem öffentlichen Schlüssel des [ *Subjekts*](../secgloss/p-gly.md) | [Zertifikate und öffentliche Schlüssel](certificates-and-public-keys.md)           |
| Informationen zu den Zertifikatanforderungseigenschaften                                                                                                              | [Richtlinien für Zertifikatanforderungen](certificate-request-guidelines.md)       |
| Details zur Verarbeitung eines Zertifikats durch Zertifikatdienste                                                                                                 | [Informationen zu Zertifikaten](about-certificates.md)                               |
| Beschreibung des [*Erneuerungsprozesses der*](../secgloss/c-gly.md) Zertifizierungsstelle        | [Erneuerung der Zertifizierungsstelle](certification-authority-renewal.md)     |



 

Die folgenden zusätzlichen nützlichen Themen sind ebenfalls enthalten.



| Content                                                                                                                                             | `Section`                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Dokumentation zur Zertifikatregistrierungssteuerung, die Dienste zum Erstellen von Zertifikatanforderungen einschließlich Anforderungen für Smartcardbenutzer bietet. | [Steuerung der Zertifikatregistrierung](certificate-enrollment-control.md) |
| Dokumentation zur Microsoft Cryptographic Application Programming Interface, die kryptografische Sicherheitsdienste bietet.                | [Kryptografie-Essentials](cryptography-essentials.md)               |
| Dokumentation zur Smartcard, die Dienste für die Entwicklung und Verwendung von Smartcardsystemen bietet.                                                   | [Smartcard](../secauthn/smart-card-authentication.md)                     |
| Namenseigenschaften von Zertifikaten und Zertifikatanforderungen.                                                                                           | [Namenseigenschaften](name-properties.md)                               |
| Liste und Beschreibungen der [*X.509-Zertifikateigenschaften.*](../secgloss/x-gly.md)                                  | [Zertifikateigenschaften](certificate-properties.md)                 |



 

 

 
