---
description: Der Schlüssel Qualifizierer gibt an, ob die Eigenschaft Teil des Namespace Handles ist.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Schlüssel Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758323"
---
# <a name="key-qualifier"></a>Schlüssel Qualifizierer

Der **Schlüssel** Qualifizierer gibt an, ob die Eigenschaft Teil des Namespace Handles ist. Wenn mehr als eine Eigenschaft den **Schlüssel** Qualifizierer aufweist, bilden alle diese Eigenschaften zusammen den Schlüssel (einen Verbund Schlüssel). Bei gemeinsamer Erstellung müssen die Schlüsseleigenschaften einen eindeutigen Verweis für jede Klasseninstanz angeben. Wenn dieser Qualifizierer für eine Eigenschaft platziert wird, ist nur der Wert **true** zulässig.

Sie können einen beliebigen Eigenschaftentyp verwenden, mit Ausnahme der folgenden:

-   Arrays
-   Real-und Gleit Komma Zahlen
-   Eingebettete Objekte
-   Zeichen niedriger als ASCII 32 (d. h. Leerzeichen)
-   Zeichen folgen vom Typ **char16** oder Zeichen folgen, die als Schlüssel definiert sind, müssen Werte größer als U + 0020 enthalten. Dies liegt daran, dass WMI Schlüsselwerte in Objekt Pfaden verwendet und Sie keine nicht druckbaren Zeichen in einem Objekt Pfad verwenden können.

Wenn eine übergeordnete Klasse einen Schlüssel angibt, erben alle Klassen, die von der übergeordneten Klasse abgeleitet sind, diesen Schlüssel. Die abgeleiteten Klassen können den geerbten Schlüssel nicht ändern oder eine neue Schlüsseleigenschaft definieren. Wenn Sie jedoch eine Unterklasse von einer abstrakten Klasse ohne einen Schlüssel ableiten, können Sie einen Schlüssel in der Unterklasse einfügen.

Alle Klassen, die mehr als eine Instanz definieren, müssen einen Schlüssel angeben. Da abstrakte Klassen keine-Instanzen definieren, müssen Sie keine Schlüssel angeben. Da Singleton-Klassen nur eine Instanz definieren, können Sie keine Schlüssel angeben.

Schlüssel werden bei der Objekt Instanziierung einmal geschrieben und dürfen nicht später geändert werden. Es ist nicht sinnvoll, einen Standardwert auf eine Schlüssel qualifizierte Eigenschaft anzuwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

 




