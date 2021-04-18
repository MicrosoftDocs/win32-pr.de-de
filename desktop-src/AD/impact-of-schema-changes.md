---
title: Auswirkungen von Schema Änderungen
description: In diesem Thema wird beschrieben, wie sich eine Schema Erweiterung auf die Active Directory Gesamtstruktur auswirkt.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Auswirkung von Schema Änderungen AD
- Schema AD, Auswirkung der Änderung des Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45aa43ed208b6eca5889220e09c78e8ada4a50a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338366"
---
# <a name="impact-of-schema-changes"></a>Auswirkungen von Schema Änderungen

Eine Schema Erweiterung wirkt sich auf eine Domänen Gesamtstruktur aus, die von Active Directory Domain Services gesteuert wird:

-   Schema Änderungen sind Global. Es gibt ein einzelnes Schema für eine gesamte Gesamtstruktur. Das Schema wird Global repliziert: eine Kopie des Schemas ist auf jedem DC in der Gesamtstruktur vorhanden. Wenn Sie das Schema erweitern, wird es für die gesamte Gesamtstruktur erweitert.
-   Schema Objekt Ergänzungen können nicht rückgängig gemacht werden. Wenn dem Schema eine neue Klasse oder ein neues Attribut Objekt hinzugefügt wird, kann es nicht entfernt werden. Ein vorhandenes Attribut oder eine vorhandene Klasse kann deaktiviert, aber nicht entfernt werden. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute](disabling-existing-classes-and-attributes.md). Das Deaktivieren einer Klasse oder eines Attributs wirkt sich nicht auf vorhandene Instanzen der Klasse oder des Attributs aus, verhindert jedoch das Erstellen neuer Instanzen. Ein Attribut kann nicht deaktiviert werden, wenn es in einer Klasse enthalten ist, die nicht deaktiviert ist.
-   OIDs müssen eindeutig sein. Wenn dem Schema ein Attribut oder eine Klasse hinzugefügt wird, kann kein Attribut oder keine Klasse mit derselben OID hinzugefügt werden. Dies gilt auch, wenn eine Klasse oder ein Attribut deaktiviert wurde. Aus diesem Grund müssen Sie gültige OIDs verwenden. Sie können keine OID synthetisieren und keine vorhandene OID wieder verwenden. Weitere Informationen zum Abrufen einer gültigen OID finden Sie unter Abrufen [eines Stamm Objekt Bezeichners](obtaining-an-object-identifier.md).
-   Nach der Erstellung können einige Änderungen vorgenommen werden:

    -   Für eine Klasse der Kategorie 1 oder Kategorie 2 können Sie Werte im Attribut " **possvorgesetzten** " hinzufügen oder entfernen. Die **Besitzer** Werte geben die Objektklassen an, die die Klasse enthalten können.
    -   Für eine Klasse der Kategorie 1 oder Kategorie 2 können Sie Werte im Attribut " **mayare** " hinzufügen oder entfernen. Die Werte von " **mayare** " geben die optionalen Attribute an, sind jedoch möglicherweise in einer Instanz der-Klasse vorhanden.

-   Der **ldapDisplayName** für eine Klasse oder ein Attribut der Kategorie 2 kann geändert werden, nachdem er erstellt wurde. In der Regel sollten Sie den **ldapDisplayName** nicht ändern. Es gibt jedoch einen legitimen Grund, den LDAP-Namen zu ändern. Dies liegt daran, dass Sie beim Definieren des Attributs oder der Klasse einen Fehler festgelegt haben und ein neues erstellen müssen, um das alte zu ersetzen. Um dies zu tun, müssen Sie nicht den relativen Distinguished Name (RDN) des Attributs oder des Klassen Schemas umbenennen. Wenn der LDAP-Name geändert wird, können Sie einen Fehler umgehen, anstatt die gesamte Windows 2000-Infrastruktur neu zu erstellen. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute](disabling-existing-classes-and-attributes.md).

    Der **ldapDisplayName** für vordefinierte Klassen oder Attribute (Kategorie 1) kann nicht geändert werden. Weitere Informationen zu Schema Objekten der Kategorie 1 und 2 finden Sie unter [Einschränkungen bei der Schema Erweiterung](restrictions-on-schema-extension.md).

 

 




