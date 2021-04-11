---
title: Quellattribut
description: Das Attribut \ Source \ gibt an, dass ein Member einer Co-Klasse, einer Eigenschaft oder Methode eine Quelle von Ereignissen ist. Bei einem Member einer Co-Klasse bedeutet dieses Attribut, dass der Member aufgerufen wird, anstatt implementiert zu werden.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- Quell Attribut-Mittel l
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948616"
---
# <a name="source-attribute"></a><span data-ttu-id="c6636-105">Quellattribut</span><span class="sxs-lookup"><span data-stu-id="c6636-105">source attribute</span></span>

<span data-ttu-id="c6636-106">Das **\[ Source \]** -Attribut gibt an, dass ein Member einer [**Co-Klasse**](coclass.md), einer Eigenschaft oder Methode eine Quelle von Ereignissen ist.</span><span class="sxs-lookup"><span data-stu-id="c6636-106">The **\[source\]** attribute indicates that a member of a [**coclass**](coclass.md), property, or method is a source of events.</span></span> <span data-ttu-id="c6636-107">Bei einem Member einer **Co-Klasse** bedeutet dieses Attribut, dass der Member aufgerufen wird, anstatt implementiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="c6636-107">For a member of a **coclass**, this attribute means that the member is called rather than implemented.</span></span>

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="c6636-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6636-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6636-109">*coclass-Attribute*</span><span class="sxs-lookup"><span data-stu-id="c6636-109">*coclass-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-110">0 (null) oder mehr Attribute, die auf die [**Co-Klasse**](coclass.md)angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6636-110">Zero or more attributes that will be applied to the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6636-111">*Name der Co-Klasse*</span><span class="sxs-lookup"><span data-stu-id="c6636-111">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-112">Der namens Bezeichner der [**Co-Klasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="c6636-112">The name identifier of the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6636-113">*optionale Attribute*</span><span class="sxs-lookup"><span data-stu-id="c6636-113">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-114">NULL oder mehr mittlere Attribute.</span><span class="sxs-lookup"><span data-stu-id="c6636-114">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="c6636-115">*Anweisungstyp*</span><span class="sxs-lookup"><span data-stu-id="c6636-115">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-116">Kann " [**Interface**](interface.md) " oder " [**dispinterface**](dispinterface.md)" sein.</span><span class="sxs-lookup"><span data-stu-id="c6636-116">Can be [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6636-117">*Anweisungs Name*</span><span class="sxs-lookup"><span data-stu-id="c6636-117">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-118">Der Name der [**Schnittstelle**](interface.md) oder der [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="c6636-118">The name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6636-119">*Objekttyp*</span><span class="sxs-lookup"><span data-stu-id="c6636-119">*object-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-120">Der Typ des Objekts, das von der Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c6636-120">The type of the object that the method returns.</span></span> <span data-ttu-id="c6636-121">Dieses Objekt ist eine Quelle von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="c6636-121">This object is a source of events.</span></span>

</dd> <dt>

<span data-ttu-id="c6636-122">*function-name*</span><span class="sxs-lookup"><span data-stu-id="c6636-122">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-123">Der Name einer Methode in einer [**Schnittstelle**](interface.md) oder einer [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="c6636-123">The name of a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6636-124">*Optional-Parameter-List*</span><span class="sxs-lookup"><span data-stu-id="c6636-124">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c6636-125">NULL oder mehr Methoden Parameter.</span><span class="sxs-lookup"><span data-stu-id="c6636-125">Zero or more method parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6636-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6636-126">Remarks</span></span>

<span data-ttu-id="c6636-127">Bei einer Eigenschaft oder Methode gibt das **\[ Quell \]** Attribut an, dass der Member ein Objekt oder eine Variante zurückgibt, das eine Quelle von Ereignissen ist.</span><span class="sxs-lookup"><span data-stu-id="c6636-127">On a property or method, the **\[source\]** attribute indicates that the member returns an object or VARIANT that is a source of events.</span></span> <span data-ttu-id="c6636-128">Das Objekt implementiert **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="c6636-128">The object implements **IConnectionPointContainer**.</span></span>

### <a name="flags"></a><span data-ttu-id="c6636-129">Flags</span><span class="sxs-lookup"><span data-stu-id="c6636-129">Flags</span></span>

<span data-ttu-id="c6636-130">impltypeflag \_ f Source, varflag \_ Source, funcflag \_ Source</span><span class="sxs-lookup"><span data-stu-id="c6636-130">IMPLTYPEFLAG\_FSOURCE, VARFLAG\_SOURCE, FUNCFLAG\_SOURCE</span></span>

## <a name="examples"></a><span data-ttu-id="c6636-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6636-131">Examples</span></span>

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a><span data-ttu-id="c6636-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6636-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6636-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="c6636-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="c6636-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="c6636-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="c6636-135">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="c6636-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c6636-136">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="c6636-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="c6636-137">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="c6636-137">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c6636-138">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="c6636-138">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c6636-139">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="c6636-139">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 