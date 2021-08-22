---
title: size_is-Attribut
description: Verwenden Sie das \_ \size is\-Attribut, um die Größe des Arbeitsspeichers in -Elementen anzugeben, die für Zeiger mit größenbemessener Größe zugeordnet sind, Zeiger mit größenvergrößerten Zeigern und ein- oder mehrdimensionale Arrays.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is-Attribut MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd57748d3ad92407fd65f3a6af7fc1ebb68321b576d57a50b6ba6f5546f8d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066700"
---
# <a name="size_is-attribute"></a>size \_ is attribute

Verwenden Sie das Size \[ **\_ is-Attribut,** um die Größe des Arbeitsspeichers in Elementen anzugeben, die für Zeiger mit \] größenbemessener Größe zugeordnet sind, zeigergrößenbezogene Zeiger auf zeigergröße und ein- oder mehrdimensionale Arrays.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*eingeschränkte Ausdrucksliste* 
</dt> <dd>

Gibt einen oder mehrere C-Sprachausdrücke an. Jeder Ausdruck wird zu einer nicht negativen ganzzahligen Zahl ausgewertet, die die Menge an Arbeitsspeicher darstellt, die einem Zeiger der Größe oder einem Array zugeordnet ist. Im Fall eines Arrays gibt einen einzelnen Ausdruck an, der die Zuordnungsgröße in Elementen der ersten Dimension dieses Arrays darstellt. Der MIDL-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. MIDL lässt keine Funktionsaufrufe in Ausdrücken und keine Inkrement- und Dekrementoperatoren zu. Verwenden Sie Kommas als Platzhalter für implizite Parameter oder zum Trennen mehrerer Ausdrücke.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie das \[ **Size \_ is-Attribut** \] verwenden, um Speicher für ein mehrdimensionales Array zuzuordnen, und Sie array \[ \] notation verwenden, denken Sie daran, dass nur die erste Dimension eines mehrdimensionalen Arrays zur Laufzeit dynamisch bestimmt werden kann. Die anderen Dimensionen müssen statisch angegeben werden. Weitere Informationen zur Verwendung des \[ **"size \_ is"-Attributs** \] mit mehreren Zeigerebenen, um einem Server das Zurückgeben eines Arrays von Daten mit dynamischer Größe an einen Client zu ermöglichen, wie im Beispiel Proc7 gezeigt, finden Sie unter [Mehrere Zeigerebenen.](/windows/desktop/Rpc/multiple-levels-of-pointers)

Sie können entweder \[ **size \_ is** \] oder max [**\_ is**](max-is.md) (aber nicht beide in derselben Attributliste) verwenden, um die Größe eines Arrays anzugeben, dessen Obergrenzen zur Laufzeit bestimmt werden. Beachten Sie jedoch, dass die \[ **Größe \_ des** \] Attributs nicht für feste Arraydimensionen verwendet werden kann. Das \[ **Attribut max \_ is** \] gibt den maximal gültigen Arrayindex an. Daher entspricht die Angabe der \[ Größe \_ is(n) \] der Angabe von max \[ \_ is(n-1). \]

Ein \[ [**in-**](in.md) \] oder \[ in-, [**out**](out-idl.md) \] conformant-array-Parameter mit dem \[ [**Zeichenfolgenattribut**](string.md) muss nicht über die \] Größe oder das Attribut max \[ **\_** \] \[ [**\_ is**](max-is.md) \] verfügen. In diesem Fall wird die Größe der Zuordnung anhand des NULL-Abschlusszeichens der Eingabezeichenfolge bestimmt. Alle anderen konformen Arrays mit dem \[ \] Zeichenfolgenattribut müssen das \[ **Attribut size \_ oder** \] max \[ **\_ is** \] aufweisen.

Obwohl es zulässig ist, das \[ **Size \_ is-Attribut** mit einer Konstante zu \] verwenden, ist dies ineffizient und unnötig. Verwenden Sie beispielsweise ein Array mit fester Größe:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

Anstelle von:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

Sie können die \[ **Attribute size \_ is** \] und length \[ [**\_ is**](length-is.md) \] zusammen verwenden. Wenn Sie dies tun, steuert die \[ **Größe \_ des** \] Attributs die Menge an Arbeitsspeicher, die den Daten zugeordnet ist. Das \[ **Attribut length \_ is** \] gibt an, wie viele Elemente übertragen werden. Die durch die Größe angegebene \[ **Arbeitsspeichermenge \_ ist** \] , und die Länge \[ **\_ der** \] Attribute muss nicht identisch sein. Beispielsweise kann Ihr Client einen \[ \] in,out-Parameter an einen Server übergeben und eine große Speicherbelegung mit \[ **der Größe \_** \] angeben, obwohl er eine kleine Anzahl von Datenelementen angibt, die mit der Länge übergeben werden \[ **\_** \] sollen. Dadurch kann der Server das Array mit mehr Daten füllen, als er empfangen hat, die er dann an den Client zurücksenden kann.

Im Allgemeinen ist es nicht sinnvoll, sowohl die Größe als auch die Länge für \[ **\_** \] \[ [**\_**](length-is.md) \] \[ \] ein- oder \[ ausgehende \] Parameter anzugeben. In beiden Fällen \[ **\_ steuert die Größe** \] die Speicherbelegung. Ihre Anwendung kann \[ **die \_ Größe** \] verwenden, um mehr Arrayelemente zuzuordnen, als sie überträgt (wie durch length angegeben \[ **\_ ist).** \] Dies wäre jedoch ineffizient. Es wäre auch ineffizient, identische Werte für \[ **die Größe \_ anzugeben,** \] und die Länge \[ **\_ ist** \] . Dies würde zusätzlichen Mehraufwand beim Marshalling von Parametern verursachen. Wenn die Werte der \[ **Größe \_ gleich** \] sind und length immer gleich \[ **\_ ist,** sollten Sie das Attribut length \] \[ **\_ is** weglassen. \]

## <a name="examples"></a>Beispiele

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[Feldattribute](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**\_first ist**](first-is.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**last \_ ist**](last-is.md)
</dt> <dt>

[**length \_ ist**](length-is.md)
</dt> <dt>

[**max \_ ist**](max-is.md)
</dt> <dt>

[**min \_ ist**](min-is.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> </dl>

 

 