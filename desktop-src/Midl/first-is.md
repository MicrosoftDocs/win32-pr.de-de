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
# <a name="first_is-attribute"></a><span data-ttu-id="c2ae4-104">erstes \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="c2ae4-104">first\_is attribute</span></span>

<span data-ttu-id="c2ae4-105">Das \[ **erste \_ is** - \] Attribut gibt den Index des ersten Array Elements an, das übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-105">The \[**first\_is**\] attribute specifies the index of the first array element to be transmitted.</span></span>

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a><span data-ttu-id="c2ae4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2ae4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2ae4-107">*begrenzte Ausdrucks Liste*</span><span class="sxs-lookup"><span data-stu-id="c2ae4-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c2ae4-108">Gibt einen oder mehrere C-sprach Ausdrücke an.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="c2ae4-109">Jeder Ausdruck ergibt eine ganze Zahl, die den Array Index des ersten zu übertragenden Array Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-109">Each expression evaluates to an integer that represents the array index of the first array element to be transmitted.</span></span> <span data-ttu-id="c2ae4-110">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="c2ae4-111">"Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="c2ae4-112">Trennen Sie mehrere Ausdrücke durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2ae4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2ae4-113">Remarks</span></span>

<span data-ttu-id="c2ae4-114">Wenn das **\[ erste \_ Attribut \] ist** , das nicht vorhanden ist, oder wenn der angegebene Index eine negative Zahl ist, ist Array Element NULL das erste übertragene Element.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-114">If the **\[first\_is\]** attribute is not present, or if the specified index is a negative number, array element zero is the first element transmitted.</span></span>

<span data-ttu-id="c2ae4-115">Das **\[ erste \_ ist \]** -Attribut kann auch helfen, die Werte der Array Indizes zu ermitteln, die dem **\[** [**letzten \_ is**](last-is.md) - **\]** oder length-Attribut entsprechen, **\[** [**\_**](length-is.md) **\]** Wenn diese Attribute nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-115">The **\[first\_is\]** attribute can also help determine the values of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** or **\[**[**length\_is**](length-is.md)**\]** attribute when these attributes are not specified.</span></span> <span data-ttu-id="c2ae4-116">Die Beziehung zwischen diesen Array Indizes lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c2ae4-116">The relationship between these array indexes is:</span></span>

``` syntax
length = last - first + 1
```

<span data-ttu-id="c2ae4-117">Die folgende Beziehung muss ebenfalls enthalten:</span><span class="sxs-lookup"><span data-stu-id="c2ae4-117">The following relationship must also hold:</span></span>

``` syntax
0 <= first_is <= max_is
```

<span data-ttu-id="c2ae4-118">Die folgende Beziehung muss enthalten sein, wenn **\[** Max **\] <= 0** [**\_ ist**](max-is.md) :</span><span class="sxs-lookup"><span data-stu-id="c2ae4-118">The following relationship must hold when **\[**[**max\_is**](max-is.md)**\] <= 0:**</span></span>

``` syntax
first_is == 0
```

<span data-ttu-id="c2ae4-119">Das **\[ erste \_ is \]** -Attribut kann nicht gleichzeitig mit dem **\[** [**String**](string.md) -Attribut verwendet werden **\]** .</span><span class="sxs-lookup"><span data-stu-id="c2ae4-119">The **\[first\_is\]** attribute cannot be used at the same time as the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="c2ae4-120">Die Verwendung eines konstanten Ausdrucks mit dem **\[ ersten \_ is \]** -Attribut ist eine ungeeignete Verwendung des-Attributs.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-120">Using a constant expression with the **\[first\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="c2ae4-121">Dies ist zulässig, aber ineffizient und führt zu einem langsameren Marshallingcode.</span><span class="sxs-lookup"><span data-stu-id="c2ae4-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

## <a name="examples"></a><span data-ttu-id="c2ae4-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2ae4-122">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a><span data-ttu-id="c2ae4-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2ae4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ae4-124">Feld \_ Attribute</span><span class="sxs-lookup"><span data-stu-id="c2ae4-124">field\_attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="c2ae4-125">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="c2ae4-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c2ae4-126">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="c2ae4-126">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="c2ae4-127">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="c2ae4-127">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="c2ae4-128">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="c2ae4-128">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="c2ae4-129">**Min \_ ist**</span><span class="sxs-lookup"><span data-stu-id="c2ae4-129">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="c2ae4-130">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="c2ae4-130">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="c2ae4-131">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2ae4-131">**string**</span></span>](string.md)
</dt> </dl>

 

 