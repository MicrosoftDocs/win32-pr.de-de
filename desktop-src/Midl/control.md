---
title: Control-Attribut
description: Das \ Control \-Attribut identifiziert eine Co-Klasse oder eine Bibliothek als com-Steuerelement, aus dem eine Container Site zusätzliche Typbibliotheken oder Komponenten Objektklassen ableitet.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- Steuerelement Attribut-Mittel l
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724953"
---
# <a name="control-attribute"></a><span data-ttu-id="ba013-104">Control-Attribut</span><span class="sxs-lookup"><span data-stu-id="ba013-104">control attribute</span></span>

<span data-ttu-id="ba013-105">Das **\[ Control \]** -Attribut identifiziert eine [**Co-Klasse**](coclass.md) oder eine [**Bibliothek**](library.md) als com-Steuerelement, aus dem eine Container Site zusätzliche Typbibliotheken oder Komponenten Objektklassen ableitet.</span><span class="sxs-lookup"><span data-stu-id="ba013-105">The **\[control\]** attribute identifies a [**coclass**](coclass.md) or [**library**](library.md) as a COM control, from which a container site will derive additional type libraries or component object classes.</span></span>

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a><span data-ttu-id="ba013-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba013-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba013-107">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="ba013-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ba013-108">Gibt 0 (null) oder mehr Attribute an, die für die [**Library**](library.md) -oder [**Co-Klasse**](coclass.md) -Anweisung gelten.</span><span class="sxs-lookup"><span data-stu-id="ba013-108">Specifies zero or more attributes that apply to the [**library**](library.md) or [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="ba013-109">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="ba013-109">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ba013-110">*lib-oder-CoClassname*</span><span class="sxs-lookup"><span data-stu-id="ba013-110">*lib-or-coclassname*</span></span> 
</dt> <dd>

<span data-ttu-id="ba013-111">Gibt den Namen der [**Bibliothek**](library.md) oder der [**Co-Klasse**](coclass.md)an.</span><span class="sxs-lookup"><span data-stu-id="ba013-111">Specifies the name of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba013-112">*definiert*</span><span class="sxs-lookup"><span data-stu-id="ba013-112">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="ba013-113">Mittel l-Anweisungen, die die Member der [**Bibliothek**](library.md) oder der [**Co-Klasse**](coclass.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="ba013-113">MIDL statements that specify the members of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba013-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba013-114">Remarks</span></span>

<span data-ttu-id="ba013-115">Mit diesem Attribut können Sie Typbibliotheken markieren, die Steuerelemente beschreiben, sodass Sie nicht in Typbrowsern angezeigt werden, die für nicht visuelle Objekte bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="ba013-115">This attribute allows you to mark type libraries that describe controls so they will not be displayed in type browsers intended for nonvisual objects.</span></span>

### <a name="flags"></a><span data-ttu-id="ba013-116">Flags</span><span class="sxs-lookup"><span data-stu-id="ba013-116">Flags</span></span>

<span data-ttu-id="ba013-117">TYPEFLAG-Steuerelement \_ , libflag \_ -Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ba013-117">TYPEFLAG\_FCONTROL, LIBFLAG\_FCONTROL</span></span>

## <a name="examples"></a><span data-ttu-id="ba013-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba013-118">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a><span data-ttu-id="ba013-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ba013-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba013-120">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="ba013-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="ba013-121">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="ba013-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ba013-122">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="ba013-122">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ba013-123">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="ba013-123">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="ba013-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="ba013-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="ba013-125">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="ba013-125">**library**</span></span>](library.md)
</dt> </dl>

 

 