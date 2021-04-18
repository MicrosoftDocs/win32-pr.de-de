---
title: ausgeblendetes Attribut
description: Das Attribut \ Hidden \ gibt an, dass das Element vorhanden ist, aber nicht in einem benutzerorientierten Browser angezeigt werden sollte.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- Hidden-Attribut, Mittel
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337645"
---
# <a name="hidden-attribute"></a><span data-ttu-id="83968-104">ausgeblendetes Attribut</span><span class="sxs-lookup"><span data-stu-id="83968-104">hidden attribute</span></span>

<span data-ttu-id="83968-105">Das **\[ Hidden \]** -Attribut gibt an, dass das Element vorhanden ist, aber nicht in einem benutzerorientierten Browser angezeigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="83968-105">The **\[hidden\]** attribute indicates that the item exists but should not be displayed in a user-oriented browser.</span></span>

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="83968-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83968-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83968-107">*andere-Attribute*</span><span class="sxs-lookup"><span data-stu-id="83968-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="83968-108">NULL oder mehr optionale Mittelwert Attribute.</span><span class="sxs-lookup"><span data-stu-id="83968-108">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="83968-109">*gewisses*</span><span class="sxs-lookup"><span data-stu-id="83968-109">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="83968-110">Eine der folgenden Direktiven: " [**Co-Klasse**](coclass.md)", " [**dispinterface**](dispinterface.md)", " [**Interface**](interface.md)" oder " [**Library**](library.md)".</span><span class="sxs-lookup"><span data-stu-id="83968-110">One of the following directives: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), or [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="83968-111">*Elementname*</span><span class="sxs-lookup"><span data-stu-id="83968-111">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="83968-112">Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element zu definieren.</span><span class="sxs-lookup"><span data-stu-id="83968-112">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="83968-113">*definiert*</span><span class="sxs-lookup"><span data-stu-id="83968-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="83968-114">Gibt die-Anweisungen an, die die Element Definition bilden.</span><span class="sxs-lookup"><span data-stu-id="83968-114">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="83968-115">*Funktionstyp*</span><span class="sxs-lookup"><span data-stu-id="83968-115">*function-type*</span></span> 
</dt> <dd>

<span data-ttu-id="83968-116">Der Rückgabetyp der Funktion.</span><span class="sxs-lookup"><span data-stu-id="83968-116">Return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="83968-117">*function-name*</span><span class="sxs-lookup"><span data-stu-id="83968-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="83968-118">Der Name, der zum Aufrufen der Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83968-118">Name used for invoking the function.</span></span>

</dd> <dt>

<span data-ttu-id="83968-119">*Optional-Parameter-List*</span><span class="sxs-lookup"><span data-stu-id="83968-119">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="83968-120">NULL oder mehr Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="83968-120">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83968-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83968-121">Remarks</span></span>

<span data-ttu-id="83968-122">Mit dem ausgeblendeten Attribut können Sie Elemente aus der Schnittstelle entfernen (indem Sie Sie vor der weiteren Verwendung schützen) und gleichzeitig die Kompatibilität mit vorhandenem Code beibehalten **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="83968-122">The **\[hidden\]** attribute allows you to remove members from your interface (by shielding them from further use) while maintaining compatibility with existing code.</span></span> <span data-ttu-id="83968-123">Sie können das **\[ Hidden \]** -Attribut für Eigenschaften, Methoden und die Anweisungen [**Co-Klasse**](coclass.md), [**dispinterface**](dispinterface.md), [**Interface**](interface.md)und [**Library**](library.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="83968-123">You can use the **\[hidden\]** attribute on properties, methods, and the [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), and [**library**](library.md) statements.</span></span>

<span data-ttu-id="83968-124">Wenn es für eine Bibliothek angegeben ist, verhindert das **\[ Hidden \]** -Attribut, dass die gesamte Bibliothek angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83968-124">When specified for a library, the **\[hidden\]** attribute prevents the entire library from being displayed.</span></span> <span data-ttu-id="83968-125">Dies ist für die Verwendung mit Steuerelementen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="83968-125">This usage is intended for use with controls.</span></span> <span data-ttu-id="83968-126">Hosts müssen eine neue Typbibliothek erstellen, die das Steuerelement mit erweiterten Eigenschaften umschließt.</span><span class="sxs-lookup"><span data-stu-id="83968-126">Hosts need to create a new type library that wraps the control with extended properties.</span></span>

### <a name="flags"></a><span data-ttu-id="83968-127">Flags</span><span class="sxs-lookup"><span data-stu-id="83968-127">Flags</span></span>

<span data-ttu-id="83968-128">varflag, ausgeblendetes funkflag, ausgeblendetes " \_ \_ TYPEFLAG" \_</span><span class="sxs-lookup"><span data-stu-id="83968-128">VARFLAG\_FHIDDEN, FUNCFLAG\_FHIDDEN, TYPEFLAG\_FHIDDEN</span></span>

## <a name="examples"></a><span data-ttu-id="83968-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83968-129">Examples</span></span>

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="83968-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83968-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83968-131">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="83968-131">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="83968-132">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="83968-132">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="83968-133">**coclass**</span><span class="sxs-lookup"><span data-stu-id="83968-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="83968-134">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="83968-134">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="83968-135">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="83968-135">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="83968-136">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="83968-136">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="83968-137">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="83968-137">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="83968-138">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="83968-138">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 