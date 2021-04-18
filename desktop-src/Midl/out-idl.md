---
title: out-Attribut
description: Das Attribut \ out \ identifiziert Zeiger Parameter, die von der aufgerufenen Prozedur an die aufrufenden Prozeduren zurückgegeben werden (vom Server an den Client).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- Out-Attribut, Mittel l
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340903"
---
# <a name="out-attribute"></a><span data-ttu-id="be12e-104">out-Attribut</span><span class="sxs-lookup"><span data-stu-id="be12e-104">out attribute</span></span>

<span data-ttu-id="be12e-105">Das \[ **out** - \] Attribut identifiziert Zeiger Parameter, die von der aufgerufenen Prozedur an die aufrufenden Prozeduren zurückgegeben werden (vom Server an den Client).</span><span class="sxs-lookup"><span data-stu-id="be12e-105">The \[**out**\] attribute identifies pointer parameters that are returned from the called procedure to the calling procedure (from the server to the client).</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a><span data-ttu-id="be12e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be12e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be12e-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="be12e-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="be12e-108">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="be12e-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="be12e-109">Gültige Funktions Attribute sind \[ [**Callback**](callback.md) \] , \[ [**local**](local.md), \] das Zeiger Attribut \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] oder \[ [**ptr**](ptr.md) \] und die Zeichenfolge der Verwendungs Attribute \[ [**Zeichenfolge**](string.md) \] , \[ [**ignorieren**](ignore.md) \] und \[ [**Kontext \_ handle**](context-handle.md) \] .</span><span class="sxs-lookup"><span data-stu-id="be12e-109">Valid function attributes are \[[**callback**](callback.md)\], \[[**local**](local.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**string**](string.md)\], \[[**ignore**](ignore.md)\], and \[[**context\_handle**](context-handle.md)\].</span></span>

</dd> <dt>

<span data-ttu-id="be12e-110">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="be12e-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="be12e-111">Gibt einen [ \_ Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="be12e-111">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="be12e-112">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="be12e-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="be12e-113">*Zeiger-Deklarator*</span><span class="sxs-lookup"><span data-stu-id="be12e-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="be12e-114">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="be12e-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="be12e-115">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="be12e-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="be12e-116">*function-name*</span><span class="sxs-lookup"><span data-stu-id="be12e-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="be12e-117">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="be12e-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="be12e-118">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="be12e-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="be12e-119">Gibt NULL oder mehr Attribute an, die für einen angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="be12e-119">Specifies zero or more attributes appropriate for a specified parameter type.</span></span> <span data-ttu-id="be12e-120">Parameter Attribute mit dem \[ **out** - \] Attribut können auch das direktionale Attribut annehmen \[  \] . die Feld Attribute \[ [**\_ sind zuerst**](first-is.md) \] , " \[ [**Last \_**](last-is.md)" \] , " \[ [**length \_**](length-is.md)" \] , " \[ [**Max \_ is**](max-is.md)" \] , "size" und " \[ [**\_**](size-is.md) \] \[ [**Switch \_ Type**](switch-type.md)", \] das Zeiger Attribut " \[ [**ref**](ref.md)" \] , " \[ [**Unique**](unique.md)" \] oder " \[ [**ptr**](ptr.md)" \] und das \[ [**Kontext \_ handle**](context-handle.md) \] und die \[ [**Zeichenfolge**](string.md) \] der Verwendungs Attribute</span><span class="sxs-lookup"><span data-stu-id="be12e-120">Parameter attributes with the \[**out**\] attribute can also take the directional attribute \[**out**\]; the field attributes \[[**first\_is**](first-is.md)\], \[[**last\_is**](last-is.md)\], \[[**length\_is**](length-is.md)\], \[[**max\_is**](max-is.md)\], \[[**size\_is**](size-is.md)\], and \[[**switch\_type**](switch-type.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**context\_handle**](context-handle.md)\] and \[[**string**](string.md)\].</span></span> <span data-ttu-id="be12e-121">Das Usage-Attribut " \[ [**Ignore**](ignore.md) " \] kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be12e-121">The usage attribute \[[**ignore**](ignore.md)\] cannot be used as a parameter attribute.</span></span> <span data-ttu-id="be12e-122">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="be12e-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="be12e-123">*Deklarator*</span><span class="sxs-lookup"><span data-stu-id="be12e-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="be12e-124">Gibt die Standard Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="be12e-124">Specifies the standard declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="be12e-125">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="be12e-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="be12e-126">Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.</span><span class="sxs-lookup"><span data-stu-id="be12e-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be12e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be12e-127">Remarks</span></span>

<span data-ttu-id="be12e-128">Das \[ **out** \] -Attribut gibt an, dass ein Parameter, der als Zeiger und die zugehörigen Daten im Arbeitsspeicher fungiert, von der aufgerufenen Prozedur an die aufrufende Prozedur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="be12e-128">The \[**out**\] attribute indicates that a parameter that acts as a pointer and its associated data in memory are to be passed back from the called procedure to the calling procedure.</span></span>

