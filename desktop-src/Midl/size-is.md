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
# <a name="size_is-attribute"></a><span data-ttu-id="a006b-104">Größe \_ ist Attribut</span><span class="sxs-lookup"><span data-stu-id="a006b-104">size\_is attribute</span></span>

<span data-ttu-id="a006b-105">Verwenden \[ Sie das Attribut **size \_ is** , \] um die Größe des Arbeitsspeichers in-Elementen anzugeben, die für Größen Zeiger, große Zeiger auf Größen Zeiger und einzelne oder mehrdimensionale Arrays reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="a006b-105">Use the \[**size\_is**\] attribute to specify the size of memory, in elements, allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a><span data-ttu-id="a006b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a006b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a006b-107">*begrenzte Ausdrucks Liste*</span><span class="sxs-lookup"><span data-stu-id="a006b-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a006b-108">Gibt einen oder mehrere C-sprach Ausdrücke an.</span><span class="sxs-lookup"><span data-stu-id="a006b-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="a006b-109">Jeder Ausdruck ergibt eine nicht negative ganze Zahl, die die Menge an Arbeitsspeicher darstellt, die einem Zeiger oder einem Array zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a006b-109">Each expression evaluates to a non-negative integer that represents the amount of memory allocated to a sized pointer or an array.</span></span> <span data-ttu-id="a006b-110">Gibt im Fall eines Arrays einen einzelnen Ausdruck an, der die Zuordnungs Größe der ersten Dimension dieses Arrays in-Elementen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a006b-110">In the case of an array, specifies a single expression that represents the allocation size, in elements, of the first dimension of that array.</span></span> <span data-ttu-id="a006b-111">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="a006b-111">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="a006b-112">"Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.</span><span class="sxs-lookup"><span data-stu-id="a006b-112">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="a006b-113">Verwenden Sie Kommas als Platzhalter für implizite Parameter oder, um mehrere Ausdrücke voneinander zu trennen.</span><span class="sxs-lookup"><span data-stu-id="a006b-113">Use commas as placeholders for implicit parameters, or to separate multiple expressions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a006b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a006b-114">Remarks</span></span>

<span data-ttu-id="a006b-115">Wenn Sie das Attribut " \[ **size \_ is** " verwenden, \] um Arbeitsspeicher für ein mehrdimensionales Array zuzuordnen, und Sie die Array \[ \] Notation verwenden, beachten Sie, dass nur die erste Dimension eines mehrdimensionalen Arrays zur Laufzeit dynamisch bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a006b-115">If you are using the \[**size\_is**\] attribute to allocate memory for a multidimensional array and you are using array \[ \] notation, keep in mind that only the first dimension of a multidimensional array can be dynamically determined at run time.</span></span> <span data-ttu-id="a006b-116">Die anderen Dimensionen müssen statisch angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a006b-116">The other dimensions must be statically specified.</span></span> <span data-ttu-id="a006b-117">Weitere Informationen zum Verwenden der \[ **Größe \_ ist** \] Attribute mit mehreren Ebenen von Zeigern, damit ein Server ein dynamisch großes Array von Daten an einen Client zurückgeben kann, wie im Beispiel Proc7 gezeigt, finden Sie unter [mehrere Ebenen von Zeigern](/windows/desktop/Rpc/multiple-levels-of-pointers).</span><span class="sxs-lookup"><span data-stu-id="a006b-117">For more information on using the \[**size\_is**\] attribute with multiple levels of pointers to enable a server to return a dynamically-sized array of data to a client, as shown in the example Proc7, see [Multiple Levels of Pointers](/windows/desktop/Rpc/multiple-levels-of-pointers).</span></span>

