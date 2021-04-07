---
title: Schema Implementierung
description: In Active Directory Domain Services werden Klassen-und Attribut Definitionen im Verzeichnis als Instanzen der Klassen Schema und attributeSchema gespeichert.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ff18046841b5603be235266e33a7252049f93c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038734"
---
# <a name="schema-implementation"></a>Schema Implementierung

In Active Directory Domain Services werden Klassen-und Attribut Definitionen im Verzeichnis als Instanzen der Klassen [**Schema**](/windows/desktop/ADSchema/c-classschema) und [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) gespeichert. **classSchema** und **attributeSchema** sind Klassen, die im Schema definiert sind. Um das Active Directory Schema zu bearbeiten, verwenden Sie die gleichen LDAP-Vorgänge, die zum Bearbeiten anderer Objekte verwendet werden. Da es sich bei dem Schema um einen Schlüsselteil des Verzeichnisses handelt, der sich auf die gesamte Gesamtstruktur auswirkt, gelten spezielle Einschränkungen für Schema Erweiterungen. Weitere Informationen zu Einschränkungen finden Sie unter [Einschränkungen für Schema Erweiterungen](restrictions-on-schema-extension.md).

Zusammenfassen der Schema Implementierung:

-   Instanzen der [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Klasse definieren jede Objektklasse, die von Active Directory Domain Services unterstützt wird. Die Attribute eines **classSchema** -Objekts, z. b. die Attribute " [**mayare**](/windows/desktop/ADSchema/a-maycontain) " und " [**mustattribute**](/windows/desktop/ADSchema/a-mustcontain) ", beschreiben eine Objektklasse, wie die Attribute eines Benutzer Objekts, z. b. die Attribute " [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) " und " [**telefonienumber**](/windows/desktop/ADSchema/a-telephonenumber) ", den Benutzer beschreiben. Weitere Informationen finden Sie unter [Eigenschaften von Objektklassen](characteristics-of-object-classes.md).
-   Instanzen der [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Klasse werden verwendet, um alle Attribute zu definieren, die von Active Directory Domain Services unterstützt werden. Die Attribute eines **attributeSchema** -Objekts, z. b. die Attribute **attributeSyntax** und **issinglewert,** beschreiben ein Attribut, und zwar auf dieselbe Weise, wie die Attribute eines Benutzer Objekts diesen Benutzer beschreiben. Weitere Informationen finden Sie unter [Merkmale von Attributen](characteristics-of-attributes.md).
-   Instanzen der [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Klasse und der [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Klasse werden an einem bekannten Ort im Verzeichnis, dem Schema Container, gespeichert. Der Schema Container hat immer einen Distinguished Name in der Form:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    dabei &lt; ist "DC = forestroot &gt; " der Distinguished Name des Stamms der Gesamtstruktur, z. b. "DC = fabrikam, DC = com".

    Um den Distinguished Name des Schema Containers zu erhalten, lesen Sie das **schemaNamingContext** -Attribut von RootDSE. Weitere Informationen zu RootDSE und den zugehörigen Attributen finden Sie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md).

Beachten Sie Folgendes, wenn Sie über das Schema nachdenken:

-   Schema Änderungen sind Global. Es gibt ein einzelnes Schema für eine gesamte Gesamtstruktur. Das Schema wird Global repliziert: eine Kopie des Schemas ist auf jedem Domänen Controller in der Gesamtstruktur vorhanden. Wenn Sie das Schema erweitern, tun Sie dies für die gesamte Gesamtstruktur.
-   Schema Erweiterungen können nicht rückgängig gemacht werden. Wenn dem Schema eine neue Klasse oder ein neues Attribut hinzugefügt wird, kann es nicht entfernt werden. Ein vorhandenes Attribut oder eine vorhandene Klasse kann deaktiviert, aber nicht entfernt werden. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute](disabling-existing-classes-and-attributes.md).
-   Das Deaktivieren einer Klasse oder eines Attributs wirkt sich nicht auf vorhandene Instanzen der Klasse oder des Attributs aus, verhindert jedoch, dass neue Instanzen erstellt werden. Ein Attribut kann nicht deaktiviert werden, wenn es in einer Klasse enthalten ist, die nicht deaktiviert ist.

 

 