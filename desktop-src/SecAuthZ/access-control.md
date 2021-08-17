---
description: Zugriffssteuerung bezieht sich auf Sicherheitsfeatures, die steuern, wer auf Ressourcen im Betriebssystem zugreifen kann. Anwendungen rufen Zugriffssteuerungsfunktionen auf, um zu festlegen, wer auf bestimmte Ressourcen zugreifen oder den Zugriff auf von der Anwendung bereitgestellte Ressourcen steuern kann.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Access Control (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34be93577446066fcaf7e01e634c60632c68c430198a375eadc2efbcec3e701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785640"
---
# <a name="access-control-authorization"></a>Access Control (Autorisierung)

Zugriffssteuerung bezieht sich auf Sicherheitsfeatures, die steuern, wer auf Ressourcen im Betriebssystem zugreifen kann. Anwendungen rufen Zugriffssteuerungsfunktionen auf, um zu festlegen, wer auf bestimmte Ressourcen zugreifen oder den Zugriff auf von der Anwendung bereitgestellte Ressourcen steuern kann.

Diese Übersicht beschreibt das Sicherheitsmodell zum Steuern des Zugriffs auf Windows-Objekte, z. B. Dateien, und zum Steuern des Zugriffs auf administrative Funktionen, z. B. festlegen der Systemzeit oder Überwachen von Benutzeraktionen. Das [Access Control Model-Thema](access-control-model.md) enthält eine allgemeine Beschreibung der Teile der Zugriffssteuerung und deren Interaktion.

In den folgenden Themen wird die Zugriffssteuerung beschrieben:

-   [Sicherheit auf C2-Ebene](c2-level-security.md)
-   [Access Control Modell](access-control-model.md)
-   [Definitionssprache für Sicherheitsbeschreibungen](security-descriptor-definition-language.md)
-   [Berechtigungen](privileges.md)
-   [Generierung von Überwachungsdatensätzen](audit-generation.md)
-   [Sicherungsfähige Objekte](securable-objects.md)
-   [Low-Level-Access Control](low-level-access-control.md)

Im Folgenden finden Sie allgemeine Aufgaben zur Zugriffssteuerung:

-   [Steuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md)
-   [Steuern der Erstellung untergeordneter Objekte in C++](controlling-child-object-creation-in-c--.md)
-   [ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts](aces-to-control-access-to-an-object-s-properties.md)
-   [Anfordern von Zugriffsrechten für ein Objekt](requesting-access-rights-to-an-object.md)

Die folgenden Themen enthalten Beispielcode für Zugriffssteuerungsaufgaben:

-   [Ändern der ACLs eines Objekts in C++](modifying-the-acls-of-an-object-in-c--.md)
-   [Erstellen eines Sicherheitsdeskriptors für ein neues Objekt in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [Steuern der Erstellung untergeordneter Objekte in C++](controlling-child-object-creation-in-c--.md)
-   [Aktivieren und Deaktivieren von Berechtigungen in C++](enabling-and-disabling-privileges-in-c--.md)
-   [Suchen nach einer SID in einem Zugriffstoken in C++](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [Suchen des Besitzers eines Dateiobjekts in C++](finding-the-owner-of-a-file-object-in-c--.md)
-   [Übernehmen des Objektbesitzes in C++](taking-object-ownership-in-c--.md)
-   [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 
