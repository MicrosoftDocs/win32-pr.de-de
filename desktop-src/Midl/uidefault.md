---
title: uidefault-Attribut
description: Das Attribut \ Uidefault \ gibt an, dass das Typinformationsmember der Standard Member für die Anzeige in der Benutzeroberfläche ist.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- Uidefault-Attribut-Mittel l
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390171"
---
# <a name="uidefault-attribute"></a><span data-ttu-id="17f26-104">uidefault-Attribut</span><span class="sxs-lookup"><span data-stu-id="17f26-104">uidefault attribute</span></span>

<span data-ttu-id="17f26-105">Das **\[ Uidefault \]** -Attribut gibt an, dass der Typinformationsmember der Standard Member für die Anzeige in der Benutzeroberfläche ist.</span><span class="sxs-lookup"><span data-stu-id="17f26-105">The **\[uidefault\]** attribute indicates that the type information member is the default member for display in the user interface.</span></span>

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="17f26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17f26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f26-107">*Method-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="17f26-107">*method-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="17f26-108">Andere Attribute, die auf die-Methode angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="17f26-108">Other attributes that apply to the method.</span></span>

</dd> <dt>

<span data-ttu-id="17f26-109">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="17f26-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="17f26-110">Der Typ der Daten, die von der Methode zurückgegeben werden, wenn Sie die Ausführung beendet.</span><span class="sxs-lookup"><span data-stu-id="17f26-110">The type of the data that the method will return when it finishes execution.</span></span>

</dd> <dt>

<span data-ttu-id="17f26-111">*Methodenname*</span><span class="sxs-lookup"><span data-stu-id="17f26-111">*method-name*</span></span> 
</dt> <dd>

<span data-ttu-id="17f26-112">Der Name der Methode.</span><span class="sxs-lookup"><span data-stu-id="17f26-112">The name of the method.</span></span>

</dd> <dt>

<span data-ttu-id="17f26-113">*method-Parameter-List*</span><span class="sxs-lookup"><span data-stu-id="17f26-113">*method-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="17f26-114">NULL oder mehr Parameter für die Methode.</span><span class="sxs-lookup"><span data-stu-id="17f26-114">Zero or more parameters for the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17f26-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17f26-115">Remarks</span></span>

<span data-ttu-id="17f26-116">Wenn Sie das **\[ Uidefault \]** -Attribut auf einen Member einer Schnittstelle oder eine dispinterface anwenden, wird Visual Basic zur Entwurfszeit aufgefordert, das Ereignis oder die Eigenschaft automatisch für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="17f26-116">Applying the **\[uidefault\]** attribute to a member of an interface or a dispinterface tells Visual Basic, at design-time, to automatically display this event or property to the user.</span></span> <span data-ttu-id="17f26-117">Dies bedeutet Folgendes: Wenn der Benutzer auf ein Objekt doppelklickt, springt Visual Basic zum Ereignis in der standardmäßigen Quell Schnittstelle, das über das **\[ Uidefault \]** -Attribut verfügt.</span><span class="sxs-lookup"><span data-stu-id="17f26-117">This means that when the user double-clicks an object, Visual Basic jumps to the event in the default source interface that has the **\[uidefault\]** attribute.</span></span> <span data-ttu-id="17f26-118">Wenn der Benutzer ein Objekt auswählt, zeigt der Eigenschaften Browser Visual Basic die Eigenschaft in der standardmäßigen Quell Schnittstelle an, die über dieses Attribut verfügt.</span><span class="sxs-lookup"><span data-stu-id="17f26-118">When the user selects an object, Visual Basic's Properties browser displays the property in the default source interface that has this attribute.</span></span> <span data-ttu-id="17f26-119">Wenn kein Ereignis oder keine Eigenschaft über das **\[ Uidefault \]** -Attribut verfügt, zeigt Visual Basic das erste Ereignis oder die Eigenschaft an, das in der Standardschnittstelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="17f26-119">If no event or property has the **\[uidefault\]** attribute, Visual Basic displays the first event or property listed in the default interface.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="17f26-120">TYPEFLAG-Darstellung</span><span class="sxs-lookup"><span data-stu-id="17f26-120">Typeflag Representation</span></span>

<span data-ttu-id="17f26-121">Das vorhanden sein von funcflag \_ fuidefault oder varflag \_ fuidefault</span><span class="sxs-lookup"><span data-stu-id="17f26-121">The presence of FUNCFLAG\_FUIDEFAULT or VARFLAG\_FUIDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="17f26-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17f26-122">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="17f26-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="17f26-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f26-124">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="17f26-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="17f26-125">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="17f26-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="17f26-126">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="17f26-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 