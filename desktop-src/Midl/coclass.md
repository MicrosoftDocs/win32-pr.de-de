---
title: Co-Klasse-Attribut
description: Die Co-Klasse-Anweisung stellt eine Auflistung der unterstützten Schnittstellen für ein Komponenten Objekt bereit.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- Co-Klasse-Attribut-Mittel l
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390252"
---
# <a name="coclass-attribute"></a><span data-ttu-id="4d649-104">Co-Klasse-Attribut</span><span class="sxs-lookup"><span data-stu-id="4d649-104">coclass attribute</span></span>

<span data-ttu-id="4d649-105">Die **Co-Klasse** -Anweisung stellt eine Auflistung der unterstützten Schnittstellen für ein Komponenten Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="4d649-105">The **coclass** statement provides a listing of the supported interfaces for a component object.</span></span>

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a><span data-ttu-id="4d649-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d649-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d649-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4d649-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4d649-108">Das **\[** [**UUID**](uuid.md) - **\]** Attribut ist für eine **Co-Klasse** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d649-108">The **\[**[**uuid**](uuid.md)**\]** attribute is required on a **coclass**.</span></span> <span data-ttu-id="4d649-109">Dabei handelt es sich um dieselbe **\[ UUID \]** , die in der System Registrierungsdatenbank als CLSID registriert ist.</span><span class="sxs-lookup"><span data-stu-id="4d649-109">This is the same **\[uuid\]** that is registered as a CLSID in the system registration database.</span></span> <span data-ttu-id="4d649-110">Die **\[** Attribute [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**lizenzierte**](licensed.md) **\]** , **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** und **\[** [**appobject**](appobject.md) **\]** werden vor einer **Co-Klassen** Definition akzeptiert, jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d649-110">The **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**licensed**](licensed.md)**\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, and **\[**[**appobject**](appobject.md)**\]** attributes are accepted, but not required, before a **coclass** definition.</span></span>

</dd> <dt>

<span data-ttu-id="4d649-111">*classname*</span><span class="sxs-lookup"><span data-stu-id="4d649-111">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="4d649-112">Der Name, mit dem das allgemeine Objekt in der Typbibliothek bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4d649-112">Name by which the common object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="4d649-113">*Interface-Attribute*</span><span class="sxs-lookup"><span data-stu-id="4d649-113">*interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="4d649-114">Optionale Attribute für die Schnittstelle oder die dispinterface.</span><span class="sxs-lookup"><span data-stu-id="4d649-114">Optional attributes for the interface or dispinterface.</span></span> <span data-ttu-id="4d649-115">Die **\[** Attribute [**Quelle**](source.md) **\]** , **\[** [**default**](default.md) **\]** und **\[** [**restricted**](restricted.md) **\]** werden für eine Schnittstelle oder eine dispinterface innerhalb einer **Co-Klasse** akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4d649-115">The **\[**[**source**](source.md)**\]**, **\[**[**default**](default.md)**\]**, and **\[**[**restricted**](restricted.md)**\]** attributes are accepted on an interface or dispinterface within a **coclass**.</span></span>

</dd> <dt>

<span data-ttu-id="4d649-116">*Schnittstellenname*</span><span class="sxs-lookup"><span data-stu-id="4d649-116">*interfacename*</span></span> 
</dt> <dd>

<span data-ttu-id="4d649-117">Entweder eine Schnittstelle, die mit dem Schlüsselwort " [**Interface**](interface.md) " deklariert wurde, oder eine mit dem Schlüsselwort " [**dispinterface**](dispinterface.md) " deklarierte</span><span class="sxs-lookup"><span data-stu-id="4d649-117">Either an interface declared with the [**interface**](interface.md) keyword, or a dispinterface declared with the [**dispinterface**](dispinterface.md) keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d649-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d649-118">Remarks</span></span>

<span data-ttu-id="4d649-119">Die Microsoft-Component Object Model definiert eine Klasse als eine-Implementierung, die **QueryInterface** zwischen einem Satz von Schnittstellen zulässt.</span><span class="sxs-lookup"><span data-stu-id="4d649-119">The Microsoft Component Object Model defines a class as an implementation that allows **QueryInterface** between a set of interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="4d649-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d649-120">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a><span data-ttu-id="4d649-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d649-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d649-122">**appobject**</span><span class="sxs-lookup"><span data-stu-id="4d649-122">**appobject**</span></span>](appobject.md)
</dt> <dt>

[<span data-ttu-id="4d649-123">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="4d649-123">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="4d649-124">**vorgegebene**</span><span class="sxs-lookup"><span data-stu-id="4d649-124">**default**</span></span>](default.md)
</dt> <dt>

[<span data-ttu-id="4d649-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="4d649-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="4d649-126">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="4d649-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="4d649-127">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="4d649-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4d649-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="4d649-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="4d649-129">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="4d649-129">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="4d649-130">**verbirgt**</span><span class="sxs-lookup"><span data-stu-id="4d649-130">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="4d649-131">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="4d649-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="4d649-132">**lizenziert**</span><span class="sxs-lookup"><span data-stu-id="4d649-132">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="4d649-133">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="4d649-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4d649-134">**begrenz**</span><span class="sxs-lookup"><span data-stu-id="4d649-134">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="4d649-135">**Ausgangs**</span><span class="sxs-lookup"><span data-stu-id="4d649-135">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="4d649-136">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="4d649-136">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="4d649-137">**UUID**</span><span class="sxs-lookup"><span data-stu-id="4d649-137">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="4d649-138">**version**</span><span class="sxs-lookup"><span data-stu-id="4d649-138">**version**</span></span>](version.md)
</dt> </dl>

 

 