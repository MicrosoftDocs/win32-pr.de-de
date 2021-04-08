---
title: typedef-Attribut
description: Das IDL-typedef-Schlüsselwort lässt typedef-Deklarationen zu, die den Deklarationen der C-Programmiersprache typedef sehr ähneln.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef-Attribut-Mittel l
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725144"
---
# <a name="typedef-attribute"></a><span data-ttu-id="dda12-104">typedef-Attribut</span><span class="sxs-lookup"><span data-stu-id="dda12-104">typedef attribute</span></span>

<span data-ttu-id="dda12-105">Das IDL- **typedef** -Schlüsselwort lässt **typedef** -Deklarationen zu, die den Deklarationen der C-Programmiersprache **typedef** sehr ähneln.</span><span class="sxs-lookup"><span data-stu-id="dda12-105">The IDL **typedef** keyword allows **typedef** declarations that are very similar to C-language **typedef** declarations.</span></span>

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a><span data-ttu-id="dda12-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dda12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda12-107">*IDL-Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="dda12-107">*idl-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dda12-108">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dda12-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="dda12-109">Gültige Typattribute in einer IDL-Datei sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und das **\[** [**Kontext \_ handle**](context-handle.md) **\]** , die **\[** [**Zeichenfolge**](string.md) **\]** und **\[** [](ignore.md) **\]** die Syntax der Verwendungs Attribute.</span><span class="sxs-lookup"><span data-stu-id="dda12-109">Valid type attributes in an IDL file include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="dda12-110">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="dda12-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="dda12-111">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="dda12-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="dda12-112">Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="dda12-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="dda12-113">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dda12-113">An optional storage specification can precede *type-specifier*.</span></span> <span data-ttu-id="dda12-114">Das [**Schlüssel**](const.md) Wort "Schlüsselwort" kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dda12-114">The [**const**](const.md) keyword can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="dda12-115">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="dda12-115">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dda12-116">Gibt standardmäßige Mittelwert Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="dda12-116">Specifies standard MIDL declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="dda12-117">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="dda12-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="dda12-118">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="dda12-118">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="dda12-119">*ACF-Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="dda12-119">*acf-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dda12-120">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dda12-120">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="dda12-121">Zu den gültigen Typattributen in einer ACF gehören **\[** [**zuordnen**](allocate.md) **\]** , **\[** [**Codieren**](encode.md) **\]** und **\[** [**decodieren**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dda12-121">Valid type attributes in an ACF include **\[**[**allocate**](allocate.md)**\]**, **\[**[**encode**](encode.md)**\]**, and **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="dda12-122">*typeName*</span><span class="sxs-lookup"><span data-stu-id="dda12-122">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="dda12-123">Gibt einen Typ an, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="dda12-123">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dda12-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dda12-124">Remarks</span></span>

<span data-ttu-id="dda12-125">Die IDL- **typedef** -Deklaration wird erweitert, um es Ihnen zu ermöglichen, den definierten Typen Typattribute zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="dda12-125">The IDL **typedef** declaration is augmented to allow you to associate type attributes with the defined types.</span></span> <span data-ttu-id="dda12-126">Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dda12-126">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span>

<span data-ttu-id="dda12-127">Das **typedef** -Schlüsselwort in einer ACF wendet Attribute auf Typen an, die in der entsprechenden IDL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="dda12-127">The **typedef** keyword in an ACF applies attributes to types that are defined in the corresponding IDL file.</span></span> <span data-ttu-id="dda12-128">Beispielsweise können Sie mit dem Attribut " [**zuordnen**](allocate.md) " die Speicher Belegung und die Aufhebung der Zuordnung sowohl von der Anwendung als auch vom Stub anpassen.</span><span class="sxs-lookup"><span data-stu-id="dda12-128">For example, the [**allocate**](allocate.md) type attribute allows you to customize memory allocation and deallocation by both the application and the stubs.</span></span>

<span data-ttu-id="dda12-129">Die ACF- **typedef** -Anweisung wird als Teil des ACF-Texts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dda12-129">The ACF **typedef** statement appears as part of the ACF body.</span></span> <span data-ttu-id="dda12-130">Beachten Sie, dass die ACF- **typedef** -Syntax von der IDL- **typedef** -Syntax und der Syntax der C-Programmiersprache **typedef** abweicht.</span><span class="sxs-lookup"><span data-stu-id="dda12-130">Note that the ACF **typedef** syntax is different from the IDL **typedef** syntax and the C-language **typedef** syntax.</span></span> <span data-ttu-id="dda12-131">In der ACF können keine neuen Typen eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dda12-131">No new types can be introduced in the ACF.</span></span>

## <a name="see-also"></a><span data-ttu-id="dda12-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dda12-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda12-133">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="dda12-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="dda12-134">**allocate**</span><span class="sxs-lookup"><span data-stu-id="dda12-134">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="dda12-135">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="dda12-135">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="dda12-136">**const**</span><span class="sxs-lookup"><span data-stu-id="dda12-136">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="dda12-137">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="dda12-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="dda12-138">**Decodieren**</span><span class="sxs-lookup"><span data-stu-id="dda12-138">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="dda12-139">**Codieren**</span><span class="sxs-lookup"><span data-stu-id="dda12-139">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="dda12-140">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="dda12-140">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="dda12-141">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="dda12-141">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="dda12-142">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="dda12-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="dda12-143">**lassen**</span><span class="sxs-lookup"><span data-stu-id="dda12-143">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="dda12-144">**ptr**</span><span class="sxs-lookup"><span data-stu-id="dda12-144">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="dda12-145">**ref**</span><span class="sxs-lookup"><span data-stu-id="dda12-145">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="dda12-146">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dda12-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="dda12-147">**struct**</span><span class="sxs-lookup"><span data-stu-id="dda12-147">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="dda12-148">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="dda12-148">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="dda12-149">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="dda12-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="dda12-150">**Union**</span><span class="sxs-lookup"><span data-stu-id="dda12-150">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="dda12-151">**gem**</span><span class="sxs-lookup"><span data-stu-id="dda12-151">**unique**</span></span>](unique.md)
</dt> </dl>

 

 