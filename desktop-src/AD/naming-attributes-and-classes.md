---
title: Benennungs Attribute und-Klassen
description: Dieses Thema enthält Richtlinien für die Benennung von Attributen und Klassen.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Benennungs Attribute und-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "106339528"
---
# <a name="naming-attributes-and-classes"></a>Benennungs Attribute und-Klassen

Dieses Thema enthält Richtlinien für die Benennung von Attributen und Klassen.

Um eine neue Klasse oder ein neues Attribut zu erstellen, befolgen Sie die folgenden Benennungs Regeln:

-   Verwenden Sie den gleichen Namen für die **CN** -Eigenschaft und die **ldapDisplayName** -Eigenschaft eines neuen **attributeSchema** -oder **classSchema** -Objekts.
-   Identifizieren Sie das Unternehmen mit einem Kleinbuchstaben-Präfix im ersten Abschnitt des Namens. Dieses Präfix kann ein DNS-Name, ein Akronym oder eine andere Zeichenfolge sein, die das Unternehmen eindeutig identifiziert. Mit dem Präfix wird sichergestellt, dass alle Attribute und Klassen für ein bestimmtes Unternehmen beim Durchsuchen des Schemas nacheinander angezeigt werden.
-   Wenn Sie eine Schema Erweiterung als unabhängigen Softwarehersteller entwickeln, fügen Sie eine Abkürzung des Produkt namens des Präfix hinzu. Dadurch wird die Unterscheidung zwischen mehreren Produkten hinzugefügt, die LDAP-Schema Erweiterungen enthalten.
-   Verwenden Sie einen Bindestrich als das nächste Zeichen nach dem Präfix.
-   Geben Sie einen Attribut-oder Klassennamen an, der innerhalb des Unternehmens Attributs nach dem Bindestrich eindeutig ist. Dieser Teil des allgemeinen namens sollte beschreibend sein. Verwenden Sie keine unlogisch-Namen, die für Entwickler und Viewer des Schemas bedeutungslos sind.

Wenn beispielsweise das fiktive Fabrikam-Unternehmen das Schema durch Hinzufügen eines Attributs zum Speichern eines sprach-e-Mail-Bezeichners erweitert hat, könnte **CN** und **ldapDisplayName** des neuen Attributs "Fabrikam-voicemailid" lauten.

Wenn der **ldapDisplayName** eines Attributs oder einer Klasse nicht angegeben ist, verwendet das System den **CN** zum Generieren eines Attributs. Der System Algorithmus zum Erstellen des Namens kann jedoch zu Namenskollisionen oder Namen führen, die schwer lesbar sind. Um diese Probleme zu vermeiden, wird empfohlen, dass ein **ldapDisplayName** für alle Attribute und Klassen explizit angegeben wird.

Zu Entwicklungs-und Testzwecken ist es möglicherweise wünschenswert, ein Versions Suffix an **CN** und **ldapDisplayName** anzufügen, z. b. "Fabrikam-voicemailid-001". In einer verteilten Entwicklungs-/Testumgebung können Entwickler mit einem Versions Suffix mehrere Versionen Ihrer Software gleichzeitig ausführen. Benennen Sie nach Abschluss der Tests das Attribut oder die Klasse um, um das Suffix zu entfernen.

Es ist nicht möglich, veraltete Versionen von Schema Erweiterungen zu löschen, aber es ist möglich, Sie zu deaktivieren und Sie mit nicht verfallenen Namen umzubenennen. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute](disabling-existing-classes-and-attributes.md).

 

 