<span data-ttu-id="a006b-118">\[ **\_** \] Zum Angeben der Größe eines Arrays, dessen obere Begrenzungen zur Laufzeit bestimmt werden, können Sie entweder size ist oder [**Max \_ is**](max-is.md) (aber nicht beides in der gleichen Attribut Liste) verwenden.</span><span class="sxs-lookup"><span data-stu-id="a006b-118">You can use either \[**size\_is**\] or [**max\_is**](max-is.md) (but not both in the same attribute list) to specify the size of an array whose upper bounds are determined at run time.</span></span> <span data-ttu-id="a006b-119">Beachten Sie jedoch, dass die \[ **size \_** - \] Eigenschaft Attribute nicht für die festgelegten Array Dimensionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a006b-119">Note, however, that the \[**size\_is**\] attribute cannot be used on array dimensions that are fixed.</span></span> <span data-ttu-id="a006b-120">Das Maximum \[ **\_ is** - \] Attribut gibt den maximalen gültigen Array Index an.</span><span class="sxs-lookup"><span data-stu-id="a006b-120">The \[**max\_is**\] attribute specifies the maximum valid array index.</span></span> <span data-ttu-id="a006b-121">Folglich \[ \_ entspricht die Angabe von Size (n) der \] Angabe von \[ Max \_ is (n-1) \] .</span><span class="sxs-lookup"><span data-stu-id="a006b-121">As a result, specifying \[size\_is(n)\] is equivalent to specifying \[max\_is(n-1)\].</span></span>

<span data-ttu-id="a006b-122">Ein \[ [**in**](in.md) \] \[ -oder in-, [**out**](out-idl.md) \] -konformitätsarray-Parameter mit dem \[ [**String**](string.md) - \] Attribut muss nicht die \[ **Größe \_** \] oder das \[ [**Maximum \_**](max-is.md) - \] Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a006b-122">An \[ [**in**](in.md)\] or \[in, [**out**](out-idl.md)\] conformant-array parameter with the \[ [**string**](string.md)\] attribute need not have the \[**size\_is**\] or \[[**max\_is**](max-is.md)\] attribute.</span></span> <span data-ttu-id="a006b-123">In diesem Fall wird die Größe der Zuordnung vom null-Terminator der Eingabe Zeichenfolge bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a006b-123">In this case, the size of the allocation is determined from the NULL terminator of the input string.</span></span> <span data-ttu-id="a006b-124">Alle anderen konformen Arrays mit dem \[ Zeichen folgen \] Attribut müssen eine \[ **Größe \_** \] oder ein \[ **Max \_** - \] Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a006b-124">All other conformant arrays with the \[string\] attribute must have a \[**size\_is**\] or \[**max\_is**\] attribute.</span></span>

<span data-ttu-id="a006b-125">Obwohl es zulässig ist, die \[ **Größe des \_** \] Attributs mit einer Konstanten zu verwenden, ist dies ineffizient und unnötig.</span><span class="sxs-lookup"><span data-stu-id="a006b-125">While it is legal to use the \[**size\_is**\] attribute with a constant, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="a006b-126">Verwenden Sie z. b. ein Array mit fester Größe:</span><span class="sxs-lookup"><span data-stu-id="a006b-126">For example, use a fixed size array:</span></span>

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

<span data-ttu-id="a006b-127">Anstelle von:</span><span class="sxs-lookup"><span data-stu-id="a006b-127">instead of:</span></span>

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

