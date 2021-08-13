---
title: max_is-Attribut
description: Das \_ \max is\-Attribut gibt den Maximalwert für einen gültigen Arrayindex an.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is-Attribut MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dfa7e8cdc5b1df752a3a6eb442524157228d354079f262a27a5514860e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642966"
---
# <a name="max_is-attribute"></a>max \_ is attribute

Das **\[ Attribut max \_ is \]** legt den Maximalwert für einen gültigen Arrayindex an.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*eingeschränkte Ausdrucksliste* 
</dt> <dd>

Gibt einen oder mehrere C-Sprachausdrücke an. Jeder Ausdruck wird zu einer ganzen Zahl ausgewertet, die den höchsten gültigen Arrayindex darstellt. Der MIDL-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. MIDL lässt keine Funktionsaufrufe in Ausdrücken und keine Inkrement- und Dekrementoperatoren zu. Trennen Sie mehrere Ausdrücke durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ Attribut max \_ is \]** entspricht nicht notwendigerweise der Anzahl der Elemente im Array. Bei einem Array der Größe *n* in C, bei dem das erste Arrayelement elementnummer 0 ist, beträgt der Höchstwert für einen gültigen Arrayindex *n*–1.

Das **\[ Attribut max \_ is \]** kann nicht gleichzeitig mit dem Attribut size **\[** [**\_ is**](size-is.md) als **\]** Feldattribut verwendet werden.

Obwohl es zulässig ist, das **\[ Attribut max \_ is \]** mit einem konstanten Ausdruck zu verwenden, ist dies ineffizient und unnötig. Verwenden Sie beispielsweise ein Array mit fester Größe:

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

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**min \_ ist**](min-is.md)
</dt> <dt>

[**size \_ ist**](size-is.md)
</dt> </dl>

 

 