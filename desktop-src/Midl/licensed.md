---
title: licensed-Attribut
description: Das Attribut \ lizenzierte \ gibt an, dass die Co-Klasse, auf die es angewendet wird, lizenziert ist und mit IClassFactory2 instanziiert werden muss.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- lizenzierte Attribute-Mittel l
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038859"
---
# <a name="licensed-attribute"></a><span data-ttu-id="f3818-104">licensed-Attribut</span><span class="sxs-lookup"><span data-stu-id="f3818-104">licensed attribute</span></span>

<span data-ttu-id="f3818-105">Das **\[ lizenzierte \]** Attribut gibt an, dass die [**Co-Klasse**](coclass.md) , auf die Sie angewendet wird, lizenziert ist und mit [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)instanziiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="f3818-105">The **\[licensed\]** attribute indicates that the [**coclass**](coclass.md) to which it applies is licensed, and must be instantiated using [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span></span>

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a><span data-ttu-id="f3818-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3818-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3818-107">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="f3818-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f3818-108">Gibt 0 (null) oder mehr Attribute an, die für die [**Co-Klasse**](coclass.md) -Anweisung gelten.</span><span class="sxs-lookup"><span data-stu-id="f3818-108">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="f3818-109">Zulässige **Co-Klasse** -Attribute sind **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ lizenziert \]**, **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** und **\[** [**Hidden**](hidden.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f3818-109">Allowable **coclass** attributes are **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[licensed\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, and **\[**[**hidden**](hidden.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f3818-110">*classname*</span><span class="sxs-lookup"><span data-stu-id="f3818-110">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="f3818-111">Gibt den Namen an, mit dem das Komponenten Objekt in der Typbibliothek bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f3818-111">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="f3818-112">*coclass-Definition*</span><span class="sxs-lookup"><span data-stu-id="f3818-112">*coclass-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="f3818-113">Gibt die-Anweisungen an, die die [**Co-Klassen**](coclass.md) Definition bilden.</span><span class="sxs-lookup"><span data-stu-id="f3818-113">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3818-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3818-114">Remarks</span></span>

<span data-ttu-id="f3818-115">Die Lizenzierung ist eine Funktion von com, die die Kontrolle über die Objekt Erstellung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f3818-115">Licensing is a feature of COM that provides control over object creation.</span></span> <span data-ttu-id="f3818-116">Lizenzierte Objekte können nur von Clients erstellt werden, die zur Verwendung autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f3818-116">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="f3818-117">Die Lizenzierung wird in com über die [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) -Schnittstelle und durch Unterstützung eines Lizenzschlüssels implementiert, der zur Laufzeit übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3818-117">Licensing is implemented in COM through the [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

### <a name="flags"></a><span data-ttu-id="f3818-118">Flags</span><span class="sxs-lookup"><span data-stu-id="f3818-118">Flags</span></span>

<span data-ttu-id="f3818-119">TYPEFLAG \_ geflichtet</span><span class="sxs-lookup"><span data-stu-id="f3818-119">TYPEFLAG\_FLICENSED</span></span>

## <a name="examples"></a><span data-ttu-id="f3818-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3818-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a><span data-ttu-id="f3818-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f3818-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3818-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="f3818-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="f3818-123">Inhalt einer Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f3818-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="f3818-124">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="f3818-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="f3818-125">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="f3818-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f3818-126">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="f3818-126">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="f3818-127">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="f3818-127">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="f3818-128">**verbirgt**</span><span class="sxs-lookup"><span data-stu-id="f3818-128">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="f3818-129">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="f3818-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f3818-130">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="f3818-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="f3818-131">**Version**</span><span class="sxs-lookup"><span data-stu-id="f3818-131">**version**</span></span>](version.md)
</dt> </dl>

 

 