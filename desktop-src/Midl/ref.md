---
title: ref-Attribut
description: Das Attribut \ Ref \ identifiziert einen Verweis Zeiger. Es wird lediglich verwendet, um eine Dereferenzierungsebene darzustellen.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- Verweis Attribut-Mittel l
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858185"
---
# <a name="ref-attribute"></a><span data-ttu-id="b183c-105">ref-Attribut</span><span class="sxs-lookup"><span data-stu-id="b183c-105">ref attribute</span></span>

<span data-ttu-id="b183c-106">Das **\[ ref \]** -Attribut identifiziert einen Verweis Zeiger.</span><span class="sxs-lookup"><span data-stu-id="b183c-106">The **\[ref\]** attribute identifies a reference pointer.</span></span> <span data-ttu-id="b183c-107">Es wird lediglich verwendet, um eine Dereferenzierungsebene darzustellen.</span><span class="sxs-lookup"><span data-stu-id="b183c-107">It is used simply to represent a level of indirection.</span></span>

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="b183c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b183c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b183c-109">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b183c-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-110">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b183c-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="b183c-111">Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribute **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b183c-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attributes **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="b183c-112">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="b183c-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-113">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="b183c-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-114">Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="b183c-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="b183c-115">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b183c-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-116">*Standard-declarator*</span><span class="sxs-lookup"><span data-stu-id="b183c-116">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-117">Gibt einen Standard-C-Deklarator an, z. b. einen Bezeichner, einen zeigerdeklarator oder einen Arraydeklarator.</span><span class="sxs-lookup"><span data-stu-id="b183c-117">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="b183c-118">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="b183c-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="b183c-119">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="b183c-119">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-120">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="b183c-120">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="b183c-121">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="b183c-121">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="b183c-122">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="b183c-122">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="b183c-123">Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.</span><span class="sxs-lookup"><span data-stu-id="b183c-123">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-124">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b183c-124">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-125">Gibt 0 (null) oder mehr Feld Attribute an, die für die Struktur, den Union-Member oder den Funktionsparameter gelten.</span><span class="sxs-lookup"><span data-stu-id="b183c-125">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="b183c-126">Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage-Attribute **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** und **\[** [**context \_ handle**](context-handle.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und der Typ des Union-Attribut **\[** [**Schalters \_**](switch-type.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b183c-126">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="b183c-127">Trennen Sie mehrere Feld Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="b183c-127">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-128">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b183c-128">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-129">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="b183c-129">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="b183c-130">Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b183c-130">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-131">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="b183c-131">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-132">Gibt mindestens einen zeigerdeklarator an, auf den das **\[ ref \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b183c-132">Specifies at least one pointer declarator to which the **\[ref\]** attribute applies.</span></span> <span data-ttu-id="b183c-133">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b183c-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="b183c-134">*function-name*</span><span class="sxs-lookup"><span data-stu-id="b183c-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-135">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="b183c-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-136">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b183c-136">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b183c-137">Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="b183c-137">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="b183c-138">Parameter Attribute können die direktionalen **\[** [**Attribute ein**](in.md) **\]** -und **\[** [](out-idl.md) **\]** ausschalten. die Feld Attribute **\[** [**\_ sind zuerst**](first-is.md), "Last", " **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**length \_**](length-is.md)" **\]** , " **\[** [**Max \_ is**](max-is.md)" **\]** , "size" und " **\[** [**\_**](size-is.md) **\]** **\[** [**Switch \_ Type**](switch-type.md)", **\]** das Zeiger Attribut " **\[ \] ref**", " **\[** [**Unique**](unique.md)" **\]** oder " **\[** [**ptr**](ptr.md)" **\]** und das **\[** [**Kontext \_ handle**](context-handle.md) und die **\]** **\[** [**Zeichenfolge**](string.md) **\]** der Verwendungs Attribute</span><span class="sxs-lookup"><span data-stu-id="b183c-138">Parameter attributes can take the directional attributes **\[**[**in**](in.md)**\]** and **\[**[**out**](out-idl.md)**\]**; the field attributes **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, and **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]** and **\[**[**string**](string.md)**\]**.</span></span> <span data-ttu-id="b183c-139">Das Usage-Attribut " **\[** [**Ignore**](ignore.md) " **\]** kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b183c-139">The usage attribute **\[**[**ignore**](ignore.md)**\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="b183c-140">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="b183c-140">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b183c-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b183c-141">Remarks</span></span>

<span data-ttu-id="b183c-142">Ein Zeiger Attribut kann als Type-Attribut, als Feld Attribut, das auf einen Strukturmember, Union-Member oder Parameter angewendet wird, angewendet werden. oder als Funktions Attribut, das für den Funktions Rückgabetyp gilt.</span><span class="sxs-lookup"><span data-stu-id="b183c-142">A pointer attribute can be applied as a type attribute, as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="b183c-143">Das Zeiger Attribut kann auch mit dem **\[** [**Zeiger \_ default**](pointer-default.md) - **\]** Schlüsselwort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b183c-143">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="b183c-144">Ein Verweis Zeiger hat die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b183c-144">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="b183c-145">Verweist immer auf einen gültigen Speicherplatz. hat nie den Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="b183c-145">Always points to valid storage; never has the value **NULL**.</span></span> <span data-ttu-id="b183c-146">Ein Verweis Zeiger kann immer dereferenziert werden.</span><span class="sxs-lookup"><span data-stu-id="b183c-146">A reference pointer can always be dereferenced.</span></span>
-   <span data-ttu-id="b183c-147">Ändert sich nie während eines Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="b183c-147">Never changes during a call.</span></span> <span data-ttu-id="b183c-148">Ein Verweis Zeiger zeigt vor und nach dem-Befehl immer auf den gleichen Speicher auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="b183c-148">A reference pointer always points to the same storage on the client before and after the call.</span></span>
-   <span data-ttu-id="b183c-149">Weist keinen neuen Arbeitsspeicher auf dem Client zu.</span><span class="sxs-lookup"><span data-stu-id="b183c-149">Does not allocate new memory on the client.</span></span> <span data-ttu-id="b183c-150">Die vom Server zurückgegebenen Daten werden in den vorhandenen Speicher geschrieben, der durch den Wert des Verweis Zeigers vor dem-Befehl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b183c-150">Data returned from the server is written into existing storage specified by the value of the reference pointer before the call.</span></span>
-   <span data-ttu-id="b183c-151">Führt nicht zum Aliasing.</span><span class="sxs-lookup"><span data-stu-id="b183c-151">Does not cause aliasing.</span></span> <span data-ttu-id="b183c-152">Speicher, auf den von einem Verweis Zeiger verwiesen wird, kann nicht von einem anderen Namen in der Funktion erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="b183c-152">Storage pointed to by a reference pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="b183c-153">Ein Verweis Zeiger kann nicht als Typ eines Zeigers verwendet werden, der von einer Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b183c-153">A reference pointer cannot be used as the type of a pointer returned by a function.</span></span>

<span data-ttu-id="b183c-154">Wenn für einen Zeiger Parameter der obersten Ebene kein Attribut angegeben ist, wird es als Verweis Zeiger behandelt.</span><span class="sxs-lookup"><span data-stu-id="b183c-154">If no attribute is specified for a top-level pointer parameter, it is treated as a reference pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="b183c-155">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b183c-155">Examples</span></span>

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a><span data-ttu-id="b183c-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b183c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b183c-157">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="b183c-157">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="b183c-158">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="b183c-158">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="b183c-159">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="b183c-159">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b183c-160">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="b183c-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b183c-161">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="b183c-161">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="b183c-162">**const**</span><span class="sxs-lookup"><span data-stu-id="b183c-162">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="b183c-163">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="b183c-163">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="b183c-164">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="b183c-164">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="b183c-165">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="b183c-165">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="b183c-166">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="b183c-166">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="b183c-167">**lassen**</span><span class="sxs-lookup"><span data-stu-id="b183c-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="b183c-168">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="b183c-168">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="b183c-169">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="b183c-169">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="b183c-170">**nah**</span><span class="sxs-lookup"><span data-stu-id="b183c-170">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="b183c-171">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="b183c-171">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="b183c-172">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="b183c-172">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="b183c-173">**ptr**</span><span class="sxs-lookup"><span data-stu-id="b183c-173">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="b183c-174">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="b183c-174">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="b183c-175">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b183c-175">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="b183c-176">**struct**</span><span class="sxs-lookup"><span data-stu-id="b183c-176">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="b183c-177">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="b183c-177">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="b183c-178">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="b183c-178">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="b183c-179">**Union**</span><span class="sxs-lookup"><span data-stu-id="b183c-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="b183c-180">**gem**</span><span class="sxs-lookup"><span data-stu-id="b183c-180">**unique**</span></span>](unique.md)
</dt> </dl>

 

 