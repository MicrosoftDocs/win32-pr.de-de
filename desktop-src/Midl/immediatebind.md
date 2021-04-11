---
title: immediatebind-Attribut
description: Das Attribut \ unmittelatebind \ gibt an, dass die Datenbank sofort über alle Änderungen an einer Eigenschaft eines Daten gebundenen Objekts benachrichtigt wird.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- unmittel-BIND-Attribut (Mittel l)
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208823"
---
# <a name="immediatebind-attribute"></a><span data-ttu-id="8144b-104">immediatebind-Attribut</span><span class="sxs-lookup"><span data-stu-id="8144b-104">immediatebind attribute</span></span>

<span data-ttu-id="8144b-105">Das **\[ unmittelatebind \]** -Attribut gibt an, dass die Datenbank sofort über alle Änderungen an einer Eigenschaft eines Daten gebundenen Objekts benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="8144b-105">The **\[immediatebind\]** attribute indicates that the database will be notified immediately of all changes to a property of a data-bound object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="8144b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8144b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8144b-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="8144b-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8144b-108">Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8144b-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="8144b-109">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="8144b-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8144b-110">Gibt den Namen der [**Schnittstelle**](interface.md) oder der " [**dispinterface**](dispinterface.md)" an.</span><span class="sxs-lookup"><span data-stu-id="8144b-110">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="8144b-111">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="8144b-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8144b-112">NULL oder mehr Funktions Attribute.</span><span class="sxs-lookup"><span data-stu-id="8144b-112">Zero or more function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="8144b-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="8144b-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="8144b-114">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="8144b-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="8144b-115">*function-name*</span><span class="sxs-lookup"><span data-stu-id="8144b-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8144b-116">Gibt den Namen der Funktion in der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="8144b-116">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="8144b-117">*params*</span><span class="sxs-lookup"><span data-stu-id="8144b-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="8144b-118">NULL oder mehr Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="8144b-118">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8144b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8144b-119">Remarks</span></span>

<span data-ttu-id="8144b-120">Das **\[ unmittelatebind \]** -Attribut ermöglicht es Steuerelementen, zwischen Eigenschaften zu unterscheiden, die die Datenbank über jede Änderung benachrichtigen müssen.</span><span class="sxs-lookup"><span data-stu-id="8144b-120">The **\[immediatebind\]** attribute allows controls to differentiate between properties that need to notify the database of every change, and those that do not.</span></span> <span data-ttu-id="8144b-121">So sollte beispielsweise jede Änderung an einem CheckBox-Steuerelement sofort an die zugrunde liegende Datenbank gesendet werden, auch wenn das Steuerelement den Fokus nicht verliert.</span><span class="sxs-lookup"><span data-stu-id="8144b-121">For example, every change to a checkbox control should be sent to the underlying database immediately, even if the control has not lost the focus.</span></span> <span data-ttu-id="8144b-122">Bei einem ListBox-Steuerelement tritt jedoch eine Änderung auf, wenn eine andere Auswahl hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="8144b-122">However, for a listbox control, a change occurs whenever a different selection is highlighted.</span></span> <span data-ttu-id="8144b-123">Das Benachrichtigen der Datenbank über eine Änderung, bevor das Steuerelement den Fokus verliert, wäre ineffizient und unnötig.</span><span class="sxs-lookup"><span data-stu-id="8144b-123">Notifying the database of a change before the control loses focus would be inefficient and unnecessary.</span></span> <span data-ttu-id="8144b-124">Mit dem Attribut " **\[ unmittelatebind \]** " können Sie angeben, indem Sie das unmittelatebind-Bit festlegen, einzelne Eigenschaften auf einem Formular, dessen Änderungen sofort gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8144b-124">The **\[immediatebind\]** attribute allows you to specify, by setting the ImmediateBind bit, individual properties on a form whose changes should be reported immediately.</span></span>

<span data-ttu-id="8144b-125">Eigenschaften, die über das **\[ unmittelatebind \]** -Attribut verfügen, müssen auch über das **\[** [**bindbare**](bindable.md) **\]** Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="8144b-125">Properties that have the **\[immediatebind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="8144b-126">Flags</span><span class="sxs-lookup"><span data-stu-id="8144b-126">Flags</span></span>

<span data-ttu-id="8144b-127">funkflag " \_ smediatebind", varflag " \_ fmmediatebind"</span><span class="sxs-lookup"><span data-stu-id="8144b-127">FUNCFLAG\_FIMMEDIATEBIND, VARFLAG\_FIMMEDIATEBIND</span></span>

## <a name="examples"></a><span data-ttu-id="8144b-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8144b-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="8144b-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8144b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8144b-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="8144b-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="8144b-131">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="8144b-131">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="8144b-132">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="8144b-132">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="8144b-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="8144b-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="8144b-134">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="8144b-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="8144b-135">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="8144b-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="8144b-136">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="8144b-136">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 