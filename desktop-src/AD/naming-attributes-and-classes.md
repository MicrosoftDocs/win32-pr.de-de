---
title: Benennen von Attributen und Klassen
description: Dieses Thema enthält Richtlinien zum Benennen von Attributen und Klassen.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Benennen von Attributen und Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e042decaf7d3dd15606ea7e138d9e6315d4200f2a641c10381951f2657a5aafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185999"
---
# <a name="naming-attributes-and-classes"></a>Benennen von Attributen und Klassen

Dieses Thema enthält Richtlinien zum Benennen von Attributen und Klassen.

Um eine neue Klasse oder ein neues Attribut zu erstellen, befolgen Sie die folgenden Benennungsregeln:

-   Verwenden Sie den gleichen Namen für die **cn-** und **lDAPDisplayName-Eigenschaften** eines neuen **attributeSchema-** oder **classSchema-Objekts.**
-   Identifizieren Sie das Unternehmen mit einem Präfix in Kleinbuchstaben im ersten Abschnitt des Namens. Dieses Präfix kann ein DNS-Name, ein Akronym oder eine andere Zeichenfolge sein, die das Unternehmen eindeutig identifiziert. Das Präfix stellt sicher, dass beim Durchsuchen des Schemas alle Attribute und Klassen für ein bestimmtes Unternehmen nacheinander angezeigt werden.
-   Wenn Sie eine Schemaerweiterung als unabhängiger Softwarehersteller entwickeln, fügen Sie eine Abkürzung des Produktnamens des Präfixes hinzu. Dadurch wird zwischen mehreren Produkten unterschieden, die LDAP-Schemaerweiterungen enthalten.
-   Verwenden Sie einen Bindestrich als nächstes Zeichen nach dem Präfix.
-   Geben Sie einen Attribut- oder Klassennamen an, der innerhalb der Attribute des Unternehmens nach dem Bindestrich eindeutig ist. Dieser Teil des allgemeinen Namens sollte beschreibend sein. Verwenden Sie keine unlogischen Namen, die für Entwickler und Betrachter des Schemas bedeutungslos sind.

Wenn beispielsweise das fiktive Fabrikam-Unternehmen das Schema durch Hinzufügen eines Attributs zum Speichern eines Voice-Mail-Bezeichners erweitert hat, können **cn** und **lDAPDisplayName** des neuen Attributs "fabrikam-VoiceMailID" lauten.

Wenn der **lDAPDisplayName** eines Attributs oder einer Klasse nicht angegeben ist, verwendet das System **cn,** um eines zu generieren. Der Systemalgorithmus zum Generieren des Namens kann jedoch zu Namenskonflikten oder Namen führen, die schwer zu lesen sind. Um diese Probleme zu vermeiden, wird empfohlen, einen **lDAPDisplayName** explizit für alle Attribute und Klassen anzugeben.

Zu Entwicklungs- und Testzwecken kann es wünschenswert sein, ein Versionssuffix an **cn** und **lDAPDisplayName** anzufügen, z.B. "fabrikam-VoiceMailID-001". In einer verteilten Entwicklungs-/Testumgebung können Entwickler mit einem Versionssuffix mehrere Versionen ihrer Software gleichzeitig ausführen. Benennen Sie nach Abschluss des Tests das Attribut oder die Klasse um, um das Suffix zu entfernen.

Es ist nicht möglich, alte Versionen von Schemaerweiterungen zu löschen, aber es ist möglich, sie zu deaktivieren und mit obskuren Namen umzubenennen. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute.](disabling-existing-classes-and-attributes.md)

 

 




