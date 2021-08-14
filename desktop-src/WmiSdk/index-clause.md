---
description: Gibt einen Schlüssel zum Auswählen einer eindeutigen Zeile in einer Skalar- oder Tabellenauflistung an.
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

Die INDEX-Klausel gibt einen Schlüssel zum Auswählen einer eindeutigen Zeile in einer Skalar- oder Tabellenauflistung an. Der SNMP-Anbieter wird je nach Typ der vom SNMP-Gerät verwendeten Tabelle einem anderen Cim-Klassentyp zugeordnet. Da ein Schlüssel mehrere Objekttypen aufweisen kann, verwendet der Anbieter je nach Objekttyp innerhalb des Schlüssels unterschiedliche Zuordnungsregeln. Weitere Informationen finden Sie unter [INDEX-Klauseldatentypen.](#index-clause-data-types)

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Eine skalare Auflistung wird einer CIM-Singletonklasse zugeordnet, d.h. einer Klasse, die nur eine Instanz haben kann. Da eine Instanz nicht eindeutig von einer anderen identifiziert werden muss, legt eine Singletonklasse keine oder mehrere Eigenschaften als Schlüssel fest. Aus skalaren Auflistungen generierte Klassen:

-   Sie dürfen keine Key-Eigenschaftsqualifizierer enthalten. 
-   Enthalten Sie den CIM-Standardklassenqualifizierer **Singleton**, der vom Typ **Bool** ist.

Eine Tabellenauflistung wird einer CIM-Klasse zugeordnet, die über mehrere Instanzen verfügen kann. Daher muss die CIM-Klassendefinition mindestens eine Eigenschaft enthalten, die den Objektschlüssel definiert. Das heißt, eine Eigenschaft, die eine Instanz der -Klasse eindeutig identifiziert. Die [INDEX-Klausel des OBJECT-TYPE-Makros](object-type-macro.md) einer Tabellenauflistung gibt den Satz von Schlüsseleigenschaften der Sammlung an. Es gelten die folgenden Zuordnungsregeln:

-   Der CIM-Qualifiziererschlüssel , Typ **Bool,** definiert eine Schlüsseleigenschaft. 
-   Die Reihenfolge der INDEX-Informationen in der Tabellenauflistung definiert die Reihenfolge der Schlüssel in der CIM-Klassendefinition.

    Die **\_ Schlüsselreihenfolge** des CIM-Qualifizierers definiert die Reihenfolge der Schlüssel. Dieser Qualifizierer ist ein ganzzahliger 32-Bit-Wert ohne Vorzeichen, der für die MOF-Qualifizierersyntax mithilfe des Twos-Complement-Vorgangs in einen 32-Bit-Ganzzahlwert mit Vorzeichen konvertiert werden muss.

Derzeit verarbeitet die Zuordnung der SNMPv2C INDEX-Klausel  nicht die Verwendung des IMPLIED-Qualifizierers. In diesem Fall wird keine CIM-Klassendefinition generiert.

## <a name="index-clause-data-types"></a>Datentypen der INDEX-Klausel

Aufgrund der Flexibilität der INDEX-Klausel innerhalb des [OBJECT-TYPE-Makros](object-type-macro.md) ist die Spezifikation von schlüsselbasierten Eigenschaften nicht einfach. Stattdessen sollten Sie die Möglichkeiten berücksichtigen, dass die INDEX-Klausel einen oder mehrere der folgenden Datentypen enthalten kann:

-   Intern zugänglicher **Indexobject-Wert**

    Der **indexobject-Wert** ist ein benannter Wert, der auf eine MIB-Objektdefinition verweist, die in der konzeptionellen Zeile derselben Tabelle angezeigt wird, die die INDEX-Klausel enthält. Die MIB-Objektdefinition, auf die in der INDEX-Klausel verwiesen wird, wird einer Schlüsseleigenschaft der CIM-Klassendefinition zugeordnet.

-   Extern zugänglicher **Indexobject-Wert**

    In diesem Fall ist **indexobject** ein benannter Wert, der auf eine MIB-Objektdefinition verweist, die in der konzeptionellen Zeile einer anderen Tabelle angezeigt wird.

-   Zugänglicher **Indextypwert**

    Der **Indextypwert** ist ein benannter Typ, der auf einen der folgenden Datentypen verweist: **INTEGER,** **OCTET STRING,** **OBJECT IDENTIFIER,** **NetworkAddress** oder **IpAddress**. Wenn die INDEX-Klausel einen MIB-Typverweis enthält, gelten die folgenden Zuordnungsregeln:

    -   Das MIB-Objekt, auf das verwiesen wird, wird einer Schlüsseleigenschaft der CIM-Klassendefinition zugeordnet. Die Typsyntax basiert auf dem angegebenen **Indextypwert,** der CIM-Eigenschaftsqualifizierern mithilfe der [standardmäßigen SYNTAX-Klauselzuordnungsprozessen](syntax-clause.md) zugeordnet wird.
    -   Der Zuordnungsprozess generiert einen eindeutigen Eigenschaftennamen, indem der MIB-Tabellenobjektdeskriptor, ein Unterstrich ( \_ ) und die Rangfolge des **Indextypwerts** der INDEX-Klausel verkettet werden. Der Eigenschaftenname für den **Indextyp** der dritten Komponente der MIB-Tabelle **enterpriseIfTable** lautet beispielsweise **enterpriseIfTable \_ 3.**
    -   Die CIM-Eigenschaft wird mit dem **Virtual Key-Qualifizierer \_** versehen. Dieser Qualifizierer gibt an, dass der SNMP-Anbieter den Wert der Eigenschaft basierend auf der Obermenge der Instanzinformationen berechnen soll, die allen barrierefreien MIB-Objektdefinitionen in der Klassendefinition zugeordnet sind.
    -   Die CIM-Klassendefinition muss mindestens eine Eigenschaft enthalten, der kein **virtueller \_ Schlüsselqualifizierer** zugeordnet ist. Wenn diese Eigenschaft nicht angegeben wird, wird die Klassendefinition ungültig.

-   Untertyp mit fester Länge

    Wenn die INDEX-Klausel einer SNMP-Tabellenauflistung einen SNMP-unterstützten Typ enthält, der als OCTET STRING mit fester Länge subtypisiert ist, muss der CIM-Eigenschaftsqualifizierer **Fixed \_ Length** verwendet werden, um diesen Wert anzugeben.

 

 



