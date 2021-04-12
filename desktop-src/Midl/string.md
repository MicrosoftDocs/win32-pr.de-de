---
title: Zeichenfolgeattribut
description: Das Attribut \ String \ gibt an, dass das eindimensionale Char-, WCHAR \_ t-, Bytearray-Array oder der-Zeiger auf ein solches Array als Zeichenfolge behandelt werden muss.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- Zeichen folgen Attribut-Mittel l
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948691"
---
# <a name="string-attribute"></a><span data-ttu-id="4462f-104">Zeichenfolgeattribut</span><span class="sxs-lookup"><span data-stu-id="4462f-104">string attribute</span></span>

<span data-ttu-id="4462f-105">Das **\[ String \]** -Attribut gibt an, dass das eindimensionale [**char**](char-idl.md)-, [**WCHAR \_ t**](wchar-t.md)-, [**Bytearray**](byte.md) -Array oder der-Zeiger auf ein solches Array als Zeichenfolge behandelt werden muss.</span><span class="sxs-lookup"><span data-stu-id="4462f-105">The **\[string\]** attribute indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array or the pointer to such an array must be treated as a string.</span></span> <span data-ttu-id="4462f-106">Die Zeichenfolge kann auch ein Array (oder ein Zeiger auf ein Array) der Konstrukte sein, deren Felder alle vom Typ **Byte** sind.</span><span class="sxs-lookup"><span data-stu-id="4462f-106">The string can also be an array (or a pointer to an array) of constructs whose fields are all of the type **byte**.</span></span>

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a><span data-ttu-id="4462f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4462f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4462f-108">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4462f-108">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-109">Gibt ein oder mehrere Attribute an, die auf einen Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4462f-109">Specifies one or more attributes that apply to a type.</span></span> <span data-ttu-id="4462f-110">Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[ String \]** und **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4462f-110">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[string\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="4462f-111">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4462f-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4462f-112">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="4462f-112">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-113">Gibt einen [Basistyp](midl-base-types.md), [**Strukturtyp oder**](struct.md) Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="4462f-113">Specifies a [base type](midl-base-types.md), [**struct**](struct.md) type, or type identifier.</span></span> <span data-ttu-id="4462f-114">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4462f-114">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="4462f-115">*Standard-declarator*</span><span class="sxs-lookup"><span data-stu-id="4462f-115">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-116">Gibt einen Standard-C-Deklarator an, z. b. einen Bezeichner, einen zeigerdeklarator oder einen Arraydeklarator.</span><span class="sxs-lookup"><span data-stu-id="4462f-116">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="4462f-117">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4462f-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="4462f-118">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="4462f-118">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-119">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="4462f-119">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="4462f-120">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4462f-120">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="4462f-121">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="4462f-121">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="4462f-122">Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.</span><span class="sxs-lookup"><span data-stu-id="4462f-122">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4462f-123">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4462f-123">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-124">Gibt 0 (null) oder mehr Feld Attribute an, die für die Struktur, den Union-Member oder den Funktionsparameter gelten.</span><span class="sxs-lookup"><span data-stu-id="4462f-124">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="4462f-125">Die zwei gültigen Feld Attribute sind **\[** [**Max \_ is**](max-is.md) , **\]** und **\[** [**size \_ ist**](size-is.md), **\]** die **\[ Zeichenfolge \]** der Verwendungs Attribute, das **\[ ignorieren \]** und das **\[ Kontext \_ \] handle**, das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** oder **\[** [**ptr**](ptr.md) **\]** und der **\[ \_ Typ \]** des Union-Attribut Schalters.</span><span class="sxs-lookup"><span data-stu-id="4462f-125">The two valid field attributes are **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**, the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**, and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="4462f-126">Trennen Sie mehrere Feld Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4462f-126">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4462f-127">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4462f-127">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-128">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="4462f-128">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="4462f-129">Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ Kontext \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="4462f-129">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="4462f-130">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="4462f-130">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-131">Gibt einen optionalen zeigerdeklarator an, auf den das **\[ Zeichen \]** folgen Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4462f-131">Specifies an optional pointer declarator to which the **\[string\]** attribute applies.</span></span> <span data-ttu-id="4462f-132">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4462f-132">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="4462f-133">*function-name*</span><span class="sxs-lookup"><span data-stu-id="4462f-133">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-134">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="4462f-134">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="4462f-135">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4462f-135">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4462f-136">Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="4462f-136">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="4462f-137">Parameter Attribute können die direktionalen **\[ Attribute \] ein-und** **\[ \] Auschecken**; die Feld Attribute **\[** [**Max \_ ist**](max-is.md) **\]** , und **\[** [**size \_ ist**](size-is.md) **\]** , das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ ptr \]** und das **\[ Kontext \_ handle \]** und die **\[ Zeichenfolge \]** der Verwendungs Attribute.</span><span class="sxs-lookup"><span data-stu-id="4462f-137">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="4462f-138">Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4462f-138">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="4462f-139">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4462f-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4462f-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4462f-140">Remarks</span></span>

<span data-ttu-id="4462f-141">Wenn das **\[ Zeichen \]** folgen Attribut mit einem Array verwendet wird, dessen Begrenzungen zur Laufzeit bestimmt werden, müssen Sie auch **\[ \_ \] eine Size** -oder **\[ Max \_ is \]** -Attribut angeben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4462f-141">If the **\[string\]** attribute is used with an array whose bounds are determined at run time, you must also specify a **\[size\_is\]** or **\[max\_is\]** attribute, as in the following example:</span></span>

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

<span data-ttu-id="4462f-142">Das **\[ String \]** -Attribut kann nicht mit Attributen verwendet werden, die den Bereich der übertragenen Elemente angeben, z. b. **\[ First \_ is \]**, **\[ Last \_ is \]** und **\[ length \_ ist \]**.</span><span class="sxs-lookup"><span data-stu-id="4462f-142">The **\[string\]** attribute cannot be used with attributes that specify the range of transmitted elements, such as **\[first\_is\]**, **\[last\_is\]**, and **\[length\_is\]**.</span></span>

<span data-ttu-id="4462f-143">Bei Verwendung in mehrdimensionalen Arrays gilt das **\[ Zeichen \]** folgen Attribut für das äußteste ganz rechts.</span><span class="sxs-lookup"><span data-stu-id="4462f-143">When used on multidimensional arrays, the **\[string\]** attribute applies to the rightmost array.</span></span>

<span data-ttu-id="4462f-144">Verwenden Sie zum Definieren einer gezählten Zeichenfolge nicht das **\[ String \]** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="4462f-144">To define a counted string, do not use the **\[string\]** attribute.</span></span> <span data-ttu-id="4462f-145">Verwenden Sie ein Zeichen Array oder einen Zeichen basierten Zeiger wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="4462f-145">Use a character array or character-based pointer such as the following:</span></span>

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

<span data-ttu-id="4462f-146">Das **\[ String \]** -Attribut gibt an, dass der Stub eine von der Sprache bereitgestellte Methode verwenden soll, um die Länge von Zeichen folgen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4462f-146">The **\[string\]** attribute specifies that the stub should use a language-supplied method to determine the length of strings.</span></span>

<span data-ttu-id="4462f-147">Beim Deklarieren von Zeichen folgen in C müssen Sie Speicherplatz für ein zusätzliches Zeichen zuweisen, das das Ende der Zeichenfolge markiert.</span><span class="sxs-lookup"><span data-stu-id="4462f-147">When declaring strings in C, you must allocate space for an extra character that marks the end of the string.</span></span>

## <a name="examples"></a><span data-ttu-id="4462f-148">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4462f-148">Examples</span></span>

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a><span data-ttu-id="4462f-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4462f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4462f-150">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="4462f-150">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="4462f-151">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="4462f-151">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4462f-152">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="4462f-152">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="4462f-153">**Char**</span><span class="sxs-lookup"><span data-stu-id="4462f-153">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="4462f-154">**const**</span><span class="sxs-lookup"><span data-stu-id="4462f-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="4462f-155">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="4462f-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="4462f-156">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="4462f-156">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="4462f-157">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="4462f-157">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="4462f-158">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="4462f-158">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="4462f-159">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="4462f-159">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4462f-160">**lassen**</span><span class="sxs-lookup"><span data-stu-id="4462f-160">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="4462f-161">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="4462f-161">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="4462f-162">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="4462f-162">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="4462f-163">**nah**</span><span class="sxs-lookup"><span data-stu-id="4462f-163">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="4462f-164">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="4462f-164">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="4462f-165">**Zeiger \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="4462f-165">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="4462f-166">**ptr**</span><span class="sxs-lookup"><span data-stu-id="4462f-166">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="4462f-167">**ref**</span><span class="sxs-lookup"><span data-stu-id="4462f-167">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="4462f-168">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="4462f-168">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="4462f-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="4462f-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="4462f-170">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="4462f-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="4462f-171">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="4462f-171">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="4462f-172">**Union**</span><span class="sxs-lookup"><span data-stu-id="4462f-172">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="4462f-173">**gem**</span><span class="sxs-lookup"><span data-stu-id="4462f-173">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="4462f-174">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="4462f-174">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 