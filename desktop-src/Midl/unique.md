---
title: Eindeutiges Attribut
description: Das Attribut \ Unique \ gibt einen eindeutigen Zeiger an.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- Unique-attributmittell
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338453"
---
# <a name="unique-attribute"></a><span data-ttu-id="e0197-104">Eindeutiges Attribut</span><span class="sxs-lookup"><span data-stu-id="e0197-104">unique attribute</span></span>

<span data-ttu-id="e0197-105">Das **\[ Unique \]** -Attribut gibt einen eindeutigen Zeiger an.</span><span class="sxs-lookup"><span data-stu-id="e0197-105">The **\[unique\]** attribute specifies a unique pointer.</span></span>

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="e0197-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0197-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0197-107">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e0197-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-108">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="e0197-109">Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[ eindeutig \]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e0197-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="e0197-110">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="e0197-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e0197-111">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="e0197-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-112">Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="e0197-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="e0197-113">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e0197-114">*Deklarator und Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="e0197-114">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-115">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="e0197-115">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e0197-116">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e0197-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e0197-117">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="e0197-117">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="e0197-118">Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.</span><span class="sxs-lookup"><span data-stu-id="e0197-118">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e0197-119">*struct-or-Union-declarator*</span><span class="sxs-lookup"><span data-stu-id="e0197-119">*struct-or-union-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-120">Gibt eine mittlerer l- [**Struktur**](struct.md) oder einen [**Union**](union.md) -Deklarator an.</span><span class="sxs-lookup"><span data-stu-id="e0197-120">Specifies a MIDL [**struct**](struct.md) or [**union**](union.md) declarator.</span></span>

</dd> <dt>

