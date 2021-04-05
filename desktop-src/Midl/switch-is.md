---
title: switch_is-Attribut
description: Der \ Switch \_ is \ Attribute gibt den Ausdruck oder den Bezeichner an, der als uniondiskriminant fungiert, der das Unionmember auswählt.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- Switch_is Attribut-Mittel l
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948222"
---
# <a name="switch_is-attribute"></a><span data-ttu-id="f9fa6-104">Switch \_ ist Attribut</span><span class="sxs-lookup"><span data-stu-id="f9fa6-104">switch\_is attribute</span></span>

<span data-ttu-id="f9fa6-105">Der **\[ Switch \_ is \]** Attribute gibt den Ausdruck oder den Bezeichner an, der als uniondiskriminant fungiert, der das Unionmember auswählt.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-105">The **\[switch\_is\]** attribute specifies the expression or identifier acting as the union discriminant that selects the union member.</span></span>

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="f9fa6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9fa6-107">*struct-Tag*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-108">Gibt ein optionales Tag für eine Struktur an.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-108">Specifies an optional tag for a structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-109">*Limited-expr*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-109">*limited-expr*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-110">Gibt einen von der Mittel l unterstützten C-sprach Ausdruck an.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-110">Specifies a C-language expression supported by MIDL.</span></span> <span data-ttu-id="f9fa6-111">Fast alle C-sprach Ausdrücke werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-111">Almost all C-language expressions are supported.</span></span> <span data-ttu-id="f9fa6-112">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="f9fa6-113">Die Mittel l lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Pre-und Post-Increment-und Pre-und Post-Dekrement-Operatoren zu.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-113">MIDL does not allow function invocations in expressions and does not allow pre- and post-increment and pre- and post-decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-114">*Field-attr-List*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-114">*field-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-115">Gibt 0 (null) oder mehr Feld Attribute an, die für ein Union-Element gelten.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-115">Specifies zero or more field attributes that apply to a union member.</span></span> <span data-ttu-id="f9fa6-116">Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md), **\]** **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage **\[** -Attribut [**Zeichenfolge**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** und **\[** das [**Kontext \_ handle**](context-handle.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und für Member, die selbst Unions sind, der **\[** [**\_ Switchtyp**](switch-type.md)des Union-Attributs **\]** .</span><span class="sxs-lookup"><span data-stu-id="f9fa6-116">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and for members that are themselves unions, the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="f9fa6-117">Trennen Sie mehrere Feld Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-117">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-118">*Union-type-specifier*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-118">*union-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-119">Gibt den [**Union**](union.md) -Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-119">Specifies the [**union**](union.md) type identifier.</span></span> <span data-ttu-id="f9fa6-120">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-120">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-121">*Deklarator und Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-122">Gibt einen C-Standard Deklarator an, z. b. einen Bezeichner, einen zeigerdeklarator und einen Arraydeklarator.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-122">Specifies a standard C declarator, such as an identifier, pointer declarator, and array declarator.</span></span> <span data-ttu-id="f9fa6-123">(Funktions Deklaratoren und Bitfeld Deklarationen sind in Unions nicht zulässig, die in Remote Prozedur aufrufen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-123">(Function declarators and bit-field declarations are not allowed in unions that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="f9fa6-124">Diese Deklaratoren sind in Unions zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-124">These declarators are allowed in unions that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-125">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-126">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="f9fa6-127">Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ Kontext \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-128">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-128">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-129">Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-129">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="f9fa6-130">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-130">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-131">*Zeiger-Deklarator*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-131">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-132">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-132">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="f9fa6-133">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-134">*function-name*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-135">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-136">*param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-137">Gibt NULL oder mehr Attribute an, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-137">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="f9fa6-138">Parameter Attribute können die direktionalen **\[ Attribute \] ein-und** **\[ \]** **\[ \]** **\[ \_ \]** **\[ \] ausschalten, die** Feld Attribute **\[ \_ \] sind zuerst** **\[ \_ \] , "** Last", "length", " **\[ Max \_ \] is**", " **\[ size" \_ und "Switch Type", das Zeiger Attribut "ref", "Unique" oder "PTR" und das Kontext Handle und die Zeichenfolge der Verwendungs Attribute \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-138">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**, the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="f9fa6-139">Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-139">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="f9fa6-140">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-140">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f9fa6-141">*Union-Type*</span><span class="sxs-lookup"><span data-stu-id="f9fa6-141">*union-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fa6-142">Identifiziert den [**Union**](union.md) -Typspezifizierer.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-142">Identifies the [**union**](union.md) type specifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9fa6-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9fa6-143">Remarks</span></span>

<span data-ttu-id="f9fa6-144">Der dem **\[ Switch \_ \]** zugeordnete diskriminant muss auf derselben logischen Ebene wie die Union definiert werden:</span><span class="sxs-lookup"><span data-stu-id="f9fa6-144">The discriminant associated with the **\[switch\_is\]** attribute must be defined at the same logical level as the union:</span></span>

-   <span data-ttu-id="f9fa6-145">Wenn die Union ein Parameter ist, muss der Union-diskriminant ein anderer Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-145">When the union is a parameter, the union discriminant must be another parameter.</span></span>
-   <span data-ttu-id="f9fa6-146">Wenn die Union ein Feld einer Struktur ist, muss die Diskriminante ein anderes Feld derselben Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-146">When the union is a field of a structure, the discriminant must be another field of the same structure.</span></span>

<span data-ttu-id="f9fa6-147">Die Sequenz in einer Struktur oder einer Funktionsparameter Liste ist nicht signifikant.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-147">The sequence in a structure or a function parameter list is not significant.</span></span> <span data-ttu-id="f9fa6-148">Die Union kann dem Diskriminanten vorangestellt oder folgen.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-148">The union can either precede or follow the discriminant.</span></span>

<span data-ttu-id="f9fa6-149">Der **\[ Switch \_ is \]** -Attribut kann als Feld Attribut oder als Parameter Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f9fa6-149">The **\[switch\_is\]** attribute can appear as a field attribute or as a parameter attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="f9fa6-150">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9fa6-150">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="f9fa6-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9fa6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fa6-152">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="f9fa6-152">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-153">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-153">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-154">**const**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-155">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-156">Gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="f9fa6-156">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-157">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-157">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-158">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-158">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-159">**lassen**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-159">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-160">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-160">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-161">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-161">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-162">**nah**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-162">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-163">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-163">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-164">Nicht gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="f9fa6-164">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-165">**ptr**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-165">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-166">**ref**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-166">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-167">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-167">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-168">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-168">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-170">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-171">**Union**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-171">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="f9fa6-172">**gem**</span><span class="sxs-lookup"><span data-stu-id="f9fa6-172">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




