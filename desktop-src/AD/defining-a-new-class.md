---
title: Definieren einer neuen Klasse
description: Wenn Sie eine neue Klasse definieren, geben Sie die juristischen übergeordneten Klassen der neuen Klasse an, d. h. die Klassen, die Instanzen der neuen Klasse enthalten können.
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947402"
---
# <a name="defining-a-new-class"></a>Definieren einer neuen Klasse

Wenn Sie eine neue Klasse definieren, geben Sie die juristischen übergeordneten Klassen der neuen Klasse an, d. h. die Klassen, die Instanzen der neuen Klasse enthalten können. Die zulässigen übergeordneten Klassen werden in den Attributen " **posstribute** " und " **systemposstribute** " der neuen Klasse sowie in den möglichen, von den übergeordneten Klassen geerbten, jedoch nicht aus Erweiterungs Klassen festgelegt.

Achten Sie auf die Definition der für die neue Klasse zulässigen übergeordneten Klassen. Entscheiden Sie, wo Benutzer Instanzen Ihrer Klasse erstellen sollen. Wenn Sie z. b. "Container" als übergeordnetes Element angeben, kann der Benutzer in einem der Standardcontainer (**Container**, **OrganizationalUnit** usw.) Instanzen erstellen, während die Angabe von "Computer" ermöglicht, dass Instanzen nur unter Instanzen des **Computer** Objekts erstellt werden.

**So erstellen Sie eine Klasse**

1.  Wählen Sie einen Namen für die Klasse aus. Weitere Informationen zum Erstellen eines allgemeinen Namens und eines LDAP-anzeigen Amens für eine neue Klasse finden Sie unter [Benennen von Attributen und Klassen](naming-attributes-and-classes.md).
2.  Abrufen eines Objekt Bezeichners (OID) für die Klasse. Weitere Informationen finden Sie unter Abrufen [eines Objekt Bezeichners](obtaining-an-object-identifier.md).
3.  Wählen Sie für die Klasse eine "Standard Objekt Kategorie" aus. Weitere Informationen finden Sie unter [Objektklasse und Objekt Kategorie](object-class-and-object-category.md).
4.  Wählen Sie für die Klasse eine "Objektklassen Kategorie" aus. Dies gibt an, ob die Klasse abstrakt, strukturell oder Hilfswert ist. Weitere Informationen finden Sie unter [Struktur-, abstrakte und Hilfsklassen](structural-abstract-and-auxiliary-classes.md).
5.  Erstellen Sie ein neues **classSchema** -Objekt. Viele Attribute können für ein **classSchema** -Objekt festgelegt werden. Die folgenden Attribute sind wichtig für die Definition einer neuen Klasse:

    -   Klassen, von denen die neue Klasse erbt: **subClassOf**, **auxiliaryClass** und **systemAuxiliaryClass**
    -   Namen und Bezeichner für die neue Klasse: **CN**, **ldapDisplayName**, **adminDisplayName**, **schemaIdGUID**, **governsId**
    -   Mögliche Attribute der neuen Klasse: **mustare**, **systemmustist**, **mayare**, **systemmayare**
    -   Mögliche übergeordnete Elemente der neuen Klasse: **possvorgesetzten**, **systempossvorgesetzten**
    -   **objectClassCategory**
    -   **defaultObjectCategory**
    -   **defaultHidingValue**
    -   **rDNAttID**
    -   **defaultSecurityDescriptor**
    -   **Beschreibung** (optional)

    Weitere Informationen und Beschreibungen dieser Attribute finden Sie unter [Merkmale von Objektklassen](characteristics-of-object-classes.md).

    Beachten Sie, dass die in **Unterklassen von**, **possvorgesetzten**, **systempossvorgesetzten**, **auxiliaryClass** und **systemAuxiliaryClass** angegebenen Klassen vorhanden sein müssen, wenn die neue Klasse in das Verzeichnis geschrieben wird. Andernfalls kann das **classSchema** -Objekt nicht zum Verzeichnis hinzugefügt werden. Entsprechend müssen die Attribute, die in " **musttribute**", " **systemmust"**, " **mayare**" und " **systemmayare**" angegeben sind, vorhanden sein, oder der Vorgang der Klassen Erstellung schlägt fehl

6.  Schreiben Sie das neue **classSchema** -Objekt in das Verzeichnis.

**So fügen Sie der Eigenschaft "mayare" ein Attribut hinzu**

1.  Rufen Sie das **classSchema** -Objekt für die zu ändernde Klasse ab.
2.  Fügen Sie das neue-Attribut der Eigenschaft " **mayare** mehr wertig" hinzu.
3.  Schreiben Sie das geänderte **classSchema** -Objekt zurück in das Verzeichnis.

Neue Attribute können gleichzeitig mit neuen Klassen erstellt werden. die Reihenfolge der Erstellung der neuen Attribute und Klassen ist wichtig. Weitere Informationen finden Sie unter [was die Installation tun muss](what-the-installation-must-do.md).

**So fügen Sie neue Attribute und neue Klassen gleichzeitig hinzu**

1.  Definieren Sie zuerst alle neuen Attribute. Weitere Informationen finden Sie unter [Definieren eines neuen Attributs](defining-a-new-attribute.md).
2.  Aktualisieren Sie den Schema Cache, bevor Sie neue Klassen definieren. Weitere Informationen finden Sie unter [Aktualisieren des Schema Caches](updating-the-schema-cache.md).
3.  Erstellen Sie die neuen Klassen.
4.  Fügen Sie die gewünschten Attribute den neuen Klassen hinzu.
5.  Aktualisieren Sie den Schema Cache erneut.

 

 




