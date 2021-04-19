---
title: struct-Attribut
description: Das struct-Schlüsselwort wird in einem strukturtypspezifizierer verwendet.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- Struktur Attribut-Mittel l
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106342128"
---
# <a name="struct-attribute"></a><span data-ttu-id="ceb73-104">struct-Attribut</span><span class="sxs-lookup"><span data-stu-id="ceb73-104">struct attribute</span></span>

<span data-ttu-id="ceb73-105">Das **struct** -Schlüsselwort wird in einem strukturtypspezifizierer verwendet.</span><span class="sxs-lookup"><span data-stu-id="ceb73-105">The **struct** keyword is used in a structure type specifier.</span></span>

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="ceb73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ceb73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb73-107">*struct-Tag*</span><span class="sxs-lookup"><span data-stu-id="ceb73-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb73-108">Gibt ein optionales Tag für die Struktur an.</span><span class="sxs-lookup"><span data-stu-id="ceb73-108">Specifies an optional tag for the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ceb73-109">*Field-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ceb73-109">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb73-110">Gibt 0 (null) oder mehr Feld Attribute an, die für den Strukturmember gelten.</span><span class="sxs-lookup"><span data-stu-id="ceb73-110">Specifies zero or more field attributes that apply to the structure member.</span></span> <span data-ttu-id="ceb73-111">Gültige Feld Attribute sind " **\[** [**First \_ is**](first-is.md)" **\]** , " **\[** [**Last \_ is**](last-is.md)" **\]** , " **\[** [**length \_ is**](length-is.md)", " **\]** **\[** [**Max \_ is**](max-is.md)" und "size", " **\]** **\[** [**\_**](size-is.md) **\]** Usage Attribute **\[** [**String**](string.md) " **\]** und " **\[** [**Ignore**](ignore.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](switch-type.md) **\]** "</span><span class="sxs-lookup"><span data-stu-id="ceb73-111">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="ceb73-112">Trennen Sie mehrere Feld Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="ceb73-112">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ceb73-113">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="ceb73-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb73-114">Gibt einen [Basistyp](midl-base-types.md), eine **Struktur**, eine [**Union**](union.md)oder einen Aufzählungstyp [**oder einen**](enum.md) Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="ceb73-114">Specifies a [base type](midl-base-types.md), **struct**, [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="ceb73-115">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ceb73-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="ceb73-116">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="ceb73-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb73-117">Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="ceb73-117">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="ceb73-118">(Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ceb73-118">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="ceb73-119">Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="ceb73-119">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ceb73-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ceb73-120">Remarks</span></span>

<span data-ttu-id="ceb73-121">Der IDL-strukturtypspezifizierer ( **struct**) unterscheidet sich in folgenden Punkten vom standardmäßigen C-Typspezifizierer:</span><span class="sxs-lookup"><span data-stu-id="ceb73-121">The IDL structure type specifier, **struct**, differs from the standard C type specifier in the following ways:</span></span>

-   <span data-ttu-id="ceb73-122">Jeder Strukturmember kann optionalen Feld Attributen zugeordnet werden, die die Merkmale dieses Strukturmembers für den Zweck eines Remote Prozedur Aufrufes beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ceb73-122">Each structure member can be associated with optional field attributes that describe characteristics of that structure member for the purposes of a remote procedure call.</span></span>
-   <span data-ttu-id="ceb73-123">Bitfelder und Funktionsdeklaratoren sind in Strukturen, die in Remote Prozedur aufrufen verwendet werden, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ceb73-123">Bit fields and function declarators are not allowed in structures that are used in remote procedure calls.</span></span> <span data-ttu-id="ceb73-124">Diese standardmäßigen C-deklaratorkonstrukte können nur verwendet werden, wenn die Struktur nicht im Netzwerk übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="ceb73-124">These standard C declarator constructs can be used only if the structure is not transmitted on the network.</span></span>

<span data-ttu-id="ceb73-125">Die Form von Strukturen muss plattformübergreifend identisch sein, um die Konnektivität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="ceb73-125">The shape of structures must be the same across platforms to ensure interconnectivity.</span></span>

## <a name="examples"></a><span data-ttu-id="ceb73-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ceb73-126">Examples</span></span>

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="ceb73-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ceb73-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb73-128">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="ceb73-128">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="ceb73-129">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="ceb73-129">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="ceb73-130">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="ceb73-130">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ceb73-131">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="ceb73-131">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ceb73-132">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="ceb73-132">**/c\_ext**</span></span>](-c-ext.md)
</dt> <dt>

[<span data-ttu-id="ceb73-133">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="ceb73-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="ceb73-134">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ceb73-134">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="ceb73-135">**der erste \_ ist**</span><span class="sxs-lookup"><span data-stu-id="ceb73-135">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="ceb73-136">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="ceb73-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ceb73-137">**lassen**</span><span class="sxs-lookup"><span data-stu-id="ceb73-137">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="ceb73-138">**Letzter \_ ist**</span><span class="sxs-lookup"><span data-stu-id="ceb73-138">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="ceb73-139">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="ceb73-139">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="ceb73-140">**Max \_ ist**</span><span class="sxs-lookup"><span data-stu-id="ceb73-140">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="ceb73-141">**/osf**</span><span class="sxs-lookup"><span data-stu-id="ceb73-141">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="ceb73-142">**ptr**</span><span class="sxs-lookup"><span data-stu-id="ceb73-142">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="ceb73-143">**ref**</span><span class="sxs-lookup"><span data-stu-id="ceb73-143">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="ceb73-144">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="ceb73-144">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="ceb73-145">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ceb73-145">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="ceb73-146">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="ceb73-146">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="ceb73-147">**Union**</span><span class="sxs-lookup"><span data-stu-id="ceb73-147">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="ceb73-148">**gem**</span><span class="sxs-lookup"><span data-stu-id="ceb73-148">**unique**</span></span>](unique.md)
</dt> </dl>

 

 