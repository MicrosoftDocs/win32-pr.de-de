---
title: Einschränkungen der Schemaerweiterung
description: Um die Wahrscheinlichkeit von Schemaänderungen durch eine Anwendung zu reduzieren, die andere Anwendungen unterbricht, und um die Schemakonsistenz zu gewährleisten, erzwingen Active Directory Domain Services Einschränkungen für den Typ der Schemaänderungen, die eine Anwendung oder ein Benutzer vornehmen darf.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94db3c3c96f5c9b4e96cff923e70501a8977669defbc03b95fd2df019886a138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184303"
---
# <a name="restrictions-on-schema-extension"></a>Einschränkungen der Schemaerweiterung

Um die Wahrscheinlichkeit von Schemaänderungen durch eine Anwendung zu reduzieren, die andere Anwendungen unterbricht, und um die Schemakonsistenz zu gewährleisten, erzwingen Active Directory Domain Services Einschränkungen für den Typ der Schemaänderungen, die eine Anwendung oder ein Benutzer vornehmen darf.

Die Einschränkungen gelten nur für die Änderung vorhandener Schemaobjekte. Das Schema ist in zwei Kategorien unterteilt. Die Schemaobjekte, die mit Windows 2000 im Basisschema enthalten sind, gehören zu Kategorie 1. Alle Schemaobjekte, die später von anderen Anwendungen oder Benutzern über die dynamische Schemaerweiterung hinzugefügt werden, gehören zu Kategorie 2. Die Kategorie eines Schemaobjekts kann durch die 0x10 festgelegten Bit im **systemFlags-Attribut** des **classSchema-Objekts bestimmt** werden. Dieses Bit wird nur für Objekte der Kategorie 1 festgelegt und kann weder geändert noch für ein Objekt der Kategorie 2 festgelegt werden.

Das **systemFlags-Attribut** wird intern von Active Directory Domain Services verwendet, um besondere Merkmale von Infrastrukturobjekten im Basisschema zu identifizieren. Zusätzlich zum Identifizieren von Objekten der Kategorie 1 steuert **systemFlags,** ob ein Objekt verschoben, gelöscht oder umbenannt werden kann. Diese Vorgänge werden für Objekte verhindert, von denen Windows 2000 abhängig ist.

Für alle Schemaobjekte, Kategorie 1 oder 2, Active Directory Domain Services die folgenden Einschränkungen vor:

-   Sie können einer Klasse kein **neues mustContain** hinzufügen (direkt oder durch Vererbung durch Hinzufügen einer Hilfsklasse).
-   MustContain der **Klasse kann nicht gelöscht** werden (direkt oder durch Vererbung).

Darüber hinaus gelten für Schemaobjekte der Kategorie 1 die folgenden zusätzlichen Einschränkungen:

-   Sie können die folgenden Attribute eines Category 1-Attributs nicht ändern:

    -   **rangeLower** und **rangeUpper** (Wertbereich).
    -   **attributeSecurityGuid** (bestimmt, zu welchem Eigenschaftensatz das Attribut gehört, falls dies der Fall ist).

-   Sie können die **defaultObjectCategory** einer Category 1-Klasse nicht ändern.
-   Sie können die **objectCategory einer** Instanz einer Category 1-Klasse nicht ändern.
-   Sie können nicht festlegen, dass eine Klasse oder ein Attribut der Kategorie 1 nicht mehr verwendet werden kann.
-   Sie können den **lDAPDisplayName einer** Klasse oder eines Attributs der Kategorie 1 nicht ändern.
-   Sie können eine Klasse oder ein Attribut der Kategorie 1 nicht umbenennen.

 

 




