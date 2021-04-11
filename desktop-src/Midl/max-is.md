---
title: max_is-Attribut
description: Das Attribut \ Max \_ ist \ bezeichnet den maximalen Wert für einen gültigen Array Index.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- Max_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314811"
---
# <a name="max_is-attribute"></a>Max \_ ist Attribut

Das **\[ Maximum \_ is \]** -Attribut bestimmt den maximalen Wert für einen gültigen Array Index.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*begrenzte Ausdrucks Liste* 
</dt> <dd>

Gibt einen oder mehrere C-sprach Ausdrücke an. Jeder Ausdruck ergibt eine ganze Zahl, die den höchsten gültigen Array Index darstellt. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu. Trennen Sie mehrere Ausdrücke durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Maximum \_ is \]** -Attribut entspricht nicht notwendigerweise der Anzahl der Elemente im Array. Für ein Array der Größe *n* in C, bei dem das erste Array Element die Element Nummer 0 (null) ist, ist der maximale Wert für einen gültigen Array Index *n*– 1.

Das **\[ Maximum \_ is \]** -Attribut kann nicht gleichzeitig als Feld Attribut verwendet werden, wenn die **\[** [**Größe Attribute \_ ist**](size-is.md) **\]** .

Obwohl es zulässig ist, das **\[ Maximum \_ is \]** -Attribut mit einem konstanten Ausdruck zu verwenden, ist dies ineffizient und unnötig. Verwenden Sie z. b. ein Array mit fester Größe:

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

Anstelle von:

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a>Beispiele

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Feldattribute](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Min \_ ist**](min-is.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> </dl>

 

 