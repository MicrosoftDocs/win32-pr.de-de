---
title: length_is-Attribut
description: Das \ length \_ is \-Attribut gibt die Anzahl der zu übertragenden Array Elemente an. Sie müssen einen nicht negativen Wert angeben.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473044"
---
# <a name="length_is-attribute"></a>Länge \_ ist Attribut

Das **\[ length \_ is \]** -Attribut gibt die Anzahl der zu übertragenden Array Elemente an. Sie müssen einen nicht negativen Wert angeben.

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*begrenzte Ausdrucks Liste* 
</dt> <dd>

Gibt einen oder mehrere C-sprach Ausdrücke an. Jeder Ausdruck ergibt eine ganze Zahl, die die Anzahl der zu übertragenden Array Elemente darstellt. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu. Trennen Sie mehrere Ausdrücke durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ length \_ is \]** -Attribut bestimmt den Wert der Array Indizes, die dem **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** letzten is-Attribut entsprechen, wenn der letzte is-Wert nicht angegeben ist. Die Beziehung zwischen diesen Array Indizes lautet wie folgt: length = Last-First + 1.

Das **\[ length \_ is \]** -Attribut kann nicht gleichzeitig mit dem **\[** [**letzten \_ is**](last-is.md) - **\]** Attribut oder dem **\[** [**String**](string.md) -Attribut verwendet werden **\]** .

Verwenden Sie zum Definieren einer gezählten Zeichenfolge mit der **\[ Länge \_ \]** oder **\[** dem [**letzten \_ is**](last-is.md) - **\]** Attribut ein Zeichen Array oder einen Zeiger ohne das **\[** [**Zeichen**](string.md) folgen **\]** Attribut.

Die Verwendung eines konstanten Ausdrucks mit der **\[ Länge \_ is \]** -Attribut ist eine ungeeignete Verwendung des-Attributs. Dies ist zulässig, aber ineffizient und führt zu einem langsameren Marshallingcode.

Sie können die **\[** [**Größe \_**](size-is.md) **\]** und die **\[ Länge \_ \]** Attribute gleichzeitig verwenden. Wenn Sie dies tun, steuert die Größe "Attribute" die Menge an Arbeitsspeicher, die den Daten zugeordnet **\[ \_ ist \]** . Das **\[ length \_ is \]** -Attribut gibt an, wie viele Elemente übertragen werden. Der durch die **\[ \_ \] Größe** angegebene Arbeitsspeicher und die **\[ Länge \_ sind \]** Attribute müssen nicht identisch sein. Beispielsweise kann der Client einen **\[ in**-, **out \]** -Parameter an einen Server übergeben und eine große **\[ \_ \]** Speicher Belegung mit einer Größe von angeben, auch wenn er angibt, dass eine kleine **\[ \_ \]** Anzahl von Datenelementen, die übergeben werden sollen, den Wert hat. Dies ermöglicht es dem Server, das Array mit mehr Daten auszufüllen, als es empfangen hat, und es dann an den Client zurücksenden kann.

Im Allgemeinen ist es nicht sinnvoll, sowohl die **\[** [**Größe \_**](size-is.md) **\]** als auch die **\[ \_ \] Länge** in den **\[** [](in.md) **\]** **\[** [](out-idl.md) Parametern "in" und "out" anzugeben **\]** . In beiden Fällen **\[ \_ ist \] size** die Speicher Belegung von Steuerelementen. Die Anwendung kann die **\[ Größe \_ \]** verwenden, um mehr Array Elemente zuzuordnen, als Sie überträgt (wie durch **\[ length \_ \]** angegeben). Dies wäre jedoch ineffizient. Außerdem wäre es ineffizient, identische Werte für die **\[ Größe \_ \]** anzugeben, und die **\[ Länge \_ ist \]**. Da bei der Parameter Marshalling zusätzlicher Aufwand entstehen würde. Wenn die Werte der **\[ Größe \_ \]** und **\[ length \_ \]** immer identisch sind, lassen Sie die **\[ Länge \_ ist \]** Attribute Weg.

## <a name="examples"></a>Beispiele

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Feldattribute](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**der erste \_ ist**](first-is.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Letzter \_ ist**](last-is.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
</dt> <dt>

[**Min \_ ist**](min-is.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> </dl>

 

 