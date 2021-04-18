---
title: last_is-Attribut
description: Das Feld Attribut \ letzter \_ ist \ gibt den Index des letzten Array Elements an, das übertragen werden soll. Wenn der angegebene Index 0 (null) oder negativ ist, werden keine Array Elemente übertragen.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- Last_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516775"
---
# <a name="last_is-attribute"></a>Letztes \_ ist Attribut

Das Feld Attribut **\[ Last \_ \]** gibt den Index des letzten Array Elements an, das übertragen werden soll. Wenn der angegebene Index 0 (null) oder negativ ist, werden keine Array Elemente übertragen.

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*begrenzte Ausdrucks Liste* 
</dt> <dd>

Gibt einen oder mehrere C-sprach Ausdrücke an. Jeder Ausdruck ergibt eine ganze Zahl, die den Array Index des letzten zu übertragenden Array Elements darstellt. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu. Trennen Sie mehrere Ausdrücke durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Letzte \_ is \]** -Attribut bestimmt den Wert des Array Indexes, der der **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** Länge ist Attribute entspricht, wenn length nicht angegeben ist. Die Beziehung zwischen diesen Array Indizes lautet wie folgt: length = Last-First + 1.

Wenn der Wert des Array Indexes, der durch **\[** [**First \_**](first-is.md) angegeben wird **\]** , größer ist als der Wert, der durch den **\[ letzten \_ \]** Wert angegeben ist, werden keine Elemente übertragen.

Das **\[ Letzte \_ is \]** -Attribut kann nicht als Feld Attribut gleichzeitig verwendet werden, wenn die **\[** [**Länge \_**](length-is.md) **\]** Attribute oder das **\[** [**Zeichen**](string.md) folgen **\]** Attribut ist.

Die Verwendung eines konstanten Ausdrucks mit dem **\[ letzten \_ is \]** -Attribut ist eine ungeeignete Verwendung des-Attributs. Dies ist zulässig, aber ineffizient und führt zu einem langsameren Marshallingcode.

Wenn der durch Max angegebene Wert **\[** [**\_**](max-is.md) **\]** gleich oder größer als 0 (null) ist, muss die folgende Beziehung True lauten: 0 <= Last \_ is <= Max \_ ist.

## <a name="examples"></a>Beispiele

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Feldattribute](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**der erste \_ ist**](first-is.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> </dl>

 

 