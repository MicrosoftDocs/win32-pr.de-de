---
title: displaybind-Attribut
description: Das Attribut \ displaybind \ gibt eine Eigenschaft an, die dem Benutzer als Bindable angezeigt werden soll.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- Display BIND-Attribut (Mittell)
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725433"
---
# <a name="displaybind-attribute"></a><span data-ttu-id="9a208-104">displaybind-Attribut</span><span class="sxs-lookup"><span data-stu-id="9a208-104">displaybind attribute</span></span>

<span data-ttu-id="9a208-105">Das **\[ Display Bind \]** -Attribut gibt eine Eigenschaft an, die dem Benutzer als Bindable angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a208-105">The **\[displaybind\]** attribute indicates a property that should be displayed to the user as bindable.</span></span>

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="9a208-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a208-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9a208-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9a208-108">Gibt eine optionale Liste der Schnittstellen Attribute an.</span><span class="sxs-lookup"><span data-stu-id="9a208-108">Specifies an optional list of interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="9a208-109">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="9a208-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9a208-110">Der Name der Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9a208-110">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="9a208-111">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="9a208-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9a208-112">Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den Funktions Rückgabetyp angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a208-112">Specifies a list of one or more attributes, separated by commas, that apply to the function-return type.</span></span>

</dd> <dt>

<span data-ttu-id="9a208-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="9a208-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="9a208-114">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="9a208-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="9a208-115">*function-name*</span><span class="sxs-lookup"><span data-stu-id="9a208-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9a208-116">Gibt den Namen der Funktion an, auf die das **\[ Display Bind \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a208-116">Specifies the name of the function to which the **\[displaybind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="9a208-117">*params*</span><span class="sxs-lookup"><span data-stu-id="9a208-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="9a208-118">Funktionsparameter Liste.</span><span class="sxs-lookup"><span data-stu-id="9a208-118">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a208-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a208-119">Remarks</span></span>

<span data-ttu-id="9a208-120">Eigenschaften, die über das **\[ Display Bind \]** -Attribut verfügen, müssen auch über das **\[** [**bindbare**](bindable.md) **\]** Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="9a208-120">Properties that have the **\[displaybind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="9a208-121">Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="9a208-121">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="9a208-122">Flags</span><span class="sxs-lookup"><span data-stu-id="9a208-122">Flags</span></span>

<span data-ttu-id="9a208-123">funcflag " \_ f Display BIND", varflag " \_ sbind"</span><span class="sxs-lookup"><span data-stu-id="9a208-123">FUNCFLAG\_FDISPLAYBIND, VARFLAG\_FDISPLAYBIND</span></span>

## <a name="examples"></a><span data-ttu-id="9a208-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a208-124">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="9a208-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9a208-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a208-126">**bindable**</span><span class="sxs-lookup"><span data-stu-id="9a208-126">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="9a208-127">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="9a208-127">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="9a208-128">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="9a208-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9a208-129">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="9a208-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9a208-130">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="9a208-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 