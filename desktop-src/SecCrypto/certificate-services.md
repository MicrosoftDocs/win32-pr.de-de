---
description: Zertifikat Dienste, ein Dienst, der unter einem Windows Server-Betriebssystem ausgeführt wird, empfangen Anforderungen für neue digitale Zertifikate über Transporte wie RPC oder http.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Zertifikatdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351410"
---
# <a name="certificate-services"></a>Zertifikatdienste

[*Zertifikat Dienste*](../secgloss/c-gly.md), ein Dienst, der unter einem Windows Server-Betriebssystem ausgeführt wird, empfangen Anforderungen für neue digitale Zertifikate über Transporte wie RPC oder http. Er überprüft jede Anforderung anhand von benutzerdefinierten oder standortspezifischen Richtlinien, legt optionale Eigenschaften für ein auszustelltes Zertifikat fest und gibt das Zertifikat aus. Mithilfe der Zertifikat Dienste können Administratoren einer Zertifikat Sperr [*Liste*](../secgloss/c-gly.md) (CRL) Elemente hinzufügen und signierte CRLs in regelmäßigen Abständen veröffentlichen.

Die Zertifikat Dienste enthalten programmierbare Schnittstellen zum Erstellen von Unterstützung für zusätzliche Transporte, Richtlinien und Zertifikat Eigenschaften und Formate.

In Windows Server 2003 können die Zertifikat Dienste 2,0 über die **Systemsteuerung** installiert werden. Klicken **Sie** hierzu auf Software und dann auf **Windows-Komponenten hinzufügen/entfernen** , um die Zertifikat Dienste zu installieren oder zu deinstallieren.

Die Konzepte der Zertifikat Dienste werden in den folgenden Abschnitten ausführlich beschrieben. Der Inhalt soll Ihnen dabei helfen, Anwendungen zu entwickeln, die mit Zertifikat Diensten interagieren werden.



| Inhalt                                                                                                                                                           | `Section`                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Beschreibung der Features der Zertifikat Dienste                                                                                                               | [Funktionen der Zertifikat Dienste](certificate-services-features.md)         |
| Übersicht über die Architektur der Zertifikat Dienste                                                                                                                     | [Architektur der Zertifikat Dienste](certificate-services-architecture.md) |
| Beziehung zwischen einem Zertifikat, dem Betreff des Zertifikats und dem [ *öffentlichen Schlüssel* des Antragstellers](../secgloss/p-gly.md) | [Zertifikate und öffentliche Schlüssel](certificates-and-public-keys.md)           |
| Informationen zu den Eigenschaften der Zertifikat Anforderung                                                                                                              | [Richtlinien für Zertifikat Anforderungen](certificate-request-guidelines.md)       |
| Details zur Verarbeitung eines Zertifikats durch Zertifikat Dienste                                                                                                 | [Informationen zu Zertifikaten](about-certificates.md)                               |
| Beschreibung des Erneuerungsprozesses der [*Zertifizierungs*](../secgloss/c-gly.md) Stelle        | [Erneuerung der Zertifizierungsstelle](certification-authority-renewal.md)     |



 

Die folgenden zusätzlichen nützlichen Themen sind ebenfalls enthalten.



| Inhalt                                                                                                                                             | `Section`                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Dokumentation zur Zertifikat Registrierungs Steuerung, die Dienste zum Erstellen von Zertifikat Anforderungen einschließlich Anforderungen für Smartcard-Benutzer bereitstellt. | [Zertifikat Registrierungs Steuerung](certificate-enrollment-control.md) |
| Dokumentation über die kryptografische Anwendungsprogrammierschnittstelle von Microsoft, die kryptografiebasierte Sicherheitsdienste bereitstellt.                | [Grundlagen der Kryptografie](cryptography-essentials.md)               |
| Dokumentation auf der Smartcard, die Dienste zum entwickeln und Verwenden von smartcardsystemen bereitstellt.                                                   | [Smartcard](../secauthn/smart-card-authentication.md)                     |
| Benennen Sie die Eigenschaften von Zertifikaten und Zertifikat Anforderungen.                                                                                           | [Namens Eigenschaften](name-properties.md)                               |
| Liste und Beschreibungen der [*X. 509*](../secgloss/x-gly.md) -Zertifikat Eigenschaften.                                  | [Zertifikat Eigenschaften](certificate-properties.md)                 |



 

 

 
