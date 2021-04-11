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
# <a name="max_is-attribute"></a><span data-ttu-id="48b78-104">Max \_ ist Attribut</span><span class="sxs-lookup"><span data-stu-id="48b78-104">max\_is attribute</span></span>

<span data-ttu-id="48b78-105">Das **\[ Maximum \_ is \]** -Attribut bestimmt den maximalen Wert für einen gültigen Array Index.</span><span class="sxs-lookup"><span data-stu-id="48b78-105">The **\[max\_is\]** attribute designates the maximum value for a valid array index.</span></span>

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="48b78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48b78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b78-107">*begrenzte Ausdrucks Liste*</span><span class="sxs-lookup"><span data-stu-id="48b78-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="48b78-108">Gibt einen oder mehrere C-sprach Ausdrücke an.</span><span class="sxs-lookup"><span data-stu-id="48b78-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="48b78-109">Jeder Ausdruck ergibt eine ganze Zahl, die den höchsten gültigen Array Index darstellt.</span><span class="sxs-lookup"><span data-stu-id="48b78-109">Each expression evaluates to an integer that represents the highest valid array index.</span></span> <span data-ttu-id="48b78-110">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="48b78-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="48b78-111">"Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.</span><span class="sxs-lookup"><span data-stu-id="48b78-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="48b78-112">Trennen Sie mehrere Ausdrücke durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="48b78-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48b78-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b78-113">Remarks</span></span>

<span data-ttu-id="48b78-114">Das **\[ Maximum \_ is \]** -Attribut entspricht nicht notwendigerweise der Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="48b78-114">The **\[max\_is\]** attribute does not necessarily correspond to the number of elements in the array.</span></span> <span data-ttu-id="48b78-115">Für ein Array der Größe *n* in C, bei dem das erste Array Element die Element Nummer 0 (null) ist, ist der maximale Wert für einen gültigen Array Index *n*– 1.</span><span class="sxs-lookup"><span data-stu-id="48b78-115">For an array of size *n* in C, where the first array element is element number zero, the maximum value for a valid array index is *n*–1.</span></span>

<span data-ttu-id="48b78-116">Das **\[ Maximum \_ is \]** -Attribut kann nicht gleichzeitig als Feld Attribut verwendet werden, wenn die **\[** [**Größe Attribute \_ ist**](size-is.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="48b78-116">The **\[max\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**size\_is**](size-is.md)**\]** attribute.</span></span>

<span data-ttu-id="48b78-117">Obwohl es zulässig ist, das **\[ Maximum \_ is \]** -Attribut mit einem konstanten Ausdruck zu verwenden, ist dies ineffizient und unnötig.</span><span class="sxs-lookup"><span data-stu-id="48b78-117">While it is legal to use the **\[max\_is\]** attribute with a constant expression, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="48b78-118">Verwenden Sie z. b. ein Array mit fester Größe:</span><span class="sxs-lookup"><span data-stu-id="48b78-118">For example, use a fixed size array:</span></span>

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

<span data-ttu-id="48b78-119">Anstelle von:</span><span class="sxs-lookup"><span data-stu-id="48b78-119">instead of:</span></span>

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a><span data-ttu-id="48b78-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48b78-120">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="48b78-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="48b78-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b78-122">Feldattribute</span><span class="sxs-lookup"><span data-stu-id="48b78-122">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="48b78-123">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="48b78-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="48b78-124">**Min \_ ist**</span><span class="sxs-lookup"><span data-stu-id="48b78-124">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="48b78-125">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="48b78-125">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 