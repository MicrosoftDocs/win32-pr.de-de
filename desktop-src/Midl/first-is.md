---
title: first_is-Attribut
description: Das Attribut \first \_ is\ gibt den Index des ersten zu übertragenden Arrayelements an.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is MIDL-Attribut
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d08be3ce14074c126a35272ede1b670121634f75d0b3d6cfb0db34e4f305760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067280"
---
# <a name="first_is-attribute"></a>first \_ is attribute

Das \[ **erste \_ is-Attribut** \] gibt den Index des ersten zu übertragenden Arrayelements an.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Gibt einen oder mehrere C-Sprachausdrücke an. Jeder Ausdruck wird zu einer ganzen Zahl ausgewertet, die den Arrayindex des ersten zu übertragenden Arrayelements darstellt. Der MIDL-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. MIDL lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement- und Dekrementoperatoren zu. Trennen Sie mehrere Ausdrücke durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn das **\[ erste Attribut \_ nicht \]** vorhanden ist oder der angegebene Index eine negative Zahl ist, ist das Arrayelement 0 das erste übertragene Element.

Das **\[ erste \_ \] is-Attribut** kann auch dabei helfen, die Werte der Arrayindizes zu bestimmen, die dem attribut last is oder length is entspricht, wenn diese Attribute nicht **\[** [**\_**](last-is.md) **\]** angegeben **\[** [**\_**](length-is.md) **\]** sind. Die Beziehung zwischen diesen Arrayindizes ist:

``` syntax
length = last - first + 1
```

Die folgende Beziehung muss auch Folgendes besitzen:

``` syntax
0 <= first_is <= max_is
```

Die folgende Beziehung muss halten, **\[** [**wenn max \_ <**](max-is.md) **\] = 0 ist:**

``` syntax
first_is == 0
```

Das **\[ erste \_ \] is-Attribut** kann nicht gleichzeitig mit dem Zeichenfolgenattribut **\[** [**verwendet**](string.md) **\]** werden.

Die Verwendung eines konstanten Ausdrucks **\[ mit dem ersten \_ is-Attribut \]** ist eine ungeeignete Verwendung des Attributs. Dies ist legal, aber ineffizient und führt zu einem langsameren Marshalling von Code.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[\_Feldattribute](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**last \_ is**](last-is.md)
</dt> <dt>

[**length \_ ist**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**min \_ is**](min-is.md)
</dt> <dt>

[**size \_ ist**](size-is.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> </dl>

 

 