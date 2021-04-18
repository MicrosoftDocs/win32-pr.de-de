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
# <a name="last_is-attribute"></a><span data-ttu-id="4ee43-105">Letztes \_ ist Attribut</span><span class="sxs-lookup"><span data-stu-id="4ee43-105">last\_is attribute</span></span>

<span data-ttu-id="4ee43-106">Das Feld Attribut **\[ Last \_ \]** gibt den Index des letzten Array Elements an, das übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ee43-106">The field attribute **\[last\_is\]** specifies the index of the last array element to be transmitted.</span></span> <span data-ttu-id="4ee43-107">Wenn der angegebene Index 0 (null) oder negativ ist, werden keine Array Elemente übertragen.</span><span class="sxs-lookup"><span data-stu-id="4ee43-107">When the specified index is zero or negative, no array elements are transmitted.</span></span>

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="4ee43-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ee43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee43-109">*begrenzte Ausdrucks Liste*</span><span class="sxs-lookup"><span data-stu-id="4ee43-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4ee43-110">Gibt einen oder mehrere C-sprach Ausdrücke an.</span><span class="sxs-lookup"><span data-stu-id="4ee43-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="4ee43-111">Jeder Ausdruck ergibt eine ganze Zahl, die den Array Index des letzten zu übertragenden Array Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ee43-111">Each expression evaluates to an integer that represents the array index of the last array element to be transmitted.</span></span> <span data-ttu-id="4ee43-112">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="4ee43-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="4ee43-113">"Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.</span><span class="sxs-lookup"><span data-stu-id="4ee43-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="4ee43-114">Trennen Sie mehrere Ausdrücke durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4ee43-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ee43-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ee43-115">Remarks</span></span>

<span data-ttu-id="4ee43-116">Das **\[ Letzte \_ is \]** -Attribut bestimmt den Wert des Array Indexes, der der **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** Länge ist Attribute entspricht, wenn length nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4ee43-116">The **\[last\_is\]** attribute determines the value of the array index corresponding to the **\[**[**length\_is**](length-is.md)**\]** attribute when **\[length\_is\]** is not specified.</span></span> <span data-ttu-id="4ee43-117">Die Beziehung zwischen diesen Array Indizes lautet wie folgt: length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="4ee43-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="4ee43-118">Wenn der Wert des Array Indexes, der durch **\[** [**First \_**](first-is.md) angegeben wird **\]** , größer ist als der Wert, der durch den **\[ letzten \_ \]** Wert angegeben ist, werden keine Elemente übertragen.</span><span class="sxs-lookup"><span data-stu-id="4ee43-118">If the value of the array index specified by **\[**[**first\_is**](first-is.md)**\]** is larger than the value specified by **\[last\_is\]**, zero elements are transmitted.</span></span>

<span data-ttu-id="4ee43-119">Das **\[ Letzte \_ is \]** -Attribut kann nicht als Feld Attribut gleichzeitig verwendet werden, wenn die **\[** [**Länge \_**](length-is.md) **\]** Attribute oder das **\[** [**Zeichen**](string.md) folgen **\]** Attribut ist.</span><span class="sxs-lookup"><span data-stu-id="4ee43-119">The **\[last\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**length\_is**](length-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="4ee43-120">Die Verwendung eines konstanten Ausdrucks mit dem **\[ letzten \_ is \]** -Attribut ist eine ungeeignete Verwendung des-Attributs.</span><span class="sxs-lookup"><span data-stu-id="4ee43-120">Using a constant expression with the **\[last\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="4ee43-121">Dies ist zulässig, aber ineffizient und führt zu einem langsameren Marshallingcode.</span><span class="sxs-lookup"><span data-stu-id="4ee43-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="4ee43-122">Wenn der durch Max angegebene Wert **\[** [**\_**](max-is.md) **\]** gleich oder größer als 0 (null) ist, muss die folgende Beziehung True lauten: 0 <= Last \_ is <= Max \_ ist.</span><span class="sxs-lookup"><span data-stu-id="4ee43-122">When the value specified by **\[**[**max\_is**](max-is.md)**\]** is equal to or greater than zero, the following relationship must be true: 0 <= last\_is <= max\_is.</span></span>

## <a name="examples"></a><span data-ttu-id="4ee43-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ee43-123">Examples</span></span>

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a><span data-ttu-id="4ee43-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ee43-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee43-125">Feldattribute</span><span class="sxs-lookup"><span data-stu-id="4ee43-125">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="4ee43-126">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="4ee43-126">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="4ee43-127">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="4ee43-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4ee43-128">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="4ee43-128">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="4ee43-129">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="4ee43-129">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="4ee43-130">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="4ee43-130">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 