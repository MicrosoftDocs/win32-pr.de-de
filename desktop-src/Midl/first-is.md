---
title: first_is-Attribut
description: Das Attribut \ First \_ is \ gibt den Index des ersten Array Elements an, das übertragen werden soll.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- First_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858253"
---
# <a name="first_is-attribute"></a>erstes \_ Attribut

Das \[ **erste \_ is** - \] Attribut gibt den Index des ersten Array Elements an, das übertragen werden soll.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*begrenzte Ausdrucks Liste* 
</dt> <dd>

Gibt einen oder mehrere C-sprach Ausdrücke an. Jeder Ausdruck ergibt eine ganze Zahl, die den Array Index des ersten zu übertragenden Array Elements darstellt. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu. Trennen Sie mehrere Ausdrücke durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das **\[ erste \_ Attribut \] ist** , das nicht vorhanden ist, oder wenn der angegebene Index eine negative Zahl ist, ist Array Element NULL das erste übertragene Element.

Das **\[ erste \_ ist \]** -Attribut kann auch helfen, die Werte der Array Indizes zu ermitteln, die dem **\[** [**letzten \_ is**](last-is.md) - **\]** oder length-Attribut entsprechen, **\[** [**\_**](length-is.md) **\]** Wenn diese Attribute nicht angegeben werden. Die Beziehung zwischen diesen Array Indizes lautet wie folgt:

``` syntax
length = last - first + 1
```

Die folgende Beziehung muss ebenfalls enthalten:

``` syntax
0 <= first_is <= max_is
```

Die folgende Beziehung muss enthalten sein, wenn **\[** Max **\] <= 0** [**\_ ist**](max-is.md) :

``` syntax
first_is == 0
```

Das **\[ erste \_ is \]** -Attribut kann nicht gleichzeitig mit dem **\[** [**String**](string.md) -Attribut verwendet werden **\]** .

Die Verwendung eines konstanten Ausdrucks mit dem **\[ ersten \_ is \]** -Attribut ist eine ungeeignete Verwendung des-Attributs. Dies ist zulässig, aber ineffizient und führt zu einem langsameren Marshallingcode.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Feld \_ Attribute](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Letzter \_ ist**](last-is.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
</dt> <dt>

[**Min \_ ist**](min-is.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> </dl>

 

 