<span data-ttu-id="be12e-129">Das \[ **out** - \] Attribut muss ein Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="be12e-129">The \[**out**\] attribute must be a pointer.</span></span> <span data-ttu-id="be12e-130">DCE-IDL-Compiler erfordern das vorhanden sein eines expliziten \* als zeigerdeklarator in der Parameter Deklaration.</span><span class="sxs-lookup"><span data-stu-id="be12e-130">DCE IDL compilers require the presence of an explicit \* as a pointer declarator in the parameter declaration.</span></span> <span data-ttu-id="be12e-131">Microsoft IDL bietet eine Erweiterung, die diese Anforderung löscht und ein Array oder einen zuvor definierten Zeigertyp zulässt.</span><span class="sxs-lookup"><span data-stu-id="be12e-131">Microsoft IDL offers an extension that drops this requirement and allows an array or a previously defined pointer type.</span></span>

<span data-ttu-id="be12e-132">Ein verknüpftes Attribut \[ [**in**](in.md) \] gibt an, dass der Parameter von der aufrufenden Prozedur an die aufgerufene Prozedur übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="be12e-132">A related attribute, \[[**in**](in.md)\], indicates that the parameter is passed from the calling procedure to the called procedure.</span></span> <span data-ttu-id="be12e-133">Die \[ **in** \] -und \[ **out** - \] Attribute geben die Richtung an, in der die Parameter übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="be12e-133">The \[**in**\] and \[**out**\] attributes specify the direction in which the parameters are passed.</span></span> <span data-ttu-id="be12e-134">Ein Parameter kann nur als " \[ nur **in** \] -only", " \[ **out**" \] oder " \[ **in**  \] ", "out" definiert werden.</span><span class="sxs-lookup"><span data-stu-id="be12e-134">A parameter can be defined as \[**in**\]-only, \[**out**\]-only, or \[**in**, **out**\].</span></span>

<span data-ttu-id="be12e-135">\[  \] Es wird davon ausgegangen, dass ein out-only-Parameter nicht definiert ist, wenn die Remote Prozedur aufgerufen wird und der Speicher für das Objekt vom Server zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="be12e-135">An \[**out**\]-only parameter is assumed to be undefined when the remote procedure is called and memory for the object is allocated by the server.</span></span> <span data-ttu-id="be12e-136">Da Zeiger/Parameter der obersten Ebene immer auf einen gültigen Speicher zeigen und daher nicht **null** sein dürfen, \[ kann **out** \] nicht auf \[ [**eindeutige**](unique.md) \] oder \[ [**ptr**](ptr.md) - \] Zeiger der obersten Ebene angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="be12e-136">Since top-level pointer/parameters must always point to valid storage, and therefore cannot be **NULL**, \[**out**\] cannot be applied to top-level \[[**unique**](unique.md)\] or \[[**ptr**](ptr.md)\] pointers.</span></span> <span data-ttu-id="be12e-137">Parameter, die \[ **eindeutig** \] sind \[ , oder **ptr** - \] Zeiger müssen entweder \[ [**in**](in.md) - \] oder \[ **in**-, **out** - \] Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="be12e-137">Parameters that are \[**unique**\] or \[**ptr**\] pointers must be either \[[**in**](in.md)\] or \[**in**, **out**\] parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="be12e-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be12e-138">Examples</span></span>

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a><span data-ttu-id="be12e-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="be12e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be12e-140">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="be12e-140">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="be12e-141">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="be12e-141">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="be12e-142">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="be12e-142">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="be12e-143">**const**</span><span class="sxs-lookup"><span data-stu-id="be12e-143">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="be12e-144">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="be12e-144">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="be12e-145">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="be12e-145">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="be12e-146">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="be12e-146">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="be12e-147">**lassen**</span><span class="sxs-lookup"><span data-stu-id="be12e-147">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="be12e-148">**in**</span><span class="sxs-lookup"><span data-stu-id="be12e-148">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="be12e-149">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="be12e-149">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="be12e-150">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="be12e-150">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="be12e-151">**nah**</span><span class="sxs-lookup"><span data-stu-id="be12e-151">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="be12e-152">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="be12e-152">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="be12e-153">**ptr**</span><span class="sxs-lookup"><span data-stu-id="be12e-153">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="be12e-154">**ref**</span><span class="sxs-lookup"><span data-stu-id="be12e-154">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="be12e-155">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="be12e-155">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="be12e-156">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be12e-156">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="be12e-157">**struct**</span><span class="sxs-lookup"><span data-stu-id="be12e-157">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="be12e-158">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="be12e-158">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="be12e-159">**Union**</span><span class="sxs-lookup"><span data-stu-id="be12e-159">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="be12e-160">**gem**</span><span class="sxs-lookup"><span data-stu-id="be12e-160">**unique**</span></span>](unique.md)
</dt> </dl>

 

 