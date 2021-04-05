---
description: Access Control bezieht sich auf Sicherheitsfunktionen, die Steuern, wer auf Ressourcen im Betriebssystem zugreifen kann. Anwendungen greifen auf Zugriffs Steuerungsfunktionen zu, um festzulegen, wer auf bestimmte Ressourcen zugreifen oder den Zugriff auf von der Anwendung bereitgestellte Ressourcen steuern kann.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Access Control (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042138"
---
# <a name="access-control-authorization"></a>Access Control (Autorisierung)

Access Control bezieht sich auf Sicherheitsfunktionen, die Steuern, wer auf Ressourcen im Betriebssystem zugreifen kann. Anwendungen greifen auf Zugriffs Steuerungsfunktionen zu, um festzulegen, wer auf bestimmte Ressourcen zugreifen oder den Zugriff auf von der Anwendung bereitgestellte Ressourcen steuern kann.

In dieser Übersicht wird das Sicherheitsmodell zum Steuern des Zugriffs auf Windows-Objekte, z. b. Dateien, und zum Steuern des Zugriffs auf Verwaltungsfunktionen, wie das Festlegen der Systemzeit oder das Überwachen von Benutzeraktionen, beschrieben. Das Thema [Access Control Modell](access-control-model.md) enthält eine allgemeine Beschreibung der Teile der Zugriffs Steuerung und deren Interaktion untereinander.

In den folgenden Themen wird die Zugriffs Steuerung beschrieben:

-   [Sicherheit auf C2-Ebene](c2-level-security.md)
-   [Access Control Modell](access-control-model.md)
-   [Definitions Sprache für Sicherheits Deskriptoren](security-descriptor-definition-language.md)
-   [Berechtigungen](privileges.md)
-   [Generierung von Überwachungsdatensätzen](audit-generation.md)
-   [Sicherungs fähige Objekte](securable-objects.md)
-   [Access Control auf niedriger Ebene](low-level-access-control.md)

Im folgenden werden allgemeine Zugriffs Steuerungsaufgaben aufgeführt:

-   [Steuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md)
-   [Steuern der Erstellung von untergeordneten Objekten in C++](controlling-child-object-creation-in-c--.md)
-   [ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts](aces-to-control-access-to-an-object-s-properties.md)
-   [Anfordern von Zugriffsrechten für ein Objekt](requesting-access-rights-to-an-object.md)

In den folgenden Themen wird Beispielcode für Zugriffs Steuerungsaufgaben bereitgestellt:

-   [Ändern der ACLs eines Objekts in C++](modifying-the-acls-of-an-object-in-c--.md)
-   [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [Steuern der Erstellung von untergeordneten Objekten in C++](controlling-child-object-creation-in-c--.md)
-   [Aktivieren und Deaktivieren von Berechtigungen in C++](enabling-and-disabling-privileges-in-c--.md)
-   [Suchen nach einer SID in einem Zugriffs Token in C++](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [Suchen des Besitzers eines File-Objekts in C++](finding-the-owner-of-a-file-object-in-c--.md)
-   [Übernehmen des Objekt Besitzes in C++](taking-object-ownership-in-c--.md)
-   [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 
