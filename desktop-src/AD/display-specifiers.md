---
title: Anzeige spezifiker
description: In Active Directory Domain Services definiert eine Objektklasse oder Klasse einen Objekttyp, der in Active Directory Domain Services erstellt werden kann.
ms.assetid: 0c31b02b-9fd3-4547-9ebc-d511a10d7106
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be9df0b81427bafa6ebe6707a33e86b6aff7416
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948581"
---
# <a name="display-specifiers"></a>Anzeige spezifiker

In Active Directory Domain Services definiert eine Objektklasse oder Klasse einen Objekttyp, der in Active Directory Domain Services erstellt werden kann. Die Definition jeder Objektklasse wird als [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objekt im [Active Directory Schema](active-directory-schema.md)gespeichert. Neben der **classSchema** -Definition kann jede Objektklasse über einen oder mehrere Anzeige Spezifizierer verfügen, die die Benutzeroberflächen Daten für Objekte dieser Klasse angeben.

Ein Anzeige Spezifizierer ist ein Objekt der [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Klasse. Die Attribute eines **displaySpecifier** -Objekts geben lokalisierte Benutzeroberflächen Daten an, die die verschiedenen Benutzeroberflächen Elemente für eine bestimmte Objektklasse beschreiben. Anzeige Spezifizierer speichern Daten für Eigenschaften Blätter, Kontextmenüs, Symbole, Erstellungs-Assistenten und lokalisierte Klassen-und Attributnamen. Bei Eigenschaften Seiten und Kontextmenüs werden diese Daten von der Windows-Shell und Active Directory administrativen Snap-Ins verwendet, um verschiedene Benutzeroberflächen für Administratoren und Endbenutzer zu bilden – ein Satz von Eigenschaften Seiten und/oder Kontextmenüs kann administrativen Anwendungen zugeordnet werden, während einem anderen Satz von Elementen Endbenutzer Anwendungen zugeordnet werden können.

Die [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Objekte werden in Gebiets Schema spezifischen Containern im DisplaySpecifiers-Container im Konfigurations Container gespeichert, der auf jeden Domänen Controller in der Gesamtstruktur des Unternehmens repliziert wird. Der displayspecifies-Container weist Subcontainer auf, die den verschiedenen von der Enterprise-Installation unterstützten Gebiets Schemas entsprechen. Diese unter Container werden mithilfe von sprach bezeichern benannt. Der Name des Gebiets Schema Containers für US-English lautet beispielsweise 409. Dies entspricht dem hexadezimal sprach Bezeichner 0x0409. Daher kann eine Objektklasse über mehrere Anzeige Spezifizierer verfügen: eine in jedem Gebiets Schema-unter Container. Weitere Informationen und eine Liste der möglichen sprach Bezeichner finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen. Weitere Informationen zu Gebiets Schemas finden Sie unter Gebiets Schemas [und Sprachen](/windows/desktop/Intl/locales-and-languages).

Der Name eines [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Objekts wird gebildet, indem die Zeichenfolge "-Display" an den [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) der Objektklasse angehängt wird. Beispielsweise ist der Name eines **displaySpecifier** -Objekts für die [**User**](/windows/desktop/ADSchema/c-user) -Klasse "User-Display".

Sie können Eigenschaften der [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) -Objekte einer Klasse hinzufügen, löschen oder ändern, um die Benutzeroberflächen Elemente (Klassenname, Attributnamen, Eigenschaften Blätter, Kontextmenüs, Symbol usw.) anzugeben, die für jede Instanz eines Objekts dieser Klasse angezeigt werden.

Weitere Informationen zu Anzeige spezifiken finden Sie unter [displayspecifieres Container](displayspecifiers-container.md).

 

 