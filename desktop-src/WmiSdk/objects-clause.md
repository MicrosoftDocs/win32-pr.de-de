---
description: Die Objects-Klausel des Notification-Type-Makros listet den Satz von-Objekten auf, die dem Benachrichtigungs Objekt zugeordnet sind.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: Objects-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e25848e0fc98ca79ef96e25423ba7872296e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214365"
---
# <a name="objects-clause"></a>Objects-Klausel

Die Objects-Klausel des [Notification-Type-](notification-type-macro.md) Makros listet den Satz von-Objekten auf, die dem Benachrichtigungs Objekt zugeordnet sind.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Die folgenden Regeln gelten für die Zuordnung zu CIM-Klassen:

-   Jeder Member der Objects-Klausel wird einer Eigenschaft der CIM-Klassendefinition zugeordnet. Der Objekt Deskriptor des Elements wird dem CIM-Eigenschaftsnamen wörtlich zugeordnet. **Ifindex** beispielsweise wird in **ifindex** übersetzt.
-   Jede vom Mapping-Prozess generierte CIM-Eigenschaft enthält den **varbindindex** -Qualifizierer.

    **Varbindindex** ist ein **UInt32** obligatorischer Qualifizierer, der die Position des Objekts beschreibt, wie er in der Objects [-Klausel des Trap-Type-](trap-type-macro.md) oder [Notification-Type](notification-type-macro.md) -Makros angezeigt wird. Die Ganzzahl gibt auch die Position der Eigenschaft an, wie Sie in der Variablen Bindungs Liste von SNMPv1 bzw. SNMPv2C Trap PDU (Protokolldaten Einheit) angezeigt wird. (Da die ersten beiden Variablen Bindungen immer timestamp und Identification sind, werden alle zusätzlichen Variablen nach dem Wert 2 nummeriert.)

    Wenn die CIM-Ereignisklasse aus einem SNMPv1 [Trap-Type-](trap-type-macro.md) Makro generiert wird, hat der **varbindindex** -Qualifizierer den Anfangswert 1 für die erste Variable in der Variablen Bindungs Liste.

    Wenn die CIM-Ereignisklasse aus einem SNMPv2C [-Benachrichtigungstyp-](notification-type-macro.md) Makro generiert wird, hat der **varbindindex** -Qualifizierer für die erste Variable in der Liste der Variablen Bindungen den Anfangswert 3.

Beim Zuordnen einer gekapselten CIM-Klasse wird jeder Member der Objects-Klausel einer CIM-Eigenschaft zugeordnet, die den Namen, den Typ und den Wert des entsprechenden MIB-Objekts widerspiegelt. Die verwendeten Mapping-Prozeduren werden in den folgenden Themen angegeben:

-   [Syntax Klausel](syntax-clause.md)
-   [Text Konvention-Makro](textual-convention-macro.md)
-   [Access-und Max-Access-Klauseln](access-and-max-access-clauses.md)

Wenn Sie eine Referent-CIM-Klasse verwenden, wird jedes Element der Objects-Klausel wie folgt zugeordnet:

-   Jeder Member der Objects-Klausel wird einer einzelnen Eigenschaft der CIM-Klasse zugeordnet. Die-Eigenschaft ist stark typisiert als eingebettetes Objekt.
-   Die Klasse des eingebetteten Objekts wird durch die standardmäßige Objekt zuordnungsprozedur generiert. Weitere Informationen finden Sie unter [Object-Type-Makro](object-type-macro.md). Beispielsweise ist **iftable** einer eingebetteten Klasse mit dem Namen **SNMP \_ RFC1213 \_ MIB \_ iftable** zugeordnet.
-   Die Werte, die den Variablen Bindungen eines Trap-PDU zugeordnet sind, werden als eingebettete Objekte eines Objekts der Referent-Klasse instanziiert. Jedes eingebettete Objekt enthält Werte für jede der Schlüssel gebundenen Eigenschaften des Objekts und den Wert der-Eigenschaft in der Variablen Bindung, die zugeordnet wird.

 

 



