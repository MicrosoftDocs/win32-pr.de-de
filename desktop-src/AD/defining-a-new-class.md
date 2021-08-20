---
title: Definieren einer neuen Klasse
description: Wenn Sie eine neue Klasse definieren, geben Sie die rechtlichen übergeordneten Klassen der neuen Klasse an, d. h. die Klassen, die Instanzen der neuen Klasse enthalten können.
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 464466588b1ce5f825021097217ca225f398cf682d2cecc4902e4b2dedd0d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019807"
---
# <a name="defining-a-new-class"></a>Definieren einer neuen Klasse

Wenn Sie eine neue Klasse definieren, geben Sie die rechtlichen übergeordneten Klassen der neuen Klasse an, d. h. die Klassen, die Instanzen der neuen Klasse enthalten können. Die rechtlichen übergeordneten Klassen werden in den **PossSuperiors-** und **systemPossSuperiors-Attributen** der neuen Klasse sowie in den möglichen übergeordneten Klassen angegeben, die von ihren Übergeordneten Klassen geerbt wurden, aber nicht von Hilfsklassen.

Achten Sie beim Definieren der rechtlichen übergeordneten Klassen für die neue Klasse auf spezifisch. Entscheiden Sie, wo Benutzer Instanzen Ihrer Klasse erstellen sollen. Wenn Sie z. B. "container" als rechtliches übergeordnetes Element angeben, kann der Benutzer Instanzen unter einem der Standardcontainer **(Container**, **organizationalUnit** usw.) erstellen, während die Angabe von "Computer" die Erstellung von Instanzen nur unter Instanzen des **Computerobjekts** ermöglicht.

**So erstellen Sie eine Klasse**

1.  Wählen Sie einen Namen für die Klasse aus. Weitere Informationen zum Verfassen eines allgemeinen Namens und eines LDAP-Anzeigenamens für eine neue Klasse finden Sie unter [Benennen von Attributen und Klassen.](naming-attributes-and-classes.md)
2.  Rufen Sie einen Objektbezeichner (OID) für die -Klasse ab. Weitere Informationen finden Sie unter [Abrufen eines Objektbezeichners.](obtaining-an-object-identifier.md)
3.  Wählen Sie eine "Standardobjektkategorie" für die Klasse aus. Weitere Informationen finden Sie unter [Objektklasse und Objektkategorie.](object-class-and-object-category.md)
4.  Wählen Sie eine "Objektklassenkategorie" für die Klasse aus. Dies gibt an, ob die Klasse abstrakt, strukturell oder hilfsweise ist. Weitere Informationen finden Sie unter [Strukturelle, Abstrakte und Hilfsklassen.](structural-abstract-and-auxiliary-classes.md)
5.  Erstellen Sie ein neues **classSchema-Objekt.** Viele Attribute können für ein **classSchema-Objekt** festgelegt werden. Die folgenden Attribute sind wichtig für die Definition einer neuen Klasse:

    -   Klassen, von denen die neue Klasse erbt: **subClassOf,** **auxiliaryClass** und **systemAuxiliaryClass**
    -   Namen und Bezeichner für die neue Klasse: **cn**, **lDAPDisplayName**, **adminDisplayName**, **schemaIDGUID**, **governsID**
    -   Mögliche Attribute der neuen Klasse: **mustContain**, **systemMustContain**, **mayContain**, **systemMayContain**
    -   Mögliche eltern der neuen Klasse: **possSuperiors**, **systemPossSuperiors**
    -   **objectClassCategory**
    -   **defaultObjectCategory**
    -   **defaultHidingValue**
    -   **rDnAttId**
    -   **defaultSecurityDescriptor**
    -   **description** (optional)

    Weitere Informationen und Beschreibungen dieser Attribute finden Sie unter [Merkmale von Objektklassen.](characteristics-of-object-classes.md)

    Beachten Sie, dass die in **subClassOf**, **possSuperiors**, **systemPossSuperiors**, **auxiliaryClass** und **systemAuxiliaryClass** angegebenen Klassen vorhanden sein müssen, wenn die neue Klasse in das Verzeichnis geschrieben wird. Andernfalls kann das **classSchema-Objekt** nicht zum Verzeichnis hinzugefügt werden. Ebenso müssen die in **mustContain**, **systemMustContain**, **mayContain** und **systemMayContain** angegebenen Attribute vorhanden sein, oder der Klassenerstellungsvorgang schlägt fehl.

6.  Schreiben Sie das neue **classSchema-Objekt** in das Verzeichnis.

**So fügen Sie der mayContain-Eigenschaft ein Attribut hinzu**

1.  Rufen Sie das **classSchema-Objekt** für die zu ändernde Klasse ab.
2.  Fügen Sie das neue Attribut der mehrwertigen **mayContain-Eigenschaft** hinzu.
3.  Schreiben Sie das geänderte **classSchema-Objekt** zurück in das Verzeichnis.

Neue Attribute können gleichzeitig mit neuen Klassen erstellt werden. Die Reihenfolge beim Erstellen der neuen Attribute und Klassen ist wichtig. Weitere Informationen finden Sie unter [Was die Installation tun muss.](what-the-installation-must-do.md)

**So fügen Sie gleichzeitig neue Attribute und neue Klassen hinzu**

1.  Definieren Sie zuerst alle neuen Attribute. Weitere Informationen finden Sie unter [Definieren eines neuen Attributs.](defining-a-new-attribute.md)
2.  Aktualisieren Sie den Schemacache, bevor Sie neue Klassen definieren. Weitere Informationen finden Sie unter [Aktualisieren des Schemacaches.](updating-the-schema-cache.md)
3.  Erstellen Sie die neuen Klassen.
4.  Fügen Sie den neuen Klassen die gewünschten Attribute hinzu.
5.  Aktualisieren Sie den Schemacache erneut.

 

 




