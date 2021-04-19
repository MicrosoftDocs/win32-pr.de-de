---
title: Bindbares Attribut
description: Das \ Bindable \-Attribut gibt an, dass die-Eigenschaft die Datenbindung unterstützt.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- bindbares Attribut, Mittel l
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341711"
---
# <a name="bindable-attribute"></a><span data-ttu-id="ccc17-104">Bindbares Attribut</span><span class="sxs-lookup"><span data-stu-id="ccc17-104">bindable attribute</span></span>

<span data-ttu-id="ccc17-105">Das **\[ bindbare \]** Attribut gibt an, dass die Eigenschaft die Datenbindung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ccc17-105">The **\[bindable\]** attribute indicates that the property supports data binding.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="ccc17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccc17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc17-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ccc17-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc17-108">Gibt eine Liste von 0 (null) oder mehr IDL-Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccc17-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="ccc17-109">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="ccc17-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="ccc17-110">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="ccc17-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc17-111">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="ccc17-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="ccc17-112">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="ccc17-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc17-113">Gibt 0 (null) oder mehr Attribute an, die für den Funktionsprototyp für eine Eigenschaft oder eine Methode in einer [**Schnittstelle**](interface.md) oder einem [**dispinterface**](dispinterface.md)-Objekt gelten.</span><span class="sxs-lookup"><span data-stu-id="ccc17-113">Specifies zero or more attributes that apply to the function prototype for a property or a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span> <span data-ttu-id="ccc17-114">Die folgenden Attribute sind gültig: [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ String \]**](string.md), [**\[ Defaultbind \]**](defaultbind.md), [**\[ Display Bind \]**](displaybind.md), [**\[ \] unmittelatebind**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ PROPPUT \]**](propput.md), [**\[ PROPPUTREF \]**](propputref.md)und [**\[ vararg \]**](vararg.md).</span><span class="sxs-lookup"><span data-stu-id="ccc17-114">The following attributes are valid: [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[string\]**](string.md), [**\[defaultbind\]**](defaultbind.md), [**\[displaybind\]**](displaybind.md), [**\[immediatebind\]**](immediatebind.md), [**\[propget\]**](propget.md), [**\[propput\]**](propput.md), [**\[propputref\]**](propputref.md), and [**\[vararg\]**](vararg.md).</span></span> <span data-ttu-id="ccc17-115">Wenn **vararg** angegeben ist, muss der letzte Parameter ein sicheres Array vom Typ Variant sein.</span><span class="sxs-lookup"><span data-stu-id="ccc17-115">If **vararg** is specified, the last parameter must be a safe array of type VARIANT.</span></span> <span data-ttu-id="ccc17-116">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="ccc17-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ccc17-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="ccc17-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc17-118">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="ccc17-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="ccc17-119">*function-name*</span><span class="sxs-lookup"><span data-stu-id="ccc17-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc17-120">Gibt den Namen der Funktion an, auf die das **\[ bindbare \]** Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccc17-120">Specifies the name of the function to which the **\[bindable\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="ccc17-121">*params*</span><span class="sxs-lookup"><span data-stu-id="ccc17-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc17-122">Funktionsparameter Liste.</span><span class="sxs-lookup"><span data-stu-id="ccc17-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccc17-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccc17-123">Remarks</span></span>

<span data-ttu-id="ccc17-124">Durch die Unterstützung der Datenbindung ermöglicht das **\[ bindbare \]** Attribut dem Client, immer dann benachrichtigt zu werden, wenn eine Eigenschaft den Wert geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ccc17-124">By supporting data binding, the **\[bindable\]** attribute allows the client to be notified whenever a property has changed value.</span></span> <span data-ttu-id="ccc17-125">(Wenn Sie möchten, dass der Client über bevorstehende Änderungen an einer Eigenschaft benachrichtigt wird, verwenden Sie das [**\[ requestedit \]**](requestedit.md) -Attribut.)</span><span class="sxs-lookup"><span data-stu-id="ccc17-125">(If you want the client to be notified of impending changes to a property, use the [**\[requestedit\]**](requestedit.md) attribute.)</span></span>

<span data-ttu-id="ccc17-126">Da das **\[ bindbare \]** Attribut auf die Eigenschaft als Ganzes verweist, muss es immer dann angegeben werden, wenn die Eigenschaft definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ccc17-126">Because the **\[bindable\]** attribute refers to the property as a whole, it must be specified wherever the property is defined.</span></span> <span data-ttu-id="ccc17-127">Daher müssen Sie das-Attribut für die Eigenschaften Zugriffs Funktion und die-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ccc17-127">Therefore, you need to specify the attribute on both the property-accessing function and the property-setting function.</span></span>

### <a name="flags"></a><span data-ttu-id="ccc17-128">Flags</span><span class="sxs-lookup"><span data-stu-id="ccc17-128">Flags</span></span>

<span data-ttu-id="ccc17-129">funcflag \_ FBindable, varflag \_ FBindable</span><span class="sxs-lookup"><span data-stu-id="ccc17-129">FUNCFLAG\_FBINDABLE, VARFLAG\_FBINDABLE</span></span>

## <a name="examples"></a><span data-ttu-id="ccc17-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccc17-130">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="ccc17-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ccc17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc17-132">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="ccc17-132">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="ccc17-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="ccc17-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="ccc17-134">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="ccc17-134">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="ccc17-135">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="ccc17-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ccc17-136">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="ccc17-136">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="ccc17-137">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="ccc17-137">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="ccc17-138">**immediatebind**</span><span class="sxs-lookup"><span data-stu-id="ccc17-138">**immediatebind**</span></span>](immediatebind.md)
</dt> <dt>

[<span data-ttu-id="ccc17-139">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="ccc17-139">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="ccc17-140">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="ccc17-140">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ccc17-141">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="ccc17-141">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="ccc17-142">**propget**</span><span class="sxs-lookup"><span data-stu-id="ccc17-142">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="ccc17-143">**propput**</span><span class="sxs-lookup"><span data-stu-id="ccc17-143">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="ccc17-144">**propputref**</span><span class="sxs-lookup"><span data-stu-id="ccc17-144">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="ccc17-145">**requestedit**</span><span class="sxs-lookup"><span data-stu-id="ccc17-145">**requestedit**</span></span>](requestedit.md)
</dt> <dt>

[<span data-ttu-id="ccc17-146">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ccc17-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="ccc17-147">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="ccc17-147">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="ccc17-148">**vararg**</span><span class="sxs-lookup"><span data-stu-id="ccc17-148">**vararg**</span></span>](vararg.md)
</dt> </dl>

 

 