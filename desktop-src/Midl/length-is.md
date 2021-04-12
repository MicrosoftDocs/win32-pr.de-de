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
# <a name="length_is-attribute"></a><span data-ttu-id="42467-105">Länge \_ ist Attribut</span><span class="sxs-lookup"><span data-stu-id="42467-105">length\_is attribute</span></span>

<span data-ttu-id="42467-106">Das **\[ length \_ is \]** -Attribut gibt die Anzahl der zu übertragenden Array Elemente an.</span><span class="sxs-lookup"><span data-stu-id="42467-106">The **\[length\_is\]** attribute specifies the number of array elements to be transmitted.</span></span> <span data-ttu-id="42467-107">Sie müssen einen nicht negativen Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="42467-107">You must specify a non-negative value.</span></span>

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="42467-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="42467-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42467-109">*begrenzte Ausdrucks Liste*</span><span class="sxs-lookup"><span data-stu-id="42467-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="42467-110">Gibt einen oder mehrere C-sprach Ausdrücke an.</span><span class="sxs-lookup"><span data-stu-id="42467-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="42467-111">Jeder Ausdruck ergibt eine ganze Zahl, die die Anzahl der zu übertragenden Array Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="42467-111">Each expression evaluates to an integer that represents the number of array elements to be transmitted.</span></span> <span data-ttu-id="42467-112">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="42467-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="42467-113">"Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.</span><span class="sxs-lookup"><span data-stu-id="42467-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="42467-114">Trennen Sie mehrere Ausdrücke durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="42467-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42467-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42467-115">Remarks</span></span>

