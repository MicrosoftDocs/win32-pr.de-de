---
title: Wann sollte das Schema erweitert werden?
description: Erweitern Sie das Schema nur, wenn keine vorhandene Objektklasse die Anforderungen Ihrer Anwendung erfüllt. Das Erweitern des Schemas ist ein komplexer Vorgang. Schemaänderungen werden auf jeden Domänencontroller in der Unternehmensgestruktur repliziert. Berücksichtigen Sie dies sorgfältig.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Wann sollte schema ad erweitert werden?
- Schema AD , wann erweitert werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042665069b06804dd648798debca6e0cee5628e115f5f512718ea0a51cc765ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024328"
---
# <a name="when-to-extend-the-schema"></a>Wann sollte das Schema erweitert werden?

Erweitern Sie das Schema nur, wenn keine vorhandene Objektklasse die Anforderungen Ihrer Anwendung erfüllt. Das Erweitern des Schemas ist ein komplexer Vorgang. Schemaänderungen werden auf jeden Domänencontroller in der Unternehmensgestruktur repliziert. Berücksichtigen Sie dies sorgfältig.

Das Schema kann auf drei Arten erweitert werden:

-   Leiten Sie eine neue Unterklasse von einer vorhandenen Klasse ab: Die Unterklasse verfügt über alle Attribute der Übergeordneten Klasse und alle attribute, die Sie angeben. Leiten Sie von einer vorhandenen Klasse ab:
    -   Wenn die vorhandene Klasse zusätzliche Attribute erfordert, andernfalls jedoch akzeptabel ist.
    -   Wenn die Fähigkeit zum Transformieren vorhandener Objekte der -Klasse in eine neue Klasse nicht erforderlich ist. Es ist nicht möglich, einem vorhandenen Objekt eine Unterklasse hinzuzufügen.
    -   So verwenden Sie das vorhandene Verzeichnis-Manager-Snap-In zum Verwalten der erweiterten Attribute der Objekte.
-   Fügen Sie einer vorhandenen Klasse Attribute hinzu, und/oder fügen Sie übergeordnete Objekte für die Klasse hinzu. Wenn Sie mehrere Attribute hinzufügen, führen Sie diesen Vorgang strukturiert aus, indem Sie eine Hilfsklasse definieren und diese Hilfsklasse der vorhandenen Klasse hinzufügen.
-   Eine Änderung einer vorhandenen Klasse ist erforderlich, wenn eine Anwendung die Möglichkeit benötigt, vorhandene Objekte der -Klasse zu erweitern. Um beispielsweise anwendungsspezifische Daten zum User-Objekt hinzuzufügen, erweitern Sie die Klasse Benutzer normal, da Sie vorhandene Benutzer und nicht nur spezielle Benutzer behandeln müssen, die von Ihrer Anwendung erstellt wurden.
-   Erstellen Sie eine neue Klasse mit den erforderlichen Attributen. Erstellen Sie eine neue Klasse. Das heißt, eine von "Top" abgeleitete Klasse, wenn keine vorhandene Klasse die betrieblichen Anforderungen erfüllt.

Wenn Sie eine vorhandene Klasse untergliedern, werden alle Benutzeroberflächenelemente, die der ursprünglichen Klasse zugeordnet sind, nicht von der Unterklasse geerbt. Wenn Sie beispielsweise ein Benutzerobjekt untergliedern, werden die Eigenschaftenseiten und Menüelemente, die dem Benutzer zugeordnet sind, nicht geerbt. Aus diesem Grund ist es besser, ein vorhandenes Objekt zu erweitern oder eine Hilfsklasse zu erstellen, anstatt eine Unterklasse zu erstellen.

Unabhängig davon, ob Sie eine vorhandene Klasse untergliedern oder eine vorhandene Klasse ändern, möchten Sie Tools wie das Active Directory-Benutzer und -Computer Snap-In erweitern, um die erweiterten Attribute der Objekte zu verwalten. Weitere Informationen finden Sie unter [Erweitern der Benutzeroberfläche für Verzeichnisobjekte.](extending-the-user-interface-for-directory-objects.md)

 

 




