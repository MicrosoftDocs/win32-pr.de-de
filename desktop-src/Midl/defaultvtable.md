---
title: defaultvtable-Attribut
description: Das Attribut "\ defaultvtable \" definiert eine Schnittstelle als standardmäßige Vtable-Schnittstelle.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- defaultvtable-Attribut-Mittel l
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858224"
---
# <a name="defaultvtable-attribute"></a><span data-ttu-id="7ea01-104">defaultvtable-Attribut</span><span class="sxs-lookup"><span data-stu-id="7ea01-104">defaultvtable attribute</span></span>

<span data-ttu-id="7ea01-105">Das **\[ defaultvtable \]** -Attribut definiert eine Schnittstelle als standardmäßige Vtable-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7ea01-105">The **\[defaultvtable\]** attribute defines an interface as the default Vtable interface.</span></span>

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="7ea01-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ea01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea01-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7ea01-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7ea01-108">Andere Attribute, die auf die-Klasse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ea01-108">Other attributes that apply to the class.</span></span> <span data-ttu-id="7ea01-109">Die **\[** Attribute " [**Source**](source.md) " **\]** und " **\[** [**UUID**](uuid.md) " **\]** sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7ea01-109">The **\[**[**source**](source.md)**\]** and **\[**[**uuid**](uuid.md)**\]** attributes are required.</span></span>

</dd> <dt>

<span data-ttu-id="7ea01-110">*Name der Co-Klasse*</span><span class="sxs-lookup"><span data-stu-id="7ea01-110">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7ea01-111">Der Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="7ea01-111">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="7ea01-112">*coclass-Interface-List*</span><span class="sxs-lookup"><span data-stu-id="7ea01-112">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7ea01-113">Eine Liste der Schnittstellen für die-Klasse.</span><span class="sxs-lookup"><span data-stu-id="7ea01-113">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ea01-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ea01-114">Remarks</span></span>

<span data-ttu-id="7ea01-115">Eine standardmäßige Vtable-Schnittstelle kann keine dispinterface sein – Sie muss eine Dual-oder Vtable-oder-Schnittstelle sein.</span><span class="sxs-lookup"><span data-stu-id="7ea01-115">A default Vtable interface cannot be a dispinterface—it must be a dual or Vtable or interface.</span></span> <span data-ttu-id="7ea01-116">Wenn die Schnittstelle eine duale Schnittstelle ist, können senken davon ausgehen, dass Sie Ereignisse über Vtable empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="7ea01-116">If the interface is a dual interface, then sinks can assume that they will receive events through Vtable.</span></span>

<span data-ttu-id="7ea01-117">Eine Klasse kann eine standardmäßige Quell Schnittstelle und eine standardmäßige Vtable-Quell Schnittstelle sein, wie im Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ea01-117">A class can be both a default source interface and a default Vtable source interface as shown in the example.</span></span> <span data-ttu-id="7ea01-118">In diesem Fall sollte eine Anweisungs Senke IID \_ IDispatch verwenden, um dispatchereignisse zu empfangen und den Schnittstellen Bezeichner zum Empfangen von Vtable-Ereignissen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ea01-118">In this case an advise sink should use IID\_IDISPATCH to receive dispatch events and use the interface identifier to receive Vtable events.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="7ea01-119">TYPEFLAG-Darstellung</span><span class="sxs-lookup"><span data-stu-id="7ea01-119">Typeflag Representation</span></span>

<span data-ttu-id="7ea01-120">Das vorhanden sein von impltypeflag \_ fdefaultvtable.</span><span class="sxs-lookup"><span data-stu-id="7ea01-120">The presence of IMPLTYPEFLAG\_FDEFAULTVTABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="7ea01-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ea01-121">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7ea01-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ea01-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea01-123">**coclass**</span><span class="sxs-lookup"><span data-stu-id="7ea01-123">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="7ea01-124">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="7ea01-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7ea01-125">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="7ea01-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7ea01-126">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="7ea01-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7ea01-127">**Ausgangs**</span><span class="sxs-lookup"><span data-stu-id="7ea01-127">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="7ea01-128">**UUID**</span><span class="sxs-lookup"><span data-stu-id="7ea01-128">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 