<span data-ttu-id="42467-116">Das **\[ length \_ is \]** -Attribut bestimmt den Wert der Array Indizes, die dem **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** letzten is-Attribut entsprechen, wenn der letzte is-Wert nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="42467-116">The **\[length\_is\]** attribute determines the value of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** attribute when **\[last\_is\]** is not specified.</span></span> <span data-ttu-id="42467-117">Die Beziehung zwischen diesen Array Indizes lautet wie folgt: length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="42467-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="42467-118">Das **\[ length \_ is \]** -Attribut kann nicht gleichzeitig mit dem **\[** [**letzten \_ is**](last-is.md) - **\]** Attribut oder dem **\[** [**String**](string.md) -Attribut verwendet werden **\]** .</span><span class="sxs-lookup"><span data-stu-id="42467-118">The **\[length\_is\]** attribute cannot be used at the same time as the **\[**[**last\_is**](last-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="42467-119">Verwenden Sie zum Definieren einer gezählten Zeichenfolge mit der **\[ Länge \_ \]** oder **\[** dem [**letzten \_ is**](last-is.md) - **\]** Attribut ein Zeichen Array oder einen Zeiger ohne das **\[** [**Zeichen**](string.md) folgen **\]** Attribut.</span><span class="sxs-lookup"><span data-stu-id="42467-119">To define a counted string with a **\[length\_is\]** or **\[**[**last\_is**](last-is.md)**\]** attribute, use a character array or pointer without the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="42467-120">Die Verwendung eines konstanten Ausdrucks mit der **\[ Länge \_ is \]** -Attribut ist eine ungeeignete Verwendung des-Attributs.</span><span class="sxs-lookup"><span data-stu-id="42467-120">Using a constant expression with the **\[length\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="42467-121">Dies ist zulässig, aber ineffizient und führt zu einem langsameren Marshallingcode.</span><span class="sxs-lookup"><span data-stu-id="42467-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="42467-122">Sie können die **\[** [**Größe \_**](size-is.md) **\]** und die **\[ Länge \_ \]** Attribute gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="42467-122">You can use the **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** attributes together.</span></span> <span data-ttu-id="42467-123">Wenn Sie dies tun, steuert die Größe "Attribute" die Menge an Arbeitsspeicher, die den Daten zugeordnet **\[ \_ ist \]** .</span><span class="sxs-lookup"><span data-stu-id="42467-123">When you do, the **\[size\_is\]** attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="42467-124">Das **\[ length \_ is \]** -Attribut gibt an, wie viele Elemente übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="42467-124">The **\[length\_is\]** attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="42467-125">Der durch die **\[ \_ \] Größe** angegebene Arbeitsspeicher und die **\[ Länge \_ sind \]** Attribute müssen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="42467-125">The amount of memory specified by the **\[size\_is\]** and **\[length\_is\]** attributes need not be the same.</span></span> <span data-ttu-id="42467-126">Beispielsweise kann der Client einen **\[ in**-, **out \]** -Parameter an einen Server übergeben und eine große **\[ \_ \]** Speicher Belegung mit einer Größe von angeben, auch wenn er angibt, dass eine kleine **\[ \_ \]** Anzahl von Datenelementen, die übergeben werden sollen, den Wert hat.</span><span class="sxs-lookup"><span data-stu-id="42467-126">For instance, your client may pass an **\[in**, **out\]** parameter to a server and specify a large memory allocation with **\[size\_is\]**, even though it specifies a small number of data elements to be passed with **\[length\_is\]**.</span></span> <span data-ttu-id="42467-127">Dies ermöglicht es dem Server, das Array mit mehr Daten auszufüllen, als es empfangen hat, und es dann an den Client zurücksenden kann.</span><span class="sxs-lookup"><span data-stu-id="42467-127">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="42467-128">Im Allgemeinen ist es nicht sinnvoll, sowohl die **\[** [**Größe \_**](size-is.md) **\]** als auch die **\[ \_ \] Länge** in den **\[** [](in.md) **\]** **\[** [](out-idl.md) Parametern "in" und "out" anzugeben **\]** .</span><span class="sxs-lookup"><span data-stu-id="42467-128">In general, it isn't useful to specify both **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** on **\[**[**in**](in.md)**\]** or **\[**[**out**](out-idl.md)**\]** parameters.</span></span> <span data-ttu-id="42467-129">In beiden Fällen **\[ \_ ist \] size** die Speicher Belegung von Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="42467-129">In both cases, **\[size\_is\]** controls memory allocation.</span></span> <span data-ttu-id="42467-130">Die Anwendung kann die **\[ Größe \_ \]** verwenden, um mehr Array Elemente zuzuordnen, als Sie überträgt (wie durch **\[ length \_ \]** angegeben).</span><span class="sxs-lookup"><span data-stu-id="42467-130">Your application could use **\[size\_is\]** to allocate more array elements than it transmits (as specified by **\[length\_is\]**).</span></span> <span data-ttu-id="42467-131">Dies wäre jedoch ineffizient.</span><span class="sxs-lookup"><span data-stu-id="42467-131">However, this would be inefficient.</span></span> <span data-ttu-id="42467-132">Außerdem wäre es ineffizient, identische Werte für die **\[ Größe \_ \]** anzugeben, und die **\[ Länge \_ ist \]**.</span><span class="sxs-lookup"><span data-stu-id="42467-132">It would also be inefficient to specify identical values for **\[size\_is\]** and **\[length\_is\]**.</span></span> <span data-ttu-id="42467-133">Da bei der Parameter Marshalling zusätzlicher Aufwand entstehen würde.</span><span class="sxs-lookup"><span data-stu-id="42467-133">Because it would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="42467-134">Wenn die Werte der **\[ Größe \_ \]** und **\[ length \_ \]** immer identisch sind, lassen Sie die **\[ Länge \_ ist \]** Attribute Weg.</span><span class="sxs-lookup"><span data-stu-id="42467-134">When the values of **\[size\_is\]** and **\[length\_is\]** are always the same, omit the **\[length\_is\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="42467-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42467-135">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="42467-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="42467-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42467-137">Feldattribute</span><span class="sxs-lookup"><span data-stu-id="42467-137">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="42467-138">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="42467-138">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="42467-139">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="42467-139">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="42467-140">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="42467-140">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="42467-141">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="42467-141">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="42467-142">**Min \_ ist**</span><span class="sxs-lookup"><span data-stu-id="42467-142">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="42467-143">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="42467-143">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="42467-144">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42467-144">**string**</span></span>](string.md)
</dt> </dl>

 

 