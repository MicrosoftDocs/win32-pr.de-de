---
title: benutzerdefiniertes Attribut
description: Das \ Custom \-Attribut erstellt ein benutzerdefiniertes Attribut.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- benutzerdefiniertes Attribut-Mittel l
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340696"
---
# <a name="custom-attribute"></a><span data-ttu-id="0aa63-104">benutzerdefiniertes Attribut</span><span class="sxs-lookup"><span data-stu-id="0aa63-104">custom attribute</span></span>

<span data-ttu-id="0aa63-105">Das benutzerdefinierte Attribut erstellt ein benutzerdefiniertes Attribut. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="0aa63-105">The **\[custom\]** attribute creates a user-defined attribute.</span></span>

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a><span data-ttu-id="0aa63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0aa63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa63-107">*Attribut-ID*</span><span class="sxs-lookup"><span data-stu-id="0aa63-107">*attribute-id*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa63-108">Die GUID für das benutzerdefinierte Attribut.</span><span class="sxs-lookup"><span data-stu-id="0aa63-108">The GUID for the custom attribute.</span></span>

</dd> <dt>

<span data-ttu-id="0aa63-109">*Attribut-Wert*</span><span class="sxs-lookup"><span data-stu-id="0aa63-109">*attribute-value*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa63-110">Der Wert, den das Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="0aa63-110">The value that the attribute holds.</span></span> <span data-ttu-id="0aa63-111">Der Wert muss ein Typ sein, der in einen Variant-Typ eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0aa63-111">The value must be one that can be put into a VARIANT type.</span></span>

</dd> <dt>

<span data-ttu-id="0aa63-112">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="0aa63-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa63-113">Andere Attribute, z **\[** . b. [**UUID**](uuid.md) **\]** und **\[** [**HelpString**](helpstring.md) **\]** , die auf dieses Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa63-113">Other attributes, such as **\[**[**uuid**](uuid.md)**\]** and **\[**[**helpstring**](helpstring.md)**\]**, that apply to this element.</span></span>

</dd> <dt>

<span data-ttu-id="0aa63-114">*Elementtyp*</span><span class="sxs-lookup"><span data-stu-id="0aa63-114">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa63-115">Der Typ des Elements, auf das das benutzerdefinierte Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0aa63-115">The type of element to which the custom attribute applies.</span></span> <span data-ttu-id="0aa63-116">Dabei kann es sich um eine Bibliotheks Anweisung, Typinformationen, eine Variable, eine Funktion oder einen Parameter handeln.</span><span class="sxs-lookup"><span data-stu-id="0aa63-116">This can be a library statement, type information, a variable, a function, or a parameter.</span></span> <span data-ttu-id="0aa63-117">Ein benutzerdefiniertes Attribut kann nicht für einen Member einer Co-Klasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa63-117">You cannot use a custom attribute on a member of a coclass.</span></span>

</dd> <dt>

<span data-ttu-id="0aa63-118">*Elementname*</span><span class="sxs-lookup"><span data-stu-id="0aa63-118">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa63-119">Der Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="0aa63-119">The name of the element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0aa63-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0aa63-120">Remarks</span></span>

<span data-ttu-id="0aa63-121">Verwenden Sie das **\[ benutzerdefinierte \]** Attribut, um ein eigenes Attribut zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0aa63-121">Use the **\[custom\]** attribute to define your own attribute.</span></span> <span data-ttu-id="0aa63-122">Beispielsweise können Sie ein Attribut mit Zeichen folgen Wert erstellen, das die ProgID für eine Klasse übergibt.</span><span class="sxs-lookup"><span data-stu-id="0aa63-122">For example, you might create a string-valued attribute that gives the ProgID for a class.</span></span>

<span data-ttu-id="0aa63-123">Um einen benutzerdefinierten Attribut Wert abzurufen, rufen Sie einen der folgenden Werte auf:</span><span class="sxs-lookup"><span data-stu-id="0aa63-123">To retrieve a custom attribute value call one of the following:</span></span>

-   <span data-ttu-id="0aa63-124">ITypeLib2:: GetCustData (rguid, pvarval)</span><span class="sxs-lookup"><span data-stu-id="0aa63-124">ITypeLib2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="0aa63-125">ITypeInfo2:: GetCustData (rguid, pvarval)</span><span class="sxs-lookup"><span data-stu-id="0aa63-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="0aa63-126">ITypeInfo2:: GetFuncCustData (Index, rguid, pvarval)</span><span class="sxs-lookup"><span data-stu-id="0aa63-126">ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)</span></span>
-   <span data-ttu-id="0aa63-127">ITypeInfo2:: GetVarCustData (Index, rguid, pvarval)</span><span class="sxs-lookup"><span data-stu-id="0aa63-127">ITypeInfo2::GetVarCustData(index, rguid, pvarval)</span></span>
-   <span data-ttu-id="0aa63-128">ITypeInfo2:: GetParamCustData (indexfunc, indexparam, rguid, pvarval)</span><span class="sxs-lookup"><span data-stu-id="0aa63-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span></span>

## <a name="see-also"></a><span data-ttu-id="0aa63-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aa63-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa63-130">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="0aa63-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="0aa63-131">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="0aa63-131">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="0aa63-132">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="0aa63-132">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="0aa63-133">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="0aa63-133">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="0aa63-134">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="0aa63-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="0aa63-135">**UUID**</span><span class="sxs-lookup"><span data-stu-id="0aa63-135">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 