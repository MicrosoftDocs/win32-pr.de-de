---
description: Gibt einen Schlüssel an, um eine eindeutige Zeile in einer skalaren oder Tabellen Auflistung auszuwählen.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: Index-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 915cbe1c4bf1da5ccd7fbab881770722b70bc53c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131921"
---
# <a name="index-clause"></a>Index-Klausel

Die Index-Klausel gibt einen Schlüssel an, um eine eindeutige Zeile in einer skalaren oder Tabellen Auflistung auszuwählen. Der SNMP-Anbieter ist abhängig vom Typ der vom SNMP-Gerät verwendeten Tabelle einem anderen Typ von CIM-Klasse zugeordnet. Da ein Schlüssel mehr als einen Objekttyp aufweisen kann, verwendet der Anbieter je nach Objekttyp innerhalb des Schlüssels andere Zuordnungsregeln. Weitere Informationen finden Sie unter [Index-klauseldatentypen](#index-clause-data-types).

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Eine skalare Auflistung wird einer CIM-Singleton-Klasse zugeordnet, d. h. eine Klasse, die nur eine Instanz aufweisen kann. Da es nicht erforderlich ist, eine Instanz von einer anderen eindeutig zu identifizieren, bestimmt eine Singleton-Klasse nicht eine oder mehrere Eigenschaften als Schlüssel. Aus skalaren Auflistungen generierte Klassen:

-   Keine **Schlüssel** Eigenschaften Qualifizierer enthalten.
-   Enthalten den Standard-CIM-klassenqualifizierungssingleton, der vom Typ " **bool**" ist. 

Eine Tabellen Auflistung wird einer CIM-Klasse zugeordnet, die mehr als eine Instanz aufweisen kann. Folglich muss die CIM-Klassendefinition mindestens eine Eigenschaft enthalten, die den Objekt Schlüssel definiert. Das heißt, eine Eigenschaft, die eine Instanz der Klasse eindeutig identifiziert. Die Index-Klausel des [ObjektType-](object-type-macro.md) Makros einer Tabellen Auflistung gibt den Satz von Schlüsseleigenschaften der Sammlung an. Die folgenden Zuordnungsregeln gelten:

-   Der CIM- **qualifiziererschlüssel**, Typ **bool**, definiert eine Schlüsseleigenschaft.
-   Die Reihenfolge der Index Informationen in der Tabellen Auflistung definiert die Reihenfolge der Schlüssel in der CIM-Klassendefinition.

    Die **Schlüssel \_ Reihenfolge** des CIM-Qualifizierers definiert die Reihenfolge der Schlüssel. Dieser Qualifizierer ist ein ganzzahliger 32-Bit-Wert ohne Vorzeichen, der zum Zwecke der MOF-qualifizierersyntax in 32 einen ganzzahligen Wert mit Vorzeichen mit Vorzeichen mit dem Twos-Komplement-Vorgang konvertiert werden muss.

Derzeit wird die Verwendung des **impliziten** Qualifizierers nicht durch die Zuordnung der SNMPv2C Index-Klausel behandelt. In diesem Fall wird keine CIM-Klassendefinition generiert.

## <a name="index-clause-data-types"></a>Datentypen der Index-Klausel

Aufgrund der Flexibilität der Index-Klausel im [Objekttyp-](object-type-macro.md) Makro ist die Angabe von Schlüssel gebundenen Eigenschaften nicht ganz einfach. Berücksichtigen Sie stattdessen die Möglichkeiten, dass die Index-Klausel einen oder mehrere der folgenden Datentypen enthalten kann:

-   Intern zugänglicher **indexobject** -Wert

    Der **indexobject** -Wert ist ein benannter Wert, der sich auf eine MIB-Objektdefinition bezieht, die in der konzeptionellen Zeile der gleichen Tabelle angezeigt wird, die die Index-Klausel enthält. Die MIB-Objektdefinition, auf die in der Index-Klausel verwiesen wird, wird einer Schlüsseleigenschaft der CIM-Klassendefinition zugeordnet.

-   Extern zugänglicher **indexobject** -Wert

    In diesem Fall ist **indexobject** ein benannter Wert, der auf eine MIB-Objektdefinition verweist, die in der konzeptionellen Zeile einer anderen Tabelle angezeigt wird.

-   Zugänglicher **IndexType** -Wert

    Der **IndexType** -Wert ist ein benannter Typ, der auf einen der folgenden Datentypen verweist: **ganze** Zahl, **Oktett-Zeichenfolge**, **Objekt Bezeichner**, **Network Address** oder **IPAddress**. Wenn die Index-Klausel einen MIB-Typverweis enthält, gelten die folgenden Zuordnungsregeln:

    -   Das MIB-Objekt, auf das verwiesen wird, ist einer Schlüsseleigenschaft der CIM-Klassendefinition zugeordnet. Die Typsyntax basiert auf dem angegebenen **IndexType** -Wert, der CIM-Eigenschafts Qualifizierern mithilfe der [Standardsyntax-Klauseln](syntax-clause.md) Zuordnungs Prozeduren zugeordnet wird.
    -   Der Zuordnungs Prozess generiert einen eindeutigen Eigenschaftsnamen, indem der MIB-Tabellenobjekt Deskriptor, ein Unterstrich ( \_ ) und die Rang Reihenfolge des **IndexType** -Werts der Index Klausel verkettet werden. Beispielsweise ist der Eigenschaftsname für den dritten **komponentenindextype** der MIB-Tabelle **enterpriseiftable** auf **enterpriseiftable \_ 3** festgelegt.
    -   Die CIM-Eigenschaft wird mit dem Qualifizierer des **virtuellen \_ Schlüssels** kommentiert. Dieser Qualifizierer gibt an, dass der SNMP-Anbieter den Wert der-Eigenschaft basierend auf der supermenge der Instanzinformationen berechnen soll, die allen zugreif baren MIB-Objekt Definitionen in der Klassendefinition zugeordnet sind.
    -   Die CIM-Klassendefinition muss mindestens eine Eigenschaft enthalten, die über keinen zugeordneten **virtuellen \_ Schlüssel** Qualifizierer verfügt. Wenn Sie diese Eigenschaft nicht angeben, wird die Klassendefinition ungültig.

-   Untertyp mit fester Länge

    Wenn die Index-Klausel einer SNMP-Tabellen Auflistung einen von SNMP unterstützten Typ enthält, der als Oktett-Zeichenfolge mit fester Länge subtypisiert ist **, \_ muss die** Eigenschaft Qualifizierer des CIM-Eigenschaften Qualifizierers zum Angeben dieses Werts verwendet werden.

 

 



