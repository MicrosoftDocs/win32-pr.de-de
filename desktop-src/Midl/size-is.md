---
title: size_is-Attribut
description: Verwenden Sie das Attribut \ size \_ is \, um die Größe des Arbeitsspeichers in Elementen anzugeben, die für Größen Zeiger, große Zeiger auf Größen Zeiger und einzelne oder mehrdimensionale Arrays reserviert werden.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724945"
---
# <a name="size_is-attribute"></a>Größe \_ ist Attribut

Verwenden \[ Sie das Attribut **size \_ is** , \] um die Größe des Arbeitsspeichers in-Elementen anzugeben, die für Größen Zeiger, große Zeiger auf Größen Zeiger und einzelne oder mehrdimensionale Arrays reserviert werden.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*begrenzte Ausdrucks Liste* 
</dt> <dd>

Gibt einen oder mehrere C-sprach Ausdrücke an. Jeder Ausdruck ergibt eine nicht negative ganze Zahl, die die Menge an Arbeitsspeicher darstellt, die einem Zeiger oder einem Array zugeordnet wird. Gibt im Fall eines Arrays einen einzelnen Ausdruck an, der die Zuordnungs Größe der ersten Dimension dieses Arrays in-Elementen darstellt. Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke. "Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu. Verwenden Sie Kommas als Platzhalter für implizite Parameter oder, um mehrere Ausdrücke voneinander zu trennen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie das Attribut " \[ **size \_ is** " verwenden, \] um Arbeitsspeicher für ein mehrdimensionales Array zuzuordnen, und Sie die Array \[ \] Notation verwenden, beachten Sie, dass nur die erste Dimension eines mehrdimensionalen Arrays zur Laufzeit dynamisch bestimmt werden kann. Die anderen Dimensionen müssen statisch angegeben werden. Weitere Informationen zum Verwenden der \[ **Größe \_ ist** \] Attribute mit mehreren Ebenen von Zeigern, damit ein Server ein dynamisch großes Array von Daten an einen Client zurückgeben kann, wie im Beispiel Proc7 gezeigt, finden Sie unter [mehrere Ebenen von Zeigern](/windows/desktop/Rpc/multiple-levels-of-pointers).

\[ **\_** \] Zum Angeben der Größe eines Arrays, dessen obere Begrenzungen zur Laufzeit bestimmt werden, können Sie entweder size ist oder [**Max \_ is**](max-is.md) (aber nicht beides in der gleichen Attribut Liste) verwenden. Beachten Sie jedoch, dass die \[ **size \_** - \] Eigenschaft Attribute nicht für die festgelegten Array Dimensionen verwendet werden kann. Das Maximum \[ **\_ is** - \] Attribut gibt den maximalen gültigen Array Index an. Folglich \[ \_ entspricht die Angabe von Size (n) der \] Angabe von \[ Max \_ is (n-1) \] .

Ein \[ [**in**](in.md) \] \[ -oder in-, [**out**](out-idl.md) \] -konformitätsarray-Parameter mit dem \[ [**String**](string.md) - \] Attribut muss nicht die \[ **Größe \_** \] oder das \[ [**Maximum \_**](max-is.md) - \] Attribut aufweisen. In diesem Fall wird die Größe der Zuordnung vom null-Terminator der Eingabe Zeichenfolge bestimmt. Alle anderen konformen Arrays mit dem \[ Zeichen folgen \] Attribut müssen eine \[ **Größe \_** \] oder ein \[ **Max \_** - \] Attribut aufweisen.

Obwohl es zulässig ist, die \[ **Größe des \_** \] Attributs mit einer Konstanten zu verwenden, ist dies ineffizient und unnötig. Verwenden Sie z. b. ein Array mit fester Größe:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

Anstelle von:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

Sie können die \[ **\_ Größe** \] und die \[ [**Länge Attribute \_**](length-is.md) \] gleichzeitig verwenden. Wenn Sie dies tun, \[ steuert die Größe "Attribute" die Menge an Arbeitsspeicher, die den Daten zugeordnet **\_ ist** \] . Das \[ **length \_ is** - \] Attribut gibt an, wie viele Elemente übertragen werden. Der durch die Größe angegebene Arbeitsspeicher \[ **\_** \] und die \[ **Länge \_ sind** \] Attribute müssen nicht identisch sein. Beispielsweise kann der Client einen \[ in-, out \] -Parameter an einen Server übergeben und eine große Speicher Belegung mit einer \[ **Größe \_** von angeben \] , auch wenn er angibt, dass eine kleine Anzahl von Datenelementen, die übergeben werden sollen, den Wert hat \[ **\_** \] . Dies ermöglicht es dem Server, das Array mit mehr Daten auszufüllen, als es empfangen hat, und es dann an den Client zurücksenden kann.

Im Allgemeinen ist es nicht sinnvoll, sowohl die \[ **Größe \_** \] als auch die \[ [**Länge \_**](length-is.md) \] \[ in den \] \[ \] Parametern "in" und "out" anzugeben. In beiden Fällen \[ **\_ ist size** die \] Speicher Belegung von Steuerelementen. Die Anwendung kann die \[ **Größe \_** verwenden \] , um mehr Array Elemente zuzuordnen, als Sie überträgt (wie durch \[ **length \_** angegeben \] ). Dies wäre jedoch ineffizient. Außerdem wäre es ineffizient, identische Werte für die \[ **Größe anzugeben \_** , \] und die \[ **Länge \_ ist** \] . Dies würde während des Parametermarshalling einen zusätzlichen Aufwand verursachen. Wenn die Werte der \[ **Größe \_** \] und \[ **\_ length** \] immer identisch sind, lassen Sie die \[ **Länge \_ ist** \] Attribute Weg.

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

[**Mikro**](arrays-1.md)
</dt> <dt>

[Feldattribute](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**der erste \_ ist**](first-is.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**Letzter \_ ist**](last-is.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
</dt> <dt>

[**Min \_ ist**](min-is.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> </dl>

 

 