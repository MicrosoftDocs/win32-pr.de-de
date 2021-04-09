---
title: helpcontext-Attribut
description: Das Attribut \ HelpContext \ gibt einen Kontext Bezeichner an, mit dem der Benutzerinformationen zu diesem Element in der Hilfedatei anzeigen kann.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- HelpContext-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948643"
---
# <a name="helpcontext-attribute"></a><span data-ttu-id="b6812-104">helpcontext-Attribut</span><span class="sxs-lookup"><span data-stu-id="b6812-104">helpcontext attribute</span></span>

<span data-ttu-id="b6812-105">Das \[ **HelpContext** - \] Attribut gibt einen Kontext Bezeichner an, mit dem der Benutzerinformationen zu diesem Element in der Hilfedatei anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="b6812-105">The \[**helpcontext**\] attribute specifies a context identifier that lets the user view information about this element in the Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a><span data-ttu-id="b6812-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6812-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6812-107">*UUID-Nummer*</span><span class="sxs-lookup"><span data-stu-id="b6812-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="b6812-108">Gibt eine universell eindeutige ID für die [**Bibliothek**](library.md), die \[ [**importlib**](importlib.md) \] , die [**Schnittstelle**](interface.md), die [**dispinterface**](dispinterface.md), das [**Modul**](module.md), die [**typedef**](typedef.md), die **Methoden**, die **\[ Eigenschaft \]** oder die Co- [**Klasse**](coclass.md)an.</span><span class="sxs-lookup"><span data-stu-id="b6812-108">Specifies a universally unique identification number for the [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[property\]**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6812-109">*HelpContext-Wert*</span><span class="sxs-lookup"><span data-stu-id="b6812-109">*helpcontext-value*</span></span> 
</dt> <dd>

<span data-ttu-id="b6812-110">Eine eindeutige ganze Zahl, die den Hilfetext identifiziert, der dem aktuellen Mittel l-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b6812-110">A unique integer that identifies the help text associated with the current MIDL element.</span></span>

</dd> <dt>

<span data-ttu-id="b6812-111">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="b6812-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b6812-112">Gibt eine Liste mit einem oder mehreren Attributen an, die auf das Mittel l-Element als Ganzes angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6812-112">Specifies a list of one or more attributes that apply to the MIDL element as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="b6812-113">*gewisses*</span><span class="sxs-lookup"><span data-stu-id="b6812-113">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="b6812-114">Eine der folgenden Direktiven: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **method**, **Property** oder [**Co-Klasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b6812-114">One of the following directives: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6812-115">*Elementname*</span><span class="sxs-lookup"><span data-stu-id="b6812-115">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b6812-116">Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b6812-116">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="b6812-117">*definiert*</span><span class="sxs-lookup"><span data-stu-id="b6812-117">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="b6812-118">Gibt die-Anweisungen an, die die Element Definition bilden.</span><span class="sxs-lookup"><span data-stu-id="b6812-118">Specifies statements that make up the element definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6812-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6812-119">Remarks</span></span>

<span data-ttu-id="b6812-120">Das \[ **HelpContext** - \] Attribut kann auf die folgenden Elemente angewendet werden: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **method**, **Property** oder [**Co-Klasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b6812-120">The \[**helpcontext**\] attribute can be applied to the following elements: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

<span data-ttu-id="b6812-121">Der *HelpContext-Wert* ist ein 32-Bit-Kontext Bezeichner in der Hilfedatei, der mit den [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) -Funktionen in der [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) -Schnittstelle und der [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) -Schnittstelle abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6812-121">The *helpcontext-value* is a 32-bit context identifier within the Help file that can be retrieved with the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="b6812-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6812-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="b6812-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b6812-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6812-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="b6812-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="b6812-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="b6812-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="b6812-126">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="b6812-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b6812-127">**importlib**</span><span class="sxs-lookup"><span data-stu-id="b6812-127">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="b6812-128">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="b6812-128">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="b6812-129">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="b6812-129">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="b6812-130">**Mond**</span><span class="sxs-lookup"><span data-stu-id="b6812-130">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="b6812-131">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b6812-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b6812-132">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="b6812-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b6812-133">**typedef**</span><span class="sxs-lookup"><span data-stu-id="b6812-133">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 