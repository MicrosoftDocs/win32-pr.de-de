---
description: Die OBJECTS-Klausel des NOTIFICATION-TYPE-Makros enumeriert den Satz von Objekten, die dem Benachrichtigungsobjekt zugeordnet sind.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: OBJECTS-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9289be0a3fa228e74a720ec385a5b13354f849710a88287a9911f470e40758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131042"
---
# <a name="objects-clause"></a>OBJECTS-Klausel

Die OBJECTS-Klausel des [NOTIFICATION-TYPE-Makros](notification-type-macro.md) enumeriert den Satz von Objekten, die dem Benachrichtigungsobjekt zugeordnet sind.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Die folgenden Regeln gelten für die Zuordnung zu CIM-Klassen:

-   Jeder Member der OBJECTS-Klausel wird einer Eigenschaft der CIM-Klassendefinition zu ordnet. Der Objektdeskriptor des -Members wird dem CIM-Eigenschaftennamen ausführlich zuordnt. IfIndex **wird z. B.** in **ifIndex übersetzt.**
-   Jede vom Zuordnungsprozess generierte CIM-Eigenschaft enthält den VarBindIndex-Qualifizierer. 

    **VarBindIndex ist** ein **obligatorischer uint32-Qualifizierer,** der die Position des Objekts beschreibt, wie sie in der [OBJECTS-Klausel des TRAP-TYPE-](trap-type-macro.md) oder [NOTIFICATION-TYPE-Makros angezeigt](notification-type-macro.md) wird. Die ganze Zahl gibt auch die Position der Eigenschaft an, wie sie in der Variablenbindungsliste von SNMPv1 bzw. SNMPv2C TRAP PDU (Protokolldateneinheit) angezeigt wird. (Da die ersten beiden Variablenbindungen immer TimeStamp und Identification sind, werden alle zusätzlichen Variablen nach dem Wert 2 nummeriert.)

    Wenn die CIM-Ereignisklasse aus einem [SNMPv1-TRAP-TYPE-Makro](trap-type-macro.md) generiert wird, hat der **VarBindIndex-Qualifizierer** den Anfangswert 1 für die erste Variable in der Variablenbindungsliste.

    Wenn die CIM-Ereignisklasse aus einem SNMPv2C [NOTIFICATION-TYPE-Makro](notification-type-macro.md) generiert wird, hat der **VarBindIndex-Qualifizierer** den Anfangswert 3 für die erste Variable in der Variablenbindungsliste.

Beim Zuordnen einer gekapselten CIM-Klasse wird jeder Member der OBJECTS-Klausel einer CIM-Eigenschaft zu, die den Namen, Typ und Wert des entsprechenden MIB-Objekts widerspiegelt. Die verwendeten Zuordnungsverfahren werden in den folgenden Themen angegeben:

-   [SYNTAX-Klausel](syntax-clause.md)
-   [TEXTUAL-CONVENTION-Makro](textual-convention-macro.md)
-   [ACCESS- und MAX-ACCESS-Klauseln](access-and-max-access-clauses.md)

Bei Verwendung einer REFERENZ-CIM-Klasse wird jeder Member der OBJECTS-Klausel wie folgt zueinander zuordnungen:

-   Jeder Member der OBJECTS-Klausel wird einer einzelnen Eigenschaft der CIM-Klasse zuordnungen. Die -Eigenschaft ist stark als eingebettetes Objekt typiert.
-   Die Klasse des eingebetteten Objekts wird über die Standardmäßige Objektzuordnungsprozedur generiert. Weitere Informationen finden Sie unter [OBJECT-TYPE-Makro](object-type-macro.md). Beispielsweise wird **ifTable** einer eingebetteten Klasse mit dem Namen **SNMP \_ RFC1213 \_ MIB \_ ifTable zu.**
-   Die Werte, die den Variablenbindungen eines TRAP-PDU zugeordnet sind, werden als eingebettete Objekte eines Objekts der Referenzklasse instanziiert. Jedes eingebettete Objekt enthält Werte für jede der schlüsselierten Eigenschaften des Objekts und den Wert der Eigenschaft in der variablen Bindung, die zugeordnet wird.

 

 



