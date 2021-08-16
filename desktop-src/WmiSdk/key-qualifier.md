---
description: Der Schlüsselqualifizierer gibt an, ob die Eigenschaft Teil des Namespacehandrs ist.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Schlüsselqualifizierer
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
ms.openlocfilehash: 9ae5525aa85ab744e7e6824bb6079511a3611643d53594503e70c8e587f363cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555890"
---
# <a name="key-qualifier"></a>Schlüsselqualifizierer

Der **Schlüsselqualifizierer** gibt an, ob die Eigenschaft Teil des Namespacehandrs ist. Wenn mehr als eine  Eigenschaft über den Schlüsselqualifizierer verfügt, bilden alle diese Eigenschaften zusammen den Schlüssel (einen Verbundschlüssel). Zusammen müssen die Schlüsseleigenschaften einen eindeutigen Verweis für jede Klasseninstanz liefern. Wenn dieser Qualifizierer für eine Eigenschaft platziert wird, ist nur der **Wert TRUE** zulässig.

Sie können einen beliebigen Eigenschaftentyp verwenden, mit Ausnahme der folgenden:

-   Arrays
-   Real- und Gleitkommazahlen
-   Eingebettete Objekte
-   Zeichen, die niedriger als ASCII 32 sind (d. h. Leerzeichen)
-   Zeichenfolgen vom Typ **char16** oder Zeichenfolgen, die als Schlüssel definiert sind, müssen Werte enthalten, die größer als U+0020 sind. Dies liegt daran, dass WMI Schlüsselwerte in Objektpfaden verwendet und Sie keine nicht druckenden Zeichen in einem Objektpfad verwenden können.

Wenn eine übergeordnete Klasse einen Schlüssel angibt, erben alle von der übergeordneten Klasse abgeleiteten Klassen diesen Schlüssel. Die abgeleiteten Klassen können den geerbten Schlüssel nicht ändern oder eine neue Schlüsseleigenschaft definieren. Wenn Sie jedoch eine Unterklasse von einer abstrakten Klasse ohne Schlüssel ableiten, können Sie einen Schlüssel in die Unterklasse einführen.

Alle Klassen, die mehr als eine Instanz definieren, müssen einen Schlüssel angeben. Da abstrakte Klassen keine Instanzen definieren, müssen sie keine Schlüssel angeben. Da Singletonklassen nur eine Instanz definieren, können sie keine Schlüssel angeben.

Schlüssel werden einmal bei der Objekt instanziierung geschrieben und dürfen später nicht mehr geändert werden. Es ist nicht sinnvoll, einen Standardwert auf eine schlüsselqualifizierte Eigenschaft anzuwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

 




