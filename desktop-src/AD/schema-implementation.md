---
title: Schemaimplementierung
description: In Active Directory Domain Services werden Klassen- und Attributdefinitionen im Verzeichnis als Instanzen der Klassen classSchema bzw. attributeSchema gespeichert.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d35d29b4e10d27b1369c0f064e17a0ed4430cbe2d6cc59329380724cd444e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025018"
---
# <a name="schema-implementation"></a>Schemaimplementierung

In Active Directory Domain Services werden Klassen- und Attributdefinitionen im Verzeichnis als Instanzen der [**Klassen classSchema**](/windows/desktop/ADSchema/c-classschema) bzw. [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) gespeichert. **classSchema** und **attributeSchema** sind Klassen, die im Schema definiert sind. Um das Active Directory-Schema zu bearbeiten, verwenden Sie dieselben LDAP-Vorgänge, die zum Bearbeiten anderer Objekte verwendet werden. Da das Schema ein wichtiger Teil des Verzeichnisses ist, der die gesamte Gesamtstruktur betrifft, gelten besondere Einschränkungen für Schemaerweiterungen. Weitere Informationen zu Einschränkungen finden Sie unter [Einschränkungen für Schemaerweiterungen.](restrictions-on-schema-extension.md)

So fassen Sie die Schemaimplementierung zusammen:

-   Instanzen der [**classSchema-Klasse**](/windows/desktop/ADSchema/c-classschema) definieren jede Objektklasse, die von Active Directory Domain Services. Die Attribute eines **classSchema-Objekts,** z. B. die [**attribute mayContain**](/windows/desktop/ADSchema/a-maycontain) und [**mustContain,**](/windows/desktop/ADSchema/a-mustcontain) beschreiben eine Objektklasse auf die gleiche Weise wie die Attribute eines Benutzerobjekts, z. B. dessen [**UserPrincipalName-**](/windows/desktop/ADSchema/a-userprincipalname) und [**telephoneNumber-Attribute,**](/windows/desktop/ADSchema/a-telephonenumber) diesen Benutzer. Weitere Informationen finden Sie unter [Merkmale von Objektklassen.](characteristics-of-object-classes.md)
-   Instanzen der [**attributeSchema-Klasse**](/windows/desktop/ADSchema/c-attributeschema) werden verwendet, um jedes Attribut zu definieren, das von Active Directory Domain Services. Die Attribute eines **attributeSchema-Objekts,** z. B. seine **attributeSyntax-** und **isSingleValued-Attribute,** beschreiben ein Attribut auf die gleiche Weise, wie die Attribute eines Benutzerobjekts diesen Benutzer beschreiben. Weitere Informationen finden Sie unter [Merkmale von Attributen.](characteristics-of-attributes.md)
-   Instanzen der [**Klassen attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) und [**classSchema**](/windows/desktop/ADSchema/c-classschema) werden an einem bekannten Ort im Verzeichnis gespeichert, dem Schemacontainer. Der Schemacontainer hat immer einen Distinguished Name der Form:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    Wobei " DC=forestroot " der Distinguished Name des Stamms der Gesamtstruktur ist, z. B. &lt; &gt; "DC=Fabrikam,DC=Com".

    Um den Distinguished Name des Schemacontainers zu erhalten, lesen Sie **das schemaNamingContext-Attribut** von rootDSE. Weitere Informationen zu rootDSE und seinen Attributen finden Sie unter [Serverlose Bindung und RootDSE](serverless-binding-and-rootdse.md).

Denken Sie beim Überlegen des Schemas an:

-   Schemaänderungen sind global. Es gibt ein einzelnes Schema für eine gesamte Gesamtstruktur. Das Schema wird global repliziert: Auf jedem Domänencontroller in der Gesamtstruktur ist eine Kopie des Schemas vorhanden. Wenn Sie das Schema erweitern, tun Sie dies für die gesamte Gesamtstruktur.
-   Schemaerweiterungen sind nicht umkehrbar. Wenn dem Schema eine neue Klasse oder ein neues Attribut hinzugefügt wird, kann sie nicht entfernt werden. Ein vorhandenes Attribut oder eine vorhandene Klasse kann deaktiviert, aber nicht entfernt werden. Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute.](disabling-existing-classes-and-attributes.md)
-   Das Deaktivieren einer Klasse oder eines Attributs wirkt sich nicht auf vorhandene Instanzen der Klasse oder des Attributs aus, verhindert jedoch, dass neue Instanzen erstellt werden. Sie können ein Attribut nicht deaktivieren, wenn es in einer Klasse enthalten ist, die nicht deaktiviert ist.

 

 