<span data-ttu-id="a006b-128">Sie können die \[ **\_ Größe** \] und die \[ [**Länge Attribute \_**](length-is.md) \] gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="a006b-128">You can use the \[**size\_is**\] and \[[**length\_is**](length-is.md)\] attributes together.</span></span> <span data-ttu-id="a006b-129">Wenn Sie dies tun, \[ steuert die Größe "Attribute" die Menge an Arbeitsspeicher, die den Daten zugeordnet **\_ ist** \] .</span><span class="sxs-lookup"><span data-stu-id="a006b-129">When you do, the \[**size\_is**\] attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="a006b-130">Das \[ **length \_ is** - \] Attribut gibt an, wie viele Elemente übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="a006b-130">The \[**length\_is**\] attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="a006b-131">Der durch die Größe angegebene Arbeitsspeicher \[ **\_** \] und die \[ **Länge \_ sind** \] Attribute müssen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a006b-131">The amount of memory specified by the \[**size\_is**\] and \[**length\_is**\] attributes need not be the same.</span></span> <span data-ttu-id="a006b-132">Beispielsweise kann der Client einen \[ in-, out \] -Parameter an einen Server übergeben und eine große Speicher Belegung mit einer \[ **Größe \_** von angeben \] , auch wenn er angibt, dass eine kleine Anzahl von Datenelementen, die übergeben werden sollen, den Wert hat \[ **\_** \] .</span><span class="sxs-lookup"><span data-stu-id="a006b-132">For instance, your client may pass an \[in,out\] parameter to a server and specify a large memory allocation with \[**size\_is**\], even though it specifies a small number of data elements to be passed with \[**length\_is**\].</span></span> <span data-ttu-id="a006b-133">Dies ermöglicht es dem Server, das Array mit mehr Daten auszufüllen, als es empfangen hat, und es dann an den Client zurücksenden kann.</span><span class="sxs-lookup"><span data-stu-id="a006b-133">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="a006b-134">Im Allgemeinen ist es nicht sinnvoll, sowohl die \[ **Größe \_** \] als auch die \[ [**Länge \_**](length-is.md) \] \[ in den \] \[ \] Parametern "in" und "out" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a006b-134">In general, it isn't useful to specify both \[**size\_is**\] and \[[**length\_is**](length-is.md)\] on \[in\] or \[out\] parameters.</span></span> <span data-ttu-id="a006b-135">In beiden Fällen \[ **\_ ist size** die \] Speicher Belegung von Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="a006b-135">In both cases, \[**size\_is**\] controls memory allocation.</span></span> <span data-ttu-id="a006b-136">Die Anwendung kann die \[ **Größe \_** verwenden \] , um mehr Array Elemente zuzuordnen, als Sie überträgt (wie durch \[ **length \_** angegeben \] ).</span><span class="sxs-lookup"><span data-stu-id="a006b-136">Your application could use \[**size\_is**\] to allocate more array elements than it transmits (as specified by \[**length\_is**\]).</span></span> <span data-ttu-id="a006b-137">Dies wäre jedoch ineffizient.</span><span class="sxs-lookup"><span data-stu-id="a006b-137">However, this would be inefficient.</span></span> <span data-ttu-id="a006b-138">Außerdem wäre es ineffizient, identische Werte für die \[ **Größe anzugeben \_** , \] und die \[ **Länge \_ ist** \] .</span><span class="sxs-lookup"><span data-stu-id="a006b-138">It would also be inefficient to specify identical values for \[**size\_is**\] and \[**length\_is**\].</span></span> <span data-ttu-id="a006b-139">Dies würde während des Parametermarshalling einen zusätzlichen Aufwand verursachen.</span><span class="sxs-lookup"><span data-stu-id="a006b-139">It would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="a006b-140">Wenn die Werte der \[ **Größe \_** \] und \[ **\_ length** \] immer identisch sind, lassen Sie die \[ **Länge \_ ist** \] Attribute Weg.</span><span class="sxs-lookup"><span data-stu-id="a006b-140">If the values of \[**size\_is**\] and \[**length\_is**\] are always the same, omit the \[**length\_is**\] attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="a006b-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a006b-141">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a006b-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a006b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a006b-143">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="a006b-143">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="a006b-144">Feldattribute</span><span class="sxs-lookup"><span data-stu-id="a006b-144">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="a006b-145">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="a006b-145">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="a006b-146">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="a006b-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a006b-147">**in**</span><span class="sxs-lookup"><span data-stu-id="a006b-147">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="a006b-148">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="a006b-148">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="a006b-149">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="a006b-149">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="a006b-150">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="a006b-150">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="a006b-151">**Min \_ ist**</span><span class="sxs-lookup"><span data-stu-id="a006b-151">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="a006b-152">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="a006b-152">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="a006b-153">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a006b-153">**string**</span></span>](string.md)
</dt> </dl>

 

 