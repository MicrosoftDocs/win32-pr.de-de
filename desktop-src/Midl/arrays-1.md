---
title: Arrays-Attribut
description: Arrays sind homogene Auflistungen von Daten, auf die über einen Index oder eine Element Nummer zugegriffen wird
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- Arrays-Attribut-Mittel l
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106337404"
---
# <a name="arrays-attribute"></a><span data-ttu-id="6596d-104">Arrays-Attribut</span><span class="sxs-lookup"><span data-stu-id="6596d-104">arrays attribute</span></span>

<span data-ttu-id="6596d-105">Arrays sind homogene Auflistungen von Daten, auf die über einen Index oder eine Element Nummer zugegriffen wird</span><span class="sxs-lookup"><span data-stu-id="6596d-105">Arrays are homogenous collections of data accessed by an index or element number.</span></span>

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="6596d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6596d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6596d-107">*Type-attr-List*</span><span class="sxs-lookup"><span data-stu-id="6596d-107">*type-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-108">Gibt 0 (null) oder mehr Attribute an, die für den Typ gelten.</span><span class="sxs-lookup"><span data-stu-id="6596d-108">Specifies zero or more attributes that apply to the type.</span></span> <span data-ttu-id="6596d-109">Gültige Typattribute sind [**\[ handle \]**](handle.md), [**\[ \_ Switchtyp \]**](switch-type.md) [**\[ , über \_ Tragung \] als**](transmit-as.md); Zeiger Attribut Verweis, [**\[ eindeutig \]**](unique.md)oder [**\[ \] ptr**](ptr.md); und die Verwendungs Attribute [**\[ Kontext \_ handle \]**](context-handle.md), [**\[ String \]**](string.md)und [**\[ Ignore \]**](ignore.md). [**\[ \]**](ref.md)</span><span class="sxs-lookup"><span data-stu-id="6596d-109">Valid type attributes include [**\[handle\]**](handle.md), [**\[switch\_type\]**](switch-type.md), [**\[transmit\_as\]**](transmit-as.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md), [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md).</span></span> <span data-ttu-id="6596d-110">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="6596d-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="6596d-111">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="6596d-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-112">Gibt den Typbezeichner, Basistyp, [**Struktur**](struct.md), [**Union**](union.md)oder [**Enumeration**](enum.md) -Typ an.</span><span class="sxs-lookup"><span data-stu-id="6596d-112">Specifies the type identifier, base type, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type.</span></span> <span data-ttu-id="6596d-113">Die Typspezifikation kann eine optionale Speicher Spezifikation enthalten.</span><span class="sxs-lookup"><span data-stu-id="6596d-113">The type specification can include an optional storage specification.</span></span>

</dd> <dt>

<span data-ttu-id="6596d-114">*Zeiger-decl*</span><span class="sxs-lookup"><span data-stu-id="6596d-114">*pointer-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-115">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="6596d-115">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="6596d-116">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator, der aus dem Kenn Zeichner erstellt wurde **\*** , Modifizierer, z. b. **weit**, und der Qualifizierer [**Konstanten**](const.md).</span><span class="sxs-lookup"><span data-stu-id="6596d-116">A pointer declarator is the same as the pointer declarator used in C, constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="6596d-117">*Array-declarator*</span><span class="sxs-lookup"><span data-stu-id="6596d-117">*array-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-118">Gibt den Namen des Arrays an, gefolgt von einem der folgenden Konstrukte für jede Dimension des Arrays: "**\[ \]**", " **\[\*\]** ", "**\[ ***Const1*** \]**" oder "**\[ ***Lower...*** Upper \]**"Where *Lower* und *Upper* sind konstante Werte, die die unteren und oberen Begrenzungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="6596d-118">Specifies the name of the array, followed by one of the following constructs for each dimension of the array: "**\[ \]**", "**\[\*\]**", "**\[***const1***\]**", or "**\[***lower...upper***\]**" where *lower* and *upper* are constant values that represent the lower and upper bounds.</span></span> <span data-ttu-id="6596d-119">Die *untere* Konstante muss zu 0 (null) ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="6596d-119">The constant *lower* must evaluate to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6596d-120">*Tag*</span><span class="sxs-lookup"><span data-stu-id="6596d-120">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-121">Gibt ein optionales Tag für die Struktur oder Union an.</span><span class="sxs-lookup"><span data-stu-id="6596d-121">Specifies an optional tag for the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="6596d-122">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="6596d-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-123">Gibt 0 (null) oder mehr Feld Attribute an, die für die Struktur, den Union-Member oder den Funktionsparameter gelten.</span><span class="sxs-lookup"><span data-stu-id="6596d-123">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="6596d-124">Gültige Feld Attribute sind [**\[ First \_ is \]**](first-is.md), [**\[ Last \_ is \]**](last-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md), die Usage-Attribut [**\[ Zeichenfolge \]**](string.md)und [**\[ \] Ignore**](ignore.md); die Zeiger Attribute [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)und [**\[ ptr \]**](ptr.md)sowie der Typ [**\[ \_ \]**](switch-type.md)des Union-Attribut Schalters.</span><span class="sxs-lookup"><span data-stu-id="6596d-124">Valid field attributes include [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md); the usage attributes [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), and [**\[ptr\]**](ptr.md); and the union attribute [**\[switch\_type\]**](switch-type.md).</span></span> <span data-ttu-id="6596d-125">Trennen Sie mehrere Feld Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="6596d-125">Separate multiple field attributes with commas.</span></span> <span data-ttu-id="6596d-126">Beachten Sie, dass die oben aufgeführten Attribute **\[ First \_ is \]**, **\[ Last \_ is \]** und [**\[ Ignore \]**](ignore.md) für Unions nicht gültig sind.</span><span class="sxs-lookup"><span data-stu-id="6596d-126">Note that of the attributes listed above, **\[first\_is\]**, **\[last\_is\]**, and [**\[ignore\]**](ignore.md) are not valid for unions.</span></span>

