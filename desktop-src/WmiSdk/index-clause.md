---
description: Gibt einen Schlüssel zum Auswählen einer eindeutigen Zeile in einer Skalar- oder Tabellensammlung an.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: INDEX-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca4478164839412238f59d9771aa9c96417c4055390cb4599edbb40b0e6b4a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318742"
---
# <a name="index-clause"></a>INDEX-Klausel

Die INDEX-Klausel gibt einen Schlüssel zum Auswählen einer eindeutigen Zeile in einer Skalar- oder Tabellensammlung an. Der SNMP-Anbieter wird abhängig vom Typ der Tabelle, die das SNMP-Gerät verwendet, einem anderen Typ von CIM-Klasse zu. Da ein Schlüssel mehrere Objekttypen haben kann, verwendet der Anbieter je nach Objekttyp innerhalb des Schlüssels unterschiedliche Zuordnungsregeln. Weitere Informationen finden Sie unter [INDEX-Klauseldatentypen](#index-clause-data-types).

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Eine skalare Auflistung wird einer CIM-Singletonklasse(n) zu einer Klasse, die nur eine Instanz haben kann. Da es nicht notwendig ist, eine Instanz eindeutig von einer anderen zu identifizieren, bestimmt eine Singletonklasse keine oder mehrere Eigenschaften als Schlüssel. Aus skalaren Auflistungen generierte Klassen:

-   Enthalten keine  Schlüsseleigenschaftsqualifizierer.
-   Enthalten Sie den STANDARDMÄßIGEN CIM-Klassenqualifizierer **Singleton** vom Typ **Bool.**

Eine Tabellensammlung wird einer CIM-Klasse mit mehr als einer Instanz angezeigt. Daher muss die CIM-Klassendefinition mindestens eine Eigenschaft enthalten, die den Objektschlüssel definiert. das heißt, eine Eigenschaft, die eine Instanz der -Klasse eindeutig identifiziert. Die INDEX-Klausel des [OBJECT-TYPE-Makros](object-type-macro.md) einer Tabellensammlung gibt den Satz von Schlüsseleigenschaften der Auflistung an. Es gelten die folgenden Zuordnungsregeln:

-   Der **CIM-Qualifiziererschlüssel**, typ **Bool**, definiert eine Schlüsseleigenschaft.
-   Die Reihenfolge der INDEX-Informationen in der Tabellensammlung definiert die Reihenfolge der Schlüssel innerhalb der CIM-Klassendefinition.

    Die Schlüssel reihenfolge des **\_ CIM-Qualifizierers** definiert die Reihenfolge der Schlüssel. Dieser Qualifizierer ist ein 32-Bit-Ganzzahlwert ohne Vorzeichen, der im Rahmen der MOF-Qualifizierersyntax mithilfe des Twos-Complement-Vorgangs in einen ganzzahligen 32-Bit-Wert mit Vorzeichen konvertiert werden muss.

Die Zuordnung der SNMPv2C INDEX-Klausel behandelt derzeit  nicht die Verwendung des IMPLIED-Qualifizierers. In diesem Fall wird keine CIM-Klassendefinition generiert.

## <a name="index-clause-data-types"></a>INDEX-Klauseldatentypen

Aufgrund der Flexibilität der INDEX-Klausel innerhalb des [OBJECT-TYPE-Makros](object-type-macro.md) ist die Angabe von schlüsselierten Eigenschaften nicht einfach. Stattdessen sollten Sie die Möglichkeiten berücksichtigen, dass die INDEX-Klausel einen oder mehrere der folgenden Datentypen enthalten kann:

-   Intern zugänglicher **Indexobjektwert**

    Der **indexobject-Wert** ist ein benannter Wert, der auf eine MIB-Objektdefinition verweist, die in der konzeptionellen Zeile derselben Tabelle angezeigt wird, die die INDEX-Klausel enthält. Die MIB-Objektdefinition, auf die in der INDEX-Klausel verwiesen wird, wird einer Schlüsseleigenschaft der CIM-Klassendefinition zu.

-   Extern zugänglicher **Indexobjektwert**

    In diesem Fall ist **indexobject** ein benannter Wert, der auf eine MIB-Objektdefinition verweist, die in der konzeptionellen Zeile einer anderen Tabelle angezeigt wird.

-   Barrierefreier **Indextypwert**

    Der **Indextypwert** ist ein benannter Typ, der auf einen der folgenden Datentypen verweist: **INTEGER,** **OCTET STRING,** **OBJECT IDENTIFIER,** **NetworkAddress** oder **IpAddress**. Wenn die INDEX-Klausel einen MIB-Typverweis enthält, gelten die folgenden Zuordnungsregeln:

    -   Das MIB-Objekt, auf das verwiesen wird, ist einer Schlüsseleigenschaft der CIM-Klassendefinition zuordnungsbegrenzt. Die Typsyntax basiert auf dem angegebenen **Indextypwert,** der CIM-Eigenschaftenqualifizierern mithilfe der standardmäßigen SYNTAX-Klauselzuordnungs-Prozeduren entspricht. [](syntax-clause.md)
    -   Der Zuordnungsprozess generiert einen eindeutigen Eigenschaftennamen durch Verkettung des MIB-Tabellenobjektdeskriptors, eines Unterstrichs ( ) und der Rangfolge des Indextypwerts der \_ INDEX-Klausel.  Beispielsweise ist der Eigenschaftenname für  den Indextyp der dritten Komponente der MIB-Tabelle **enterpriseIfTable** **enterpriseIfTable \_ 3.**
    -   Die CIM-Eigenschaft wird mit dem Qualifizierer **\_ für virtuelle** Schlüssel kommentiert. Dieser Qualifizierer gibt an, dass der SNMP-Anbieter den Wert der Eigenschaft basierend auf der Obermenge der Instanzinformationen berechnen soll, die allen zugänglichen MIB-Objektdefinitionen in der Klassendefinition zugeordnet sind.
    -   Die CIM-Klassendefinition muss mindestens eine Eigenschaft enthalten, die nicht über einen zugeordneten Qualifizierer für virtuelle Schlüssel verfügt. Wenn diese Eigenschaft nicht angegeben wird, wird die Klassendefinition ungültig. **\_**

-   Untertyp mit fester Länge

    Wenn die INDEX-Klausel einer SNMP-Tabellensammlung einen SNMP-unterstützten Typ enthält, der als OCTET STRING fester Länge untertypisiert ist, muss der CIM-Eigenschaftenqualifizierer **Feste \_** Länge verwendet werden, um diesen Wert anzugeben.

 

 



