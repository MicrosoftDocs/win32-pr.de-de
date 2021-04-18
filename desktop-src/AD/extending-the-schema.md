---
title: Erweitern des Schemas
description: Das Schema für den Active Directory Directory-Dienst definiert die Attribute und Klassen, die in Active Directory Domain Services verwendet werden.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory mit, Schema, Erweitern des Schemas
- Schema AD, Erweitern des Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106337419"
---
# <a name="extending-the-schema"></a>Erweitern des Schemas

Das Schema für den Active Directory Directory-Dienst definiert die Attribute und Klassen, die in Active Directory Domain Services verwendet werden. Das Basis Schema, das im System enthalten ist, enthält einen umfangreichen Satz von Klassendefinitionen, wie z. b. **User**, **Computer** und **OrganizationalUnit**, und Attribut Definitionen, wie z. b. **userPrincipalName**, **telefonienumber** und **objectSID**. Die vorhandenen Klassen und Attribute sind für die meisten Anwendungen ausreichend. Das Schema ist jedoch erweiterbar, was bedeutet, dass Sie neue Klassen und Attribute definieren können. In diesem Abschnitt wird erläutert, wie das Active Directory Schema erweitert wird.

## <a name="when-to-extend-the-schema"></a>Wann soll das Schema erweitert werden?

Wenn die vorhandenen Klassen und Attribute nicht in den Datentyp passen, den Sie speichern möchten, sollten Sie das Schema erweitern. Es ist wichtig zu beachten, dass Schema Ergänzungen permanent sind. Sie können Klassen und Attribute deaktivieren, Sie können Sie jedoch nie aus dem Schema entfernen. Beachten Sie dies, wenn Sie Code testen.

Beachten Sie auch die Größe der Daten, die Sie speichern möchten. Microsoft empfiehlt, dass kein Attribut Wert 500 Kilobyte, einschließlich der Summe der mehrwertigen Attribute, überschreitet. Außerdem sollte die Größe von Objekten 1 Megabyte nicht überschreiten. Beachten Sie auch die Anzahl der Instanzen der Daten. Wenn Sie der [**User**](/windows/desktop/ADSchema/c-user) -Klasse auf einem System mit 100.000 Benutzern ein neues Attribut hinzufügen, kann dies einen beträchtlichen Speicherplatz beanspruchen.

Die Themen in diesem Abschnitt umfassen Folgendes:

-   Binden an den Schema Container und Lesen der Eigenschaften vorhandener Klassen und Attribute.
-   Gibt an, wie und wann das Schema durch Definieren neuer Attribute und Klassen erweitert werden soll.
-   Installieren von Schema Erweiterungen mithilfe von LDIFDE, CSVDE oder Programm gesteuert mit ADSI.

Weitere Informationen und eine Übersicht über das Active Directory Schema, einschließlich Informationen über die Schema Implementierung, Klassendefinitionen und Attribut Definitionen, finden Sie unter [Active Directory Schema](active-directory-schema.md).

Weitere Informationen, einschließlich Referenzseiten für die vordefinierten Schema Klassen, Attribute und Attributsyntaxen, finden Sie in der Active Directory-Schema Referenz in der [Active Directory Domain Services Referenz](active-directory-domain-services-reference.md).

 

 