</dd> <dt>

<span data-ttu-id="6596d-127">*eingeschränkter Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="6596d-127">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-128">Gibt einen C-sprach Ausdruck an.</span><span class="sxs-lookup"><span data-stu-id="6596d-128">Specifies a C-language expression.</span></span> <span data-ttu-id="6596d-129">Der mittlerer l-Compiler unterstützt bedingte Ausdrücke, logische Ausdrücke, relationale Ausdrücke und arithmetische Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="6596d-129">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="6596d-130">"Mittel l" lässt keine Funktionsaufrufe in Ausdrücken zu und lässt keine Inkrement-und Dekrementoperatoren zu.</span><span class="sxs-lookup"><span data-stu-id="6596d-130">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="6596d-131">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="6596d-131">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-132">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="6596d-132">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="6596d-133">Gültige Funktions Attribute sind [**\[ Callback \]**](callback.md), [**\[ local \]**](local.md), das Zeiger Attribut [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)oder [**\[ ptr \]**](ptr.md)sowie die [**\[ Zeichen \] Folge**](string.md)der Verwendungs Attribute und das [**\[ Kontext \_ handle \]**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="6596d-133">Valid function attributes are [**\[callback\]**](callback.md), [**\[local\]**](local.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), and [**\[context\_handle\]**](context-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="6596d-134">*function-name*</span><span class="sxs-lookup"><span data-stu-id="6596d-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-135">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="6596d-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="6596d-136">*param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="6596d-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6596d-137">Gibt die direktionalen Attribute und mindestens ein optionales Feld Attribut an, die auf den Array Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6596d-137">Specifies the directional attributes and one or more optional field attributes that apply to the array parameter.</span></span> <span data-ttu-id="6596d-138">Gültige Feld Attribute sind " [**\[ Max \_ is \]**](max-is.md)", " [**\[ size \_ \]**](size-is.md)", " [**\[ length \_ \]**](length-is.md)", " [**\[ First \_ is \]**](first-is.md)" und " [**\[ Last \_ \]**](last-is.md)".</span><span class="sxs-lookup"><span data-stu-id="6596d-138">Valid field attributes include [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), [**\[length\_is\]**](length-is.md), [**\[first\_is\]**](first-is.md), and [**\[last\_is\]**](last-is.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6596d-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6596d-139">Remarks</span></span>

<span data-ttu-id="6596d-140">Arrays in der mittleren l verwenden einen Stil, der mit identisch ist, aber nicht genau mit C und C++ identisch ist.</span><span class="sxs-lookup"><span data-stu-id="6596d-140">Arrays in MIDL use a style similar to but not exactly the same as C and C++.</span></span> <span data-ttu-id="6596d-141">Weitere Informationen finden Sie unter [Mittel l-Arrays](midl-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="6596d-141">For more information, see [MIDL Arrays](midl-arrays.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6596d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6596d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6596d-143">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="6596d-143">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="6596d-144">**const**</span><span class="sxs-lookup"><span data-stu-id="6596d-144">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="6596d-145">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="6596d-145">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="6596d-146">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6596d-146">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="6596d-147">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6596d-147">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="6596d-148">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="6596d-148">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="6596d-149">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="6596d-149">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6596d-150">**lassen**</span><span class="sxs-lookup"><span data-stu-id="6596d-150">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="6596d-151">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6596d-151">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="6596d-152">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6596d-152">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="6596d-153">**nah**</span><span class="sxs-lookup"><span data-stu-id="6596d-153">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="6596d-154">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="6596d-154">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="6596d-155">**ptr**</span><span class="sxs-lookup"><span data-stu-id="6596d-155">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="6596d-156">**ref**</span><span class="sxs-lookup"><span data-stu-id="6596d-156">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="6596d-157">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="6596d-157">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="6596d-158">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6596d-158">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="6596d-159">**struct**</span><span class="sxs-lookup"><span data-stu-id="6596d-159">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="6596d-160">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="6596d-160">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="6596d-161">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="6596d-161">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="6596d-162">**Union**</span><span class="sxs-lookup"><span data-stu-id="6596d-162">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="6596d-163">**gem**</span><span class="sxs-lookup"><span data-stu-id="6596d-163">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




