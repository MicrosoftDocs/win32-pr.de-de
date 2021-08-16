---
title: Auswirkungen von Schemaänderungen
description: In diesem Thema wird beschrieben, wie sich eine Schemaerweiterung auf die Active Directory-Gesamtstruktur auswirkt.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Auswirkungen von Schemaänderungen in AD
- Schema AD , Auswirkungen der Änderung des Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa9cc0ee4cdcd0da3581d6bf009837799387949e43dc68989612442352df591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187719"
---
# <a name="impact-of-schema-changes"></a>Auswirkungen von Schemaänderungen

Eine Schemaerweiterung wirkt sich auf verschiedene Weise auf eine Domänenstruktur aus, die von Active Directory Domain Services gesteuert wird:

-   Schemaänderungen sind global. Es gibt ein einzelnes Schema für eine gesamte Gesamtstruktur. Das Schema wird global repliziert: Auf jedem Domänencontroller in der Gesamtstruktur ist eine Kopie des Schemas vorhanden. Wenn Sie das Schema erweitern, wird es für die gesamte Gesamtstruktur erweitert.
-   Schemaobjekthinzufügungen können nicht rückgängig gemacht werden. Wenn dem Schema eine neue Klasse oder ein neues Attributobjekt hinzugefügt wird, kann es nicht entfernt werden. Ein vorhandenes Attribut oder eine vorhandene Klasse kann deaktiviert, aber nicht entfernt werden. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute.](disabling-existing-classes-and-attributes.md) Das Deaktivieren einer Klasse oder eines Attributs wirkt sich nicht auf vorhandene Instanzen der Klasse oder des Attributs aus, verhindert jedoch die Erstellung neuer Instanzen. Sie können ein Attribut nicht deaktivieren, wenn es in einer Klasse enthalten ist, die nicht deaktiviert ist.
-   OIDs müssen eindeutig sein. Wenn dem Schema ein Attribut oder eine Klasse hinzugefügt wird, kann kein Attribut oder keine Klasse mit derselben OID hinzugefügt werden. Dies gilt auch, wenn eine Klasse oder ein Attribut deaktiviert wurde. Aus diesem Grund müssen Sie gültige OIDs verwenden. Synthetisieren Sie keine OID, und verwenden Sie keine vorhandene OID wieder. Weitere Informationen zum Abrufen einer gültigen OID finden Sie unter [Abrufen eines Stammobjektbezeichners.](obtaining-an-object-identifier.md)
-   Einige Änderungen können nach der Erstellung vorgenommen werden:

    -   Für eine Klasse der Kategorie 1 oder Kategorie 2 können Sie Werte im **attribut possSuperiors** hinzufügen oder entfernen. Die **possSuperiors-Werte** geben die Objektklassen an, die die -Klasse enthalten können.
    -   Für eine Klasse der Kategorie 1 oder Kategorie 2 können Sie Werte im **mayContain-Attribut** hinzufügen oder entfernen. Die **mayContain-Werte** geben die optionalen Attribute an, können aber in einer Instanz der -Klasse vorhanden sein.

-   Der **lDAPDisplayName** für eine Klasse oder ein Attribut der Kategorie 2 kann nach der Erstellung geändert werden. In der Regel sollten Sie den **lDAPDisplayName** nicht ändern. Es gibt jedoch einen legitimen Grund für die Änderung des LDAP-Namens. Dies liegt daran, dass Sie beim Definieren des Attributs oder der Klasse einen Fehler gemacht haben und ein neues erstellen müssen, um das alte zu ersetzen. Hierfür müssen Sie den relativen Distinguished Name (RDN) des Attributs oder Klassenschemas nicht umbenennen. Wenn der LDAP-Name geändert wird, können Sie einen Fehler umgehen, anstatt die gesamte Windows 2000-Infrastruktur neu zu erstellen. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute.](disabling-existing-classes-and-attributes.md)

    Der **lDAPDisplayName** für vordefinierte Klassen oder Attribute (Kategorie 1) kann nicht geändert werden. Weitere Informationen zu Schemaobjekten der Kategorie 1 und 2 finden Sie unter [Einschränkungen für Schemaerweiterungen.](restrictions-on-schema-extension.md)

 

 




