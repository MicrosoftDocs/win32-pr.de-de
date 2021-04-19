---
title: Wann soll das Schema erweitert werden?
description: Erweitern Sie das Schema nur dann, wenn keine vorhandene Objektklasse die Anforderungen Ihrer Anwendung erfüllt. Das Erweitern des Schemas ist ein komplexer Vorgang. Schema Änderungen werden auf allen Domänen Controllern in der Gesamtstruktur des Unternehmens repliziert. Berücksichtigen Sie dies sorgfältig.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Wann soll das Schema AD erweitert werden?
- Schema-AD, wann es erweitert werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338157"
---
# <a name="when-to-extend-the-schema"></a>Wann soll das Schema erweitert werden?

Erweitern Sie das Schema nur dann, wenn keine vorhandene Objektklasse die Anforderungen Ihrer Anwendung erfüllt. Das Erweitern des Schemas ist ein komplexer Vorgang. Schema Änderungen werden auf allen Domänen Controllern in der Gesamtstruktur des Unternehmens repliziert. Berücksichtigen Sie dies sorgfältig.

Das Schema kann auf drei Arten erweitert werden:

-   Leiten Sie eine neue Unterklasse von einer vorhandenen Klasse ab: die Unterklasse verfügt über alle Attribute der übergeordneten Klasse und alle Attribute, die Sie angeben. Von einer vorhandenen Klasse ableiten:
    -   Wenn die vorhandene Klasse zusätzliche Attribute erfordert, aber andernfalls akzeptabel ist.
    -   Wenn die Möglichkeit zum Transformieren vorhandener Objekte der Klasse in eine neue Klasse nicht erforderlich ist. Es ist nicht möglich, einem vorhandenen Objekt eine Unterklasse hinzuzufügen.
    -   Verwenden Sie das vorhandene Verzeichnis-Manager-Snap-in, um die erweiterten Attribute der Objekte zu verwalten.
-   Hinzufügen von Attributen zu einer vorhandenen Klasse und/oder Hinzufügen von übergeordneten Objekten für die Klasse. Wenn Sie mehrere Attribute hinzufügen, führen Sie diesen Vorgang strukturiert aus, indem Sie eine zusätzliche Klasse definieren und diese Hilfsklasse der vorhandenen Klasse hinzufügen.
-   Änderungen an einer vorhandenen Klasse sind erforderlich, wenn eine Anwendung die Möglichkeit benötigt, vorhandene Objekte der Klasse zu erweitern. Wenn Sie z. b. dem Benutzerobjekt anwendungsspezifische Daten hinzufügen möchten, erweitern Sie die Klasse Benutzer normal, da Sie vorhandene Benutzer und nicht nur die von der Anwendung erstellten speziellen Benutzer verarbeiten müssen.
-   Erstellen Sie eine neue Klasse mit den erforderlichen Attributen. Erstellen Sie eine neue Klasse. Das heißt, eine Klasse, die von "Top" abgeleitet wird, wenn keine vorhandene Klasse die betrieblichen Anforderungen erfüllt.

Wenn Sie eine Unterklasse einer vorhandenen Klasse unterteilen, werden alle der ursprünglichen Klasse zugeordneten Benutzeroberflächen Elemente nicht von der Unterklasse geerbt. Wenn Sie z. b. ein Benutzerobjekt Unterklassen, werden die dem Benutzer zugeordneten Eigenschaften Seiten und Menü Elemente nicht geerbt. Aus diesem Grund ist es vorzuziehen, ein vorhandenes Objekt zu erweitern oder eine Hilfsklasse zu erstellen, anstatt eine Unterklasse zu erstellen.

Unabhängig davon, ob Sie eine Unterklasse einer vorhandenen Klasse oder eine vorhandene Klasse ändern, sollten Sie Tools wie das Snap-in "Active Directory-Benutzer und-Computer" erweitern, um die erweiterten Attribute der Objekte zu verwalten. Weitere Informationen finden Sie unter [Erweitern der Benutzeroberfläche für Verzeichnisobjekte](extending-the-user-interface-for-directory-objects.md).

 

 




