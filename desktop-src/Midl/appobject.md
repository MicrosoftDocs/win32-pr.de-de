---
title: appobject-Attribut
description: Das Attribut \ appobject \ identifiziert die Co-Klasse als Anwendungs Objekt, das einer vollständigen exe-Anwendung zugeordnet ist.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- appobject-Attribut-Mittel l
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390201"
---
# <a name="appobject-attribute"></a><span data-ttu-id="f19b2-104">appobject-Attribut</span><span class="sxs-lookup"><span data-stu-id="f19b2-104">appobject attribute</span></span>

<span data-ttu-id="f19b2-105">Das **\[ appobject \]** -Attribut identifiziert die [**Co-Klasse**](coclass.md) als Anwendungs Objekt, das einer vollständigen exe-Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f19b2-105">The **\[appobject\]** attribute identifies the [**coclass**](coclass.md) as an application object, which is associated with a full EXE application.</span></span>

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a><span data-ttu-id="f19b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f19b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19b2-107">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="f19b2-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="f19b2-108">Gibt eine universell eindeutige Identifikationsnummer für die [**Co-Klasse**](coclass.md)an.</span><span class="sxs-lookup"><span data-stu-id="f19b2-108">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="f19b2-109">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f19b2-109">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f19b2-110">Gibt 0 (null) oder mehr Attribute an, die für die [**Co-Klasse**](coclass.md) -Anweisung gelten.</span><span class="sxs-lookup"><span data-stu-id="f19b2-110">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="f19b2-111">Zulässige **Co-Klasse** -Attribute sind [**\[ HelpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ lizenziert \]**](licensed.md), [**\[ Version \]**](version.md), [**\[ Control \]**](control.md)und [**\[ Hidden \]**](hidden.md).</span><span class="sxs-lookup"><span data-stu-id="f19b2-111">Allowable **coclass** attributes are [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[licensed\]**](licensed.md), [**\[version\]**](version.md), [**\[control\]**](control.md), and [**\[hidden\]**](hidden.md).</span></span>

</dd> <dt>

<span data-ttu-id="f19b2-112">*classname*</span><span class="sxs-lookup"><span data-stu-id="f19b2-112">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="f19b2-113">Gibt den Namen an, mit dem das Komponenten Objekt in der Typbibliothek bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f19b2-113">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="f19b2-114">*Co-Klassendefinition*</span><span class="sxs-lookup"><span data-stu-id="f19b2-114">*coclass definition*</span></span> 
</dt> <dd>

<span data-ttu-id="f19b2-115">Gibt die-Anweisungen an, die die [**Co-Klassen**](coclass.md) Definition bilden.</span><span class="sxs-lookup"><span data-stu-id="f19b2-115">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f19b2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f19b2-116">Remarks</span></span>

<span data-ttu-id="f19b2-117">Das **\[ appobject \]** -Attribut gibt auch an, dass die Funktionen und Eigenschaften der [**Co-Klasse**](coclass.md) in der aktuellen Typbibliothek global verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f19b2-117">The **\[appobject\]** attribute also indicates that the functions and properties of the [**coclass**](coclass.md) are globally available in the current type library.</span></span>

<span data-ttu-id="f19b2-118">Die TYPEFLAG-Darstellung für dieses Attribut ist "TYPEFLAG \_ fappobject".</span><span class="sxs-lookup"><span data-stu-id="f19b2-118">The typeflag representation for this attribute is TYPEFLAG\_FAPPOBJECT</span></span>

## <a name="examples"></a><span data-ttu-id="f19b2-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f19b2-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="f19b2-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f19b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19b2-121">**coclass**</span><span class="sxs-lookup"><span data-stu-id="f19b2-121">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="f19b2-122">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="f19b2-122">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="f19b2-123">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="f19b2-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f19b2-124">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="f19b2-124">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="f19b2-125">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="f19b2-125">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="f19b2-126">**verbirgt**</span><span class="sxs-lookup"><span data-stu-id="f19b2-126">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="f19b2-127">**lizenziert**</span><span class="sxs-lookup"><span data-stu-id="f19b2-127">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="f19b2-128">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="f19b2-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f19b2-129">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="f19b2-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f19b2-130">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="f19b2-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="f19b2-131">**Version**</span><span class="sxs-lookup"><span data-stu-id="f19b2-131">**version**</span></span>](version.md)
</dt> </dl>

 

 