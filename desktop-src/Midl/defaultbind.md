---
title: defaultbind-Attribut
description: Das Attribut "\ Defaultbind \" gibt die einzelne, bindbare Eigenschaft an, die das Objekt am besten darstellt.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- Defaultbind-Attribut-Mittel l
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038963"
---
# <a name="defaultbind-attribute"></a><span data-ttu-id="b8f0d-104">defaultbind-Attribut</span><span class="sxs-lookup"><span data-stu-id="b8f0d-104">defaultbind attribute</span></span>

<span data-ttu-id="b8f0d-105">Das **\[ Defaultbind \]** -Attribut gibt die einzelne, bindbare Eigenschaft an, die das Objekt am besten darstellt.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-105">The **\[defaultbind\]** attribute indicates the single, bindable property that best represents the object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="b8f0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8f0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f0d-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b8f0d-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f0d-108">Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="b8f0d-109">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="b8f0d-110">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="b8f0d-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f0d-111">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="b8f0d-112">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="b8f0d-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f0d-113">Gibt eine Liste mit mindestens einem Attribut an, das für die Funktion gilt.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-113">Specifies a list of one or more attributes that apply to the function.</span></span> <span data-ttu-id="b8f0d-114">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-114">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="b8f0d-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="b8f0d-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f0d-116">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="b8f0d-117">*function-name*</span><span class="sxs-lookup"><span data-stu-id="b8f0d-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f0d-118">Gibt den Namen der Funktion an, auf die das **\[ Defaultbind \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-118">Specifies the name of the function to which the **\[defaultbind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="b8f0d-119">*params*</span><span class="sxs-lookup"><span data-stu-id="b8f0d-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f0d-120">Funktionsparameter Liste.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8f0d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8f0d-121">Remarks</span></span>

<span data-ttu-id="b8f0d-122">Eigenschaften, die über das **\[ Defaultbind \]** -Attribut verfügen, müssen auch über das **\[** [**bindbare**](bindable.md) **\]** Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-122">Properties that have the **\[defaultbind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="b8f0d-123">Nur eine Eigenschaft in einer Schnittstelle oder einem Dispinterface-Attribut kann das **\[ Defaultbind \]** -Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-123">Only one property in an interface or dispinterface can have the **\[defaultbind\]** attribute.</span></span>

<span data-ttu-id="b8f0d-124">Dieses Attribut wird von Containern verwendet, die ein Benutzer Modell enthalten, das die Bindung an ein Objekt und nicht die Bindung an eine Eigenschaft eines Objekts umfasst.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-124">This attribute is used by containers that have a user model involving binding to an object rather than binding to a property of an object.</span></span> <span data-ttu-id="b8f0d-125">Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="b8f0d-125">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="b8f0d-126">Flags</span><span class="sxs-lookup"><span data-stu-id="b8f0d-126">Flags</span></span>

<span data-ttu-id="b8f0d-127">funcflag " \_ sdefaultbind", varflag " \_ sdefaultbind"</span><span class="sxs-lookup"><span data-stu-id="b8f0d-127">FUNCFLAG\_FDEFAULTBIND, VARFLAG\_FDEFAULTBIND</span></span>

## <a name="examples"></a><span data-ttu-id="b8f0d-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8f0d-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="b8f0d-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b8f0d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f0d-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="b8f0d-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="b8f0d-131">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="b8f0d-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b8f0d-132">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b8f0d-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b8f0d-133">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b8f0d-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b8f0d-134">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="b8f0d-134">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 