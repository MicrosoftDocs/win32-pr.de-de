---
title: Standardattribut
description: Das \ default \-Attribut gibt an, dass die Schnittstelle oder die dispinterface, die innerhalb einer Co-Klasse definiert ist, die standardmäßige Programmierbarkeits Schnittstelle darstellt Dieses Attribut ist für die Verwendung durch Makro Sprachen vorgesehen.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- Standard Attribut-Mittell
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472845"
---
# <a name="default-attribute"></a><span data-ttu-id="788f4-105">Standardattribut</span><span class="sxs-lookup"><span data-stu-id="788f4-105">default attribute</span></span>

<span data-ttu-id="788f4-106">Das **\[ Default \]** -Attribut gibt an, dass die [**Schnitt**](interface.md) Stelle oder die in einer [**Co-Klasse**](coclass.md)definierte [**dispinterface**](dispinterface.md)die standardprogrammierbarkeits-Schnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="788f4-106">The **\[default\]** attribute Indicates that the [**interface**](interface.md) or [**dispinterface**](dispinterface.md), defined within a [**coclass**](coclass.md), represents the default programmability interface.</span></span> <span data-ttu-id="788f4-107">Dieses Attribut ist für die Verwendung durch Makro Sprachen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="788f4-107">This attribute is intended for use by macro languages.</span></span>

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a><span data-ttu-id="788f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="788f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="788f4-109">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="788f4-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="788f4-110">Gibt eine universell eindeutige Identifikationsnummer für die [**Co-Klasse**](coclass.md)an.</span><span class="sxs-lookup"><span data-stu-id="788f4-110">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="788f4-111">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="788f4-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="788f4-112">Gibt zusätzliche [**Co-Klasse**](coclass.md) -Attribute an.</span><span class="sxs-lookup"><span data-stu-id="788f4-112">Specifies additional [**coclass**](coclass.md) attributes.</span></span> <span data-ttu-id="788f4-113">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="788f4-113">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="788f4-114">*Name der Co-Klasse*</span><span class="sxs-lookup"><span data-stu-id="788f4-114">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="788f4-115">Gibt den Namen an, mit dem andere Softwarekomponenten auf diese [**Co-Klasse**](coclass.md)verweisen können.</span><span class="sxs-lookup"><span data-stu-id="788f4-115">Specifies the name by which other software components can reference this [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="788f4-116">*optional-Interface-Attribute*</span><span class="sxs-lookup"><span data-stu-id="788f4-116">*optional-interface-attribute*</span></span> 
</dt> <dd>

<span data-ttu-id="788f4-117">Das **\[** [**Quell**](source.md) **\]** Attribut, das angibt, dass eine Schnittstelle oder eine dispinterface ausgehend ist, ist das einzige andere Attribut, das hier verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="788f4-117">The **\[**[**source**](source.md)**\]** attribute, which specifies that an interface or dispinterface is outgoing, is the only other attribute that can be used here.</span></span>

</dd> <dt>

<span data-ttu-id="788f4-118">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="788f4-118">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="788f4-119">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="788f4-119">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="788f4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="788f4-120">Remarks</span></span>

<span data-ttu-id="788f4-121">Eine [**Co-Klasse**](coclass.md) kann höchstens zwei **\[ Standardmember \]** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="788f4-121">A [**coclass**](coclass.md) may have at most two **\[default\]** members.</span></span> <span data-ttu-id="788f4-122">Eine stellt die ausgehende (Quell-) Schnittstelle oder dispinterface dar, während die andere die eingehende Schnittstelle (Senke) oder "dispinterface" darstellt.</span><span class="sxs-lookup"><span data-stu-id="788f4-122">One represents the outgoing (source) interface or dispinterface, and the other represents the incoming (sink) interface or dispinterface.</span></span> <span data-ttu-id="788f4-123">Wenn das **\[ Default \]** -Attribut für keinen Member der **Co-Klasse** oder des **cotype**-Elements angegeben ist, werden die ersten ausgehenden und eingehenden Member, die nicht über das restricted-Attribut verfügen, **\[** [](restricted.md) **\]** als Standardwerte behandelt.</span><span class="sxs-lookup"><span data-stu-id="788f4-123">If the **\[default\]** attribute is not specified for any member of the **coclass** or **cotype**, the first outgoing and incoming members that do not have the **\[**[**restricted**](restricted.md)**\]** attribute are treated as the defaults.</span></span>

### <a name="flags"></a><span data-ttu-id="788f4-124">Flags</span><span class="sxs-lookup"><span data-stu-id="788f4-124">Flags</span></span>

<span data-ttu-id="788f4-125">impltypeflag (Standardwert) \_</span><span class="sxs-lookup"><span data-stu-id="788f4-125">IMPLTYPEFLAG\_FDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="788f4-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="788f4-126">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a><span data-ttu-id="788f4-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="788f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788f4-128">**coclass**</span><span class="sxs-lookup"><span data-stu-id="788f4-128">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="788f4-129">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="788f4-129">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="788f4-130">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="788f4-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="788f4-131">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="788f4-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="788f4-132">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="788f4-132">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="788f4-133">**begrenz**</span><span class="sxs-lookup"><span data-stu-id="788f4-133">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="788f4-134">**Ausgangs**</span><span class="sxs-lookup"><span data-stu-id="788f4-134">**source**</span></span>](source.md)
</dt> </dl>

 

 