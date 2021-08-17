---
title: Erweitern des Schemas
description: Das Active Directory-Verzeichnisdienstschema definiert die Attribute und Klassen, die in der Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory,using,schema,erweitern des Schemas
- Schema AD, Erweitern des Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c50853e7b782f46b84212965c249ac90b685958c799c1b44cd366d5526e158d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189558"
---
# <a name="extending-the-schema"></a>Erweitern des Schemas

Das Active Directory-Verzeichnisdienstschema definiert die Attribute und Klassen, die in der Active Directory Domain Services. Das im System enthaltene Basisschema enthält einen großen Satz von Klassendefinitionen, z. B. Benutzer-, Computer- und organizationalUnit-Attributdefinitionen, sowie Attributdefinitionen wie **userPrincipalName,** **telephoneNumber** und **objectSid.**  Die vorhandenen Klassen und Attribute sind für die meisten Anwendungen ausreichend. Das Schema ist jedoch erweiterbar, was bedeutet, dass Sie neue Klassen und Attribute definieren können. In diesem Abschnitt wird erläutert, wie Sie das Active Directory-Schema erweitern.

## <a name="when-to-extend-the-schema"></a>Wann das Schema erweitert werden soll

Wenn die vorhandenen Klassen und Attribute nicht mit dem Datentyp passen, den Sie speichern möchten, sollten Sie das Schema erweitern. Es ist wichtig zu beachten, dass Schemaerweiterungen dauerhaft sind. Sie können Klassen und Attribute deaktivieren, aber nie aus dem Schema entfernen. Beachten Sie dies beim Testen von Code.

Berücksichtigen Sie auch die Größe der Daten, die Sie speichern möchten. Microsoft empfiehlt, dass kein Attributwert 500 Kilobyte überschreitet, einschließlich der Summe mehrwertigen Attribute. Außerdem sollten Objekte eine Größe von 1 Megabyte nicht überschreiten. Berücksichtigen Sie auch die Anzahl der Instanzen der Daten. Wenn Sie der [**User-Klasse**](/windows/desktop/ADSchema/c-user) auf einem System mit 100.000 Benutzern ein neues Attribut hinzufügen, kann dies erheblichen Speicherplatz auf sichdingen.

Zu den Themen in diesem Abschnitt gehören:

-   Hier erfahren Sie, wie Sie eine Bindung an den Schemacontainer erstellen und die Eigenschaften vorhandener Klassen und Attribute lesen.
-   Wie und wann das Schema erweitert werden soll, indem neue Attribute und Klassen definiert werden.
-   Installieren von Schemaerweiterungen mit LDIFDE, CSVDE oder programmgesteuert mit ADSI.

Weitere Informationen und eine Übersicht über das Active Directory-Schema, einschließlich Informationen zur Schemaimplementierung, Klassendefinitionen und Attributdefinitionen, finden Sie unter [Active Directory-Schema.](active-directory-schema.md)

Weitere Informationen, einschließlich Referenzseiten für die vordefinierten Schemaklassen, Attribute und Attributsyntaxen, finden Sie in der Active Directory-Schemareferenz in Active Directory Domain Services [Referenz.](active-directory-domain-services-reference.md)

 

 