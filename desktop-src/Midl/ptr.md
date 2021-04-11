---
title: ptr-Attribut
description: Das Attribut \ PTR \ legt einen Zeiger als vollständigen Zeiger fest.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- PTR-Attribut-Mittel l
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314799"
---
# <a name="ptr-attribute"></a><span data-ttu-id="6d21d-104">ptr-Attribut</span><span class="sxs-lookup"><span data-stu-id="6d21d-104">ptr attribute</span></span>

<span data-ttu-id="6d21d-105">Das **\[ ptr \]** -Attribut legt einen Zeiger als vollständigen Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="6d21d-105">The **\[ptr\]** attribute designates a pointer as a full pointer.</span></span>

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="6d21d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d21d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d21d-107">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="6d21d-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-108">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d21d-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="6d21d-109">Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md)oder **\[ ptr \]**; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="6d21d-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md), or **\[ptr\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="6d21d-110">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="6d21d-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-111">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="6d21d-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-112">Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="6d21d-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="6d21d-113">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d21d-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-114">*Standard-declarator*</span><span class="sxs-lookup"><span data-stu-id="6d21d-114">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-115">Gibt einen Standard-C-Deklarator an, z. b. einen Bezeichner, einen zeigerdeklarator oder einen Arraydeklarator.</span><span class="sxs-lookup"><span data-stu-id="6d21d-115">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="6d21d-116">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="6d21d-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-117">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="6d21d-117">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-118">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="6d21d-118">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="6d21d-119">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="6d21d-119">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="6d21d-120">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="6d21d-120">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="6d21d-121">Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.</span><span class="sxs-lookup"><span data-stu-id="6d21d-121">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-122">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="6d21d-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-123">Gibt 0 (null) oder mehr Feld Attribute an, die für den Struktur-oder Union-Member oder Funktionsparameter gelten.</span><span class="sxs-lookup"><span data-stu-id="6d21d-123">Specifies zero or more field attributes that apply to the structure or union member or function parameter.</span></span> <span data-ttu-id="6d21d-124">Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage-Attribute **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** und **\[** [**context \_ handle**](context-handle.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[ \] ptr** und der Typ des Union-Attribut **\[** [**Schalters \_**](switch-type.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="6d21d-124">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="6d21d-125">Trennen Sie mehrere Feld Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="6d21d-125">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-126">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="6d21d-126">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-127">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="6d21d-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="6d21d-128">Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="6d21d-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-129">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="6d21d-129">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-130">Gibt mindestens einen zeigerdeklarator an, auf den das **\[ ptr \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d21d-130">Specifies at least one pointer declarator to which the **\[ptr\]** attribute applies.</span></span> <span data-ttu-id="6d21d-131">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6d21d-131">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-132">*function-name*</span><span class="sxs-lookup"><span data-stu-id="6d21d-132">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-133">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="6d21d-133">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="6d21d-134">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="6d21d-134">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d21d-135">Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="6d21d-135">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="6d21d-136">Parameter Attribute können die direktionalen Attribute [**ein-und**](in.md) [**Auslagern**](out-idl.md). die Feld Attribute [**\_ sind zuerst**](first-is.md), "Last", "length", " [**Max \_ is**](max-is.md)" [**\_**](last-is.md), "size" und " [**Switch \_ Type**](switch-type.md)", "Pointer Attribute [**ref**](ref.md)", " [**Unique**](unique.md)" oder " **\[ ptr \]**" und das [**Kontext \_ handle**](context-handle.md) und die [**Zeichenfolge**](string.md)der Verwendungs Attribute. [**\_**](length-is.md) [**\_**](size-is.md)</span><span class="sxs-lookup"><span data-stu-id="6d21d-136">Parameter attributes can take the directional attributes [**in**](in.md) and [**out**](out-idl.md); the field attributes [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**length\_is**](length-is.md), [**max\_is**](max-is.md), [**size\_is**](size-is.md), and [**switch\_type**](switch-type.md); the pointer attribute [**ref**](ref.md), [**unique**](unique.md), or **\[ptr\]**; and the usage attributes [**context\_handle**](context-handle.md) and [**string**](string.md).</span></span> <span data-ttu-id="6d21d-137">Das Usage-Attribut " [**Ignore**](ignore.md) " kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d21d-137">The usage attribute [**ignore**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="6d21d-138">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="6d21d-138">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d21d-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d21d-139">Remarks</span></span>

<span data-ttu-id="6d21d-140">Der durch das **\[ ptr \]** -Attribut festgelegte vollständige Zeiger nähert sich der vollständigen Funktionalität des C-sprach Zeigers.</span><span class="sxs-lookup"><span data-stu-id="6d21d-140">The full pointer designated by the **\[ptr\]** attribute approaches the full functionality of the C-language pointer.</span></span> <span data-ttu-id="6d21d-141">Der vollständige Zeiger kann den Wert **null** aufweisen und sich während des Aufrufes von **null** in einen nicht-**null**-Wert ändern.</span><span class="sxs-lookup"><span data-stu-id="6d21d-141">The full pointer can have the value **NULL** and can change during the call from **NULL** to non-**NULL**.</span></span> <span data-ttu-id="6d21d-142">Speicher, auf den von vollständigen Zeigern verwiesen wird, kann von anderen Namen in der Anwendung erreicht werden, die Aliasing und Zyklen unterstützen</span><span class="sxs-lookup"><span data-stu-id="6d21d-142">Storage pointed to by full pointers can be reached by other names in the application supporting aliasing and cycles.</span></span> <span data-ttu-id="6d21d-143">Diese Funktionalität erfordert während eines Remote Prozedur Aufrufes mehr Aufwand, um die Daten zu identifizieren, auf die der Zeiger verweist, um zu bestimmen, ob der Wert **null** ist, und um zu ermitteln, ob zwei Zeiger auf dieselben Daten zeigen.</span><span class="sxs-lookup"><span data-stu-id="6d21d-143">This functionality requires more overhead during a remote procedure call to identify the data referred to by the pointer, determine whether the value is **NULL**, and to discover if two pointers point to the same data.</span></span>

<span data-ttu-id="6d21d-144">Vollständige Zeiger verwenden für:</span><span class="sxs-lookup"><span data-stu-id="6d21d-144">Use full pointers for:</span></span>

-   <span data-ttu-id="6d21d-145">Remote Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="6d21d-145">Remote return values.</span></span>
-   <span data-ttu-id="6d21d-146">Doppelte Zeiger, wenn die Größe eines Ausgabe Parameters nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6d21d-146">Double pointers, when the size of an output parameter is not known.</span></span>
-   <span data-ttu-id="6d21d-147">**Null** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6d21d-147">**NULL** pointers.</span></span>

<span data-ttu-id="6d21d-148">Vollständige (und eindeutige) Zeiger können nicht verwendet werden, um die Größe eines Arrays oder einer Union zu beschreiben, da diese Zeiger den Wert **null** haben können.</span><span class="sxs-lookup"><span data-stu-id="6d21d-148">Full (and unique) pointers cannot be used to describe the size of an array or union because these pointers can have the value **NULL**.</span></span> <span data-ttu-id="6d21d-149">Diese Einschränkung durch das Mittel l verhindert einen Fehler, der auftreten kann, wenn ein **null** -Wert als Größe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d21d-149">This restriction by MIDL prevents an error that can result when a **NULL** value is used as the size.</span></span>

<span data-ttu-id="6d21d-150">Bei Verweis-und eindeutigen Zeigern wird davon ausgegangen, dass keine Daten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6d21d-150">Reference and unique pointers are assumed to cause no aliasing of data.</span></span> <span data-ttu-id="6d21d-151">Ein gerichtetes Diagramm, das durch das Starten eines eindeutigen oder Verweis Zeigers abgerufen wird und nur eindeutige Verweise oder Verweis Zeiger enthält, enthält weder eine erneute Konvergenz noch Zyklen.</span><span class="sxs-lookup"><span data-stu-id="6d21d-151">A directed graph obtained by starting from a unique or reference pointer and following only unique or reference pointers contains neither reconvergence nor cycles.</span></span>

<span data-ttu-id="6d21d-152">Um Aliasing zu vermeiden, sollten alle Zeiger Werte von einem Eingabe Zeiger der gleichen Klasse des Zeigers abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d21d-152">To avoid aliasing, all pointer values should be obtained from an input pointer of the same class of pointer.</span></span> <span data-ttu-id="6d21d-153">Wenn mehr als ein Zeiger auf denselben Speicherort verweist, müssen alle Zeiger vollständig Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="6d21d-153">If more than one pointer points to the same memory location, all such pointers must be full pointers.</span></span>

<span data-ttu-id="6d21d-154">In einigen Fällen können vollständige und eindeutige Zeiger gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="6d21d-154">In some cases, full and unique pointers can be mixed.</span></span> <span data-ttu-id="6d21d-155">Einem vollständigen Zeiger kann der Wert eines eindeutigen Zeigers zugewiesen werden, solange die Zuweisung nicht gegen die Einschränkungen bei der Änderung des Werts eines eindeutigen Zeigers verstößt.</span><span class="sxs-lookup"><span data-stu-id="6d21d-155">A full pointer can be assigned the value of a unique pointer, as long as the assignment does not violate the restrictions on changing the value of a unique pointer.</span></span> <span data-ttu-id="6d21d-156">Wenn Sie jedoch einen eindeutigen Zeiger auf den Wert eines vollständigen Zeigers zuweisen, können Sie Aliasing auslösen.</span><span class="sxs-lookup"><span data-stu-id="6d21d-156">However, when you assign a unique pointer the value of a full pointer, you may cause aliasing.</span></span>

<span data-ttu-id="6d21d-157">Das Kombinieren von vollständigen und eindeutigen Zeigern kann Aliasing verursachen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="6d21d-157">Mixing full and unique pointers can cause aliasing, as demonstrated in the following example:</span></span>

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

<span data-ttu-id="6d21d-158">Obwohl "t->Left" und "t->right" auf eindeutige Speicherorte verweisen, sind "t->Left->pData" und "t->right->pData" ein Alias.</span><span class="sxs-lookup"><span data-stu-id="6d21d-158">Although "t->left" and "t->right" point to unique memory locations, "t->left->pdata" and "t->right->pdata" are aliased.</span></span> <span data-ttu-id="6d21d-159">Aus diesem Grund müssen Aliasing-Unterstützungs Algorithmen allen Zeigern folgen (einschließlich eindeutiger Verweis Zeiger und Verweis Zeiger), die schließlich möglicherweise einen vollständigen Zeiger erreichen.</span><span class="sxs-lookup"><span data-stu-id="6d21d-159">For this reason, aliasing-support algorithms must follow all pointers (including unique and reference pointers) that may eventually reach a full pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="6d21d-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d21d-160">Examples</span></span>

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="6d21d-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d21d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d21d-162">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="6d21d-162">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="6d21d-163">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="6d21d-163">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="6d21d-164">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="6d21d-164">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d21d-165">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="6d21d-165">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="6d21d-166">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="6d21d-166">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="6d21d-167">**const**</span><span class="sxs-lookup"><span data-stu-id="6d21d-167">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="6d21d-168">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="6d21d-168">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="6d21d-169">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6d21d-169">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="6d21d-170">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6d21d-170">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="6d21d-171">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="6d21d-171">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="6d21d-172">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="6d21d-172">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6d21d-173">**lassen**</span><span class="sxs-lookup"><span data-stu-id="6d21d-173">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="6d21d-174">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6d21d-174">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="6d21d-175">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6d21d-175">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="6d21d-176">**nah**</span><span class="sxs-lookup"><span data-stu-id="6d21d-176">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="6d21d-177">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6d21d-177">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="6d21d-178">**Zeiger \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="6d21d-178">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="6d21d-179">**ref**</span><span class="sxs-lookup"><span data-stu-id="6d21d-179">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="6d21d-180">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="6d21d-180">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="6d21d-181">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6d21d-181">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="6d21d-182">**struct**</span><span class="sxs-lookup"><span data-stu-id="6d21d-182">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="6d21d-183">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="6d21d-183">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="6d21d-184">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="6d21d-184">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="6d21d-185">**Union**</span><span class="sxs-lookup"><span data-stu-id="6d21d-185">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="6d21d-186">**gem**</span><span class="sxs-lookup"><span data-stu-id="6d21d-186">**unique**</span></span>](unique.md)
</dt> </dl>

 

 