---
title: Attribut mit Anmerkungen versehen
description: Mit dem Attribut "\ Annotate \" können Sie eine SAL-Anmerkung-Zeichenfolge für die angegebene Methode, den Parameter oder das Strukturfeld angeben.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- Attribut-Mittell kommentieren
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732088"
---
# <a name="annotate-attribute"></a><span data-ttu-id="c0cf4-104">Attribut mit Anmerkungen versehen</span><span class="sxs-lookup"><span data-stu-id="c0cf4-104">annotate attribute</span></span>

<span data-ttu-id="c0cf4-105">Mit dem Attribut " **\[ kommentieren \]** " können Sie eine SAL-Anmerkung-Zeichenfolge für die angegebene Methode, den Parameter oder das Strukturfeld angeben.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-105">The **\[annotate\]** attribute allows you to specify a SAL annotation string for the specified method, parameter, or structure field.</span></span>

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="c0cf4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0cf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0cf4-107">*string*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-108">Die angegebene SAL-Anmerkung-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-108">Specified SAL annotation string.</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-109">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-109">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-110">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="c0cf4-111">Gültige Funktions Attribute sind [**\[ Callback \]**](callback.md), die Zeiger Attribute [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)oder [**\[ ptr \]**](ptr.md)und die Verwendungs Attribute [**\[ Zeichenfolge \]**](string.md), [**\[ ignorieren \]**](ignore.md)und [**\[ Kontext \_ handle \]**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="c0cf4-111">Valid function attributes include [**\[callback\]**](callback.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), [**\[ignore\]**](ignore.md), and [**\[context\_handle\]**](context-handle.md).</span></span> <span data-ttu-id="c0cf4-112">Mehrere Attribute müssen durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-112">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-113">*Function-declarator*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-113">*function-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-114">Gibt den Typspezifizierer, den Funktionsnamen und die Parameterliste für die Funktion an.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-114">Specifies the type specifier, function name, and parameter list for the function.</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-115">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-115">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-116">Gibt einen **\_ Basistyp**, eine [**\[ Struktur \]**](struct.md) [](union.md), eine Union oder einen Aufzählungstyp oder einen Typbezeichner an. [**\[ \]**](enum.md)</span><span class="sxs-lookup"><span data-stu-id="c0cf4-116">Specifies a **base\_type**, [**\[struct\]**](struct.md), [**union**](union.md), or [**\[enum\]**](enum.md) type or type identifier.</span></span> <span data-ttu-id="c0cf4-117">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-117">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-118">*Zeiger-Deklarator*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-118">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-119">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-119">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="c0cf4-120">Ein zeigerdeklarator ist mit dem in C verwendeten zeigerdeklarator identisch. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**\[ Konstanten \]**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-120">A pointer declarator is the same as a pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**\[const\]**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-121">*function-name*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-121">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-122">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-122">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-123">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-123">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-124">Gibt 0 (null) oder mehr für den Parametertyp geeignete Attribute an.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-124">Specifies zero or more attributes appropriate for the parameter type.</span></span> <span data-ttu-id="c0cf4-125">Parameter Attribute mit dem [**\[ in \]**](in.md) -Attribut können auch das [**\[ \]**](unique.md) [**\[ \_ \]**](last-is.md) [**\[ \]**](ref.md) [**\[ \]**](out-idl.md)direktionale Attribut zurücknehmen. die Feld Attribute [**\[ \_ sind \] zuerst**](first-is.md) [**\[ \_ , " \]**](length-is.md)Last", "length", " [**\[ Max \_ \] is**](max-is.md)", " [**\[ size" und " \_ Switch Type", die Zeiger Attribute "ref", "Unique" oder "PTR" und das Kontext Handle und die Zeichenfolge der Verwendungs \]**](size-is.md) [**\[ \]**](string.md) [**\[ \_ \]**](switch-type.md) [**\[ \_ \]**](context-handle.md) [**\[ \]**](ptr.md)</span><span class="sxs-lookup"><span data-stu-id="c0cf4-125">Parameter attributes with the [**\[in\]**](in.md) attribute can also take the directional attribute [**\[out\]**](out-idl.md); the field attributes [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), and [**\[switch\_type\]**](switch-type.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md) and [**\[string\]**](string.md).</span></span> <span data-ttu-id="c0cf4-126">Das Usage-Attribut " [**\[ Ignore \]**](ignore.md) " kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-126">The usage attribute [**\[ignore\]**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="c0cf4-127">Mehrere Attribute müssen durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-127">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-128">*Deklarator*</span><span class="sxs-lookup"><span data-stu-id="c0cf4-128">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cf4-129">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-129">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="c0cf4-130">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**\[ Arrays \]**](../rpc/arrays.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="c0cf4-130">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**\[arrays\]**](../rpc/arrays.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="c0cf4-131">Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-131">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0cf4-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0cf4-132">Remarks</span></span>

<span data-ttu-id="c0cf4-133">Das **\[ kommentieren \]** -Attribut ermöglicht das Überschreiben von in der Mitte generierten SAL-Anmerkungen oder das Hinzufügen an Stellen, an denen die-Anmerkung nicht explizit eine Anmerkung generiert.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-133">The **\[annotate\]** attribute allows overriding MIDL-generated SAL annotations or adding them in places where MIDL does not explicitly generate an annotation.</span></span> <span data-ttu-id="c0cf4-134">Wenn [**/SAL**](-sal.md) nicht in der Befehlszeile angegeben ist, wird dieses Attribut ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-134">If [**/sal**](-sal.md) is not specified on the command line, this attribute is ignored.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0cf4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0cf4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0cf4-136">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c0cf4-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c0cf4-137">**/sal**</span><span class="sxs-lookup"><span data-stu-id="c0cf4-137">**/sal**</span></span>](-sal.md)
</dt> <dt>

[<span data-ttu-id="c0cf4-138">**/SAL \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="c0cf4-138">**/sal\_local**</span></span>](-sal-local.md)
</dt> </dl>

 

 