<span data-ttu-id="e0197-121">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e0197-121">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-122">Gibt 0 (null) oder mehr Feld Attribute an, die für den Strukturmember, den Union-Member oder den Funktionsparameter gelten.</span><span class="sxs-lookup"><span data-stu-id="e0197-122">Specifies zero or more field attributes that apply to the structure member, union member, or function parameter.</span></span> <span data-ttu-id="e0197-123">Gültige Feld Attribute sind **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** die Usage-Attribute **\[ \] String**, **\[ Ignore \]** und **\[ context \_ handle \]**, das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ ptr \]** und der Typ **\[ \_ \]** des Union-Attribut Schalters.</span><span class="sxs-lookup"><span data-stu-id="e0197-123">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="e0197-124">Trennen Sie mehrere Feld Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="e0197-124">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e0197-125">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e0197-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-126">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="e0197-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="e0197-127">Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[ ref \]**, **\[ Unique \]** oder **\[ \] ptr** und die Zeichenfolge der Verwendungs Attribute **\[ Zeichenfolge \]**, **\[ ignorieren \]** und **\[ Kontext \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="e0197-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="e0197-128">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="e0197-128">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-129">Gibt mindestens einen zeigerdeklarator an, für den das **\[ eindeutige \]** Attribut gilt.</span><span class="sxs-lookup"><span data-stu-id="e0197-129">Specifies at least one pointer declarator to which the **\[unique\]** attribute applies.</span></span> <span data-ttu-id="e0197-130">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0197-130">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0197-131">*function-name*</span><span class="sxs-lookup"><span data-stu-id="e0197-131">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-132">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="e0197-132">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e0197-133">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e0197-133">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e0197-134">Besteht aus null oder mehr Attributen, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="e0197-134">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="e0197-135">Parameter Attribute können die direktionalen Attribute **\[ \] ein-und** **\[ \] ausschalten. die** **\[ \] Feld Attribute** **\[ \_ sind \] zuerst**  **\[ \_ \]** **\[ \_ , " \]** Last", "length", " **\[ Max \_ \] is**", " **\[ size" und " \_ Switch Type", das Zeiger Attribut "ref", "Unique" oder "PTR" und das Kontext Handle und die Zeichenfolge der Verwendungs Attribute \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** [](ptr.md)</span><span class="sxs-lookup"><span data-stu-id="e0197-135">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **unique**, or [**ptr**](ptr.md); and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="e0197-136">Das Usage-Attribut " **\[ Ignore \]** " kann nicht als Parameter Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-136">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="e0197-137">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="e0197-137">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0197-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0197-138">Remarks</span></span>

<span data-ttu-id="e0197-139">Zeiger Attribute können als Type-Attribut angewendet werden. als Feld Attribut, das für einen Strukturmember, ein Union-Member oder einen-Parameter gilt. oder als Funktions Attribut, das für den Funktions Rückgabetyp gilt.</span><span class="sxs-lookup"><span data-stu-id="e0197-139">Pointer attributes can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="e0197-140">Das Zeiger Attribut kann auch mit dem **\[** [**Zeiger \_ default**](pointer-default.md) - **\]** Schlüsselwort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-140">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="e0197-141">Ein eindeutiger Zeiger weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="e0197-141">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="e0197-142">Der Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e0197-142">Can have the value **NULL**.</span></span>
-   <span data-ttu-id="e0197-143">Kann während eines Aufrufes von **null** in einen nicht-**null**-Wert, von einem nicht-**null** -Wert in **null** oder von einem nicht-**null** -Wert zu einem anderen ändern.</span><span class="sxs-lookup"><span data-stu-id="e0197-143">Can change during a call from **NULL** to non-**NULL**, from non-**NULL** to **NULL**, or from one non-**NULL** value to another.</span></span>
-   <span data-ttu-id="e0197-144">Auf dem Client kann neuer Arbeitsspeicher belegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-144">Can allocate new memory on the client.</span></span> <span data-ttu-id="e0197-145">Wenn der eindeutige Zeiger von **null** in einen nicht-**null**-Wert geändert wird, werden die vom Server zurückgegebenen Daten in den neuen Speicher geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0197-145">When the unique pointer changes from **NULL** to non-**NULL**, data returned from the server is written into new storage.</span></span>
-   <span data-ttu-id="e0197-146">Kann vorhandenen Arbeitsspeicher auf dem Client verwenden, ohne neuen Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e0197-146">Can use existing memory on the client without allocating new memory.</span></span> <span data-ttu-id="e0197-147">Wenn sich ein eindeutiger Zeiger während eines Aufrufes von einem nicht-**null** -Wert in einen anderen ändert, wird davon ausgegangen, dass der Zeiger auf ein Datenobjekt desselben Typs verweist.</span><span class="sxs-lookup"><span data-stu-id="e0197-147">When a unique pointer changes during a call from one non-**NULL** value to another, the pointer is assumed to point to a data object of the same type.</span></span> <span data-ttu-id="e0197-148">Die vom Server zurückgegebenen Daten werden in den vorhandenen Speicher geschrieben, der durch den Wert des eindeutigen Zeigers vor dem-Befehl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e0197-148">Data returned from the server is written into existing storage specified by the value of the unique pointer before the call.</span></span>
-   <span data-ttu-id="e0197-149">Der Arbeitsspeicher auf dem Client kann verwaisten.</span><span class="sxs-lookup"><span data-stu-id="e0197-149">Can orphan memory on the client.</span></span> <span data-ttu-id="e0197-150">Der Speicher, auf den von einem eindeutigen Zeiger ungleich **null** verwiesen wird, wird möglicherweise nie freigegeben, wenn der eindeutige Zeiger während eines-Aufrufes in **null** ändert und der Client nicht über eine andere Möglichkeit zur Dereferenzierung des Speichers verfügt.</span><span class="sxs-lookup"><span data-stu-id="e0197-150">Memory referenced by a non-**NULL** unique pointer may never be freed if the unique pointer changes to **NULL** during a call and the client does not have another means of dereferencing the storage.</span></span>
-   <span data-ttu-id="e0197-151">Führt nicht zum Aliasing.</span><span class="sxs-lookup"><span data-stu-id="e0197-151">Does not cause aliasing.</span></span> <span data-ttu-id="e0197-152">Wie der Speicher, auf den ein Verweis Zeiger zeigt, kann der Speicher, auf den von einem eindeutigen Zeiger verwiesen wird, nicht von einem anderen Namen in der Funktion erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-152">Like storage pointed to by a reference pointer, storage pointed to by a unique pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="e0197-153">Mit den stubaten werden die vom Benutzer bereitgestellten Speicherverwaltungsfunktionen " [**mittlere \_ Benutzer \_**](/windows/desktop/Rpc/the-midl-user-allocate-function) Zuordnungen" und " [**mittlere \_ Benutzer" \_ frei**](/windows/desktop/Rpc/the-midl-user-free-function) gegeben, um den für eindeutige Zeiger und deren Verweise erforderlichen Arbeitsspeicher zuzuordnen und deren Freigabe aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="e0197-153">The stubs call the user-supplied memory-management functions [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) to allocate and deallocate memory required for unique pointers and their referents.</span></span>

<span data-ttu-id="e0197-154">Die folgenden Einschränkungen gelten für eindeutige Zeiger:</span><span class="sxs-lookup"><span data-stu-id="e0197-154">The following restrictions apply to unique pointers:</span></span>

-   <span data-ttu-id="e0197-155">Das **\[ Unique \]** -Attribut kann nicht auf Parameter für Bindungs handle ( [**handle \_ t**](handle-t.md)) und Kontext Handle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-155">The **\[unique\]** attribute cannot be applied to binding-handle parameters ( [**handle\_t**](handle-t.md)) and context-handle parameters.</span></span>
-   <span data-ttu-id="e0197-156">Das **\[ Unique \]** -Attribut kann nicht auf **\[** [**out**](out-idl.md) **\]** -only-Zeiger Parameter (Parameter, die nur über das **\[ out \]** -direktionale Attribut verfügen) angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0197-156">The **\[unique\]** attribute cannot be applied to **\[**[**out**](out-idl.md)**\]**-only top-level pointer parameters (parameters that have only the **\[out\]** directional attribute).</span></span>
-   <span data-ttu-id="e0197-157">Standardmäßig sind Zeiger der obersten Ebene in Parameterlisten **\[** [**ref**](ref.md) - **\]** Zeiger.</span><span class="sxs-lookup"><span data-stu-id="e0197-157">By default, top-level pointers in parameter lists are **\[**[**ref**](ref.md)**\]** pointers.</span></span> <span data-ttu-id="e0197-158">Dies gilt auch, wenn die Schnittstelle **Zeiger \_ Standard (eindeutig)** angibt.</span><span class="sxs-lookup"><span data-stu-id="e0197-158">This is true even if the interface specifies **pointer\_default(unique)**.</span></span> <span data-ttu-id="e0197-159">Parameter der obersten Ebene in Parameterlisten müssen mit dem **\[ Unique \]** -Attribut angegeben werden, damit es sich um einen eindeutigen Zeiger handelt.</span><span class="sxs-lookup"><span data-stu-id="e0197-159">Top-level parameters in parameter lists must be specified with the **\[unique\]** attribute to be a unique pointer.</span></span>
-   <span data-ttu-id="e0197-160">Eindeutige Zeiger können nicht verwendet werden, um die Größe eines Arrays oder eines Union-Arm zu beschreiben, da eindeutige Zeiger den Wert **null** haben können.</span><span class="sxs-lookup"><span data-stu-id="e0197-160">Unique pointers cannot be used to describe the size of an array or union arm because unique pointers can have the value **NULL**.</span></span> <span data-ttu-id="e0197-161">Diese Einschränkung verhindert den Fehler, der sich ergibt, wenn ein **null** -Wert als Array Größe oder Union-Arm-Größe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0197-161">This restriction prevents the error that results if a **NULL** value is used as the array size or the union-arm size.</span></span>

## <a name="examples"></a><span data-ttu-id="e0197-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0197-162">Examples</span></span>

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="e0197-163">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0197-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0197-164">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="e0197-164">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e0197-165">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="e0197-165">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="e0197-166">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="e0197-166">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0197-167">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="e0197-167">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e0197-168">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="e0197-168">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="e0197-169">**const**</span><span class="sxs-lookup"><span data-stu-id="e0197-169">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e0197-170">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="e0197-170">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e0197-171">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e0197-171">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e0197-172">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="e0197-172">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="e0197-173">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="e0197-173">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="e0197-174">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="e0197-174">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="e0197-175">**lassen**</span><span class="sxs-lookup"><span data-stu-id="e0197-175">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e0197-176">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="e0197-176">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="e0197-177">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="e0197-177">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="e0197-178">**nah**</span><span class="sxs-lookup"><span data-stu-id="e0197-178">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="e0197-179">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="e0197-179">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="e0197-180">mittlere Benutzer Zuordnungen \_ \_</span><span class="sxs-lookup"><span data-stu-id="e0197-180">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="e0197-181">mittlerer l- \_ Benutzer \_ kostenlos</span><span class="sxs-lookup"><span data-stu-id="e0197-181">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="e0197-182">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="e0197-182">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="e0197-183">**Zeiger \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="e0197-183">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="e0197-184">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e0197-184">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e0197-185">**ref**</span><span class="sxs-lookup"><span data-stu-id="e0197-185">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e0197-186">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="e0197-186">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="e0197-187">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e0197-187">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e0197-188">**struct**</span><span class="sxs-lookup"><span data-stu-id="e0197-188">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e0197-189">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="e0197-189">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e0197-190">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="e0197-190">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="e0197-191">**Union**</span><span class="sxs-lookup"><span data-stu-id="e0197-191">**union**</span></span>](union.md)
</dt> </dl>

 

 