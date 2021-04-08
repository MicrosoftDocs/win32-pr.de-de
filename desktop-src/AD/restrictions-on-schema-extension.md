---
title: Einschränkungen bei der Schema Erweiterung
description: Um die Wahrscheinlichkeit von Schema Änderungen durch eine Anwendung zu verringern, die andere Anwendungen unterbricht, und die Schema Konsistenz aufrechtzuerhalten, Active Directory Domain Services Einschränkungen für den Typ von Schema Änderungen erzwingen, die eine Anwendung oder ein Benutzer ausführen darf.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707566"
---
# <a name="restrictions-on-schema-extension"></a>Einschränkungen bei der Schema Erweiterung

Um die Wahrscheinlichkeit von Schema Änderungen durch eine Anwendung zu verringern, die andere Anwendungen unterbricht, und die Schema Konsistenz aufrechtzuerhalten, Active Directory Domain Services Einschränkungen für den Typ von Schema Änderungen erzwingen, die eine Anwendung oder ein Benutzer ausführen darf.

Die Einschränkungen werden nur beim Ändern vorhandener Schema Objekte auferlegt. Das Schema wird in zwei Kategorien eingeteilt. Die Schema Objekte, die im Basis Schema mit Windows 2000 ausgeliefert werden, gehören zu Kategorie 1. Alle Schema Objekte, die später von anderen Anwendungen oder Benutzern durch dynamische Schema Erweiterungen hinzugefügt werden, gehören zu Kategorie 2. Die Kategorie eines Schema Objekts kann durch das 0x10-Bit bestimmt werden, das im **systemFlags** -Attribut für das **classSchema** -Objekt festgelegt ist. Dieses Bit wird nur für Objekte der Kategorie 1 festgelegt und kann nicht geändert werden. es kann auch nicht für ein beliebiges Objekt der Kategorie 2 festgelegt werden.

Das **systemFlags** -Attribut wird intern von Active Directory Domain Services verwendet, um besondere Merkmale von "Infrastruktur"-Objekten im Basis Schema zu identifizieren. Zusätzlich zur Identifizierung von Objekten der Kategorie 1 steuert **systemFlags** , ob ein Objekt verschoben, gelöscht oder umbenannt werden kann. Diese Vorgänge werden für Objekte verhindert, von denen Windows 2000 abhängig ist, um ausgeführt zu werden.

Bei allen Schema Objekten, Kategorie 1 oder 2, müssen Active Directory Domain Services die folgenden Einschränkungen erzwingen:

-   Sie können eine neue **must-** Klasse nicht zu einer Klasse hinzufügen (direkt oder durch Vererbung durch Hinzufügen einer zusätzlichen Klasse).
-   Sie können keine **mustare** der Klasse löschen (direkt oder durch Vererbung).

Außerdem werden die folgenden zusätzlichen Einschränkungen für Schema Objekte der Kategorie 1 auferlegt:

-   Sie können die folgenden Attribute eines Attributs der Kategorie 1 nicht ändern:

    -   **rangeLower** und **rangeUpper** (Wertebereich).
    -   **attributeSecurityGuid** (bestimmt, in welchem Eigenschafts Satz das Attribut ggf. zu gehört).

-   Die **defaultobjectcategory** einer Klasse der Kategorie 1 kann nicht geändert werden.
-   Sie können die **objectCategory** einer beliebigen Instanz einer Klasse der Kategorie 1 nicht ändern.
-   Es ist nicht möglich, eine Klasse oder ein Attribut der Kategorie 1 zu überschreiben.
-   Es ist nicht möglich, den **ldapDisplayName** einer Klasse oder eines Attributs der Kategorie 1 zu ändern.
-   Sie können eine Klasse oder ein Attribut der Kategorie 1 nicht umbenennen.

 

 




