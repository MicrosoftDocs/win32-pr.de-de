---
title: defaultcollelem-Attribut
description: Das Attribut "\ Defaultcollelem \" markiert eine Eigenschaft als eine Accessorfunktion für ein Element der Standard Auflistung.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- Defaultcollelem-Attribut-Mittel l
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038936"
---
# <a name="defaultcollelem-attribute"></a><span data-ttu-id="7ee95-104">defaultcollelem-Attribut</span><span class="sxs-lookup"><span data-stu-id="7ee95-104">defaultcollelem attribute</span></span>

<span data-ttu-id="7ee95-105">Das **\[ Defaultcollelem \]** -Attribut markiert eine Eigenschaft als eine Accessorfunktion für ein Element der Standard Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7ee95-105">The **\[defaultcollelem\]** attribute flags a property as an accessor function for an element of the default collection.</span></span>

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="7ee95-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ee95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ee95-107">*Property-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7ee95-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee95-108">Andere Attribute, die auf die-Eigenschaft angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ee95-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="7ee95-109">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="7ee95-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee95-110">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="7ee95-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7ee95-111">*Eigenschaftsname*</span><span class="sxs-lookup"><span data-stu-id="7ee95-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee95-112">Den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ee95-112">The name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="7ee95-113">*Prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="7ee95-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee95-114">Eine Liste von NULL oder mehr Parametern, die der-Eigenschaft zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7ee95-114">A list of zero or more parameters associated with the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ee95-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ee95-115">Remarks</span></span>

<span data-ttu-id="7ee95-116">Das **\[ Defaultcollelem \]** -Attribut wird für die Codeoptimierung von Visual Basic® verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ee95-116">The **\[defaultcollelem\]** attribute is used for Visual BasicÂ® code optimization.</span></span> <span data-ttu-id="7ee95-117">Wenn ein Member einer Schnittstelle oder einer dispinterface als Accessorfunktion gekennzeichnet ist, wird der-Befehl direkt an diesen Member weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7ee95-117">If a member of an interface or dispinterface is flagged as an accessor function, then the call will go directly to that member.</span></span>

<span data-ttu-id="7ee95-118">Die Verwendung von **\[ Defaultcollelem \]** muss für eine Eigenschaft einheitlich sein.</span><span class="sxs-lookup"><span data-stu-id="7ee95-118">Use of **\[defaultcollelem\]** must be consistent for a property.</span></span> <span data-ttu-id="7ee95-119">Wenn Sie z. b. das-Attribut für eine *Get* -Eigenschaft verwenden, muss es auch in einer *Let* -Eigenschaft vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7ee95-119">For example, if you use the attribute on a *Get* property, it must also be present on a *Let* property.</span></span>

### <a name="typeflags-representation"></a><span data-ttu-id="7ee95-120">TYPEFLAGS-Darstellung</span><span class="sxs-lookup"><span data-stu-id="7ee95-120">Typeflags Representation</span></span>

<span data-ttu-id="7ee95-121">Das vorhanden sein von funkflag " \_ sdefaultcollelem" oder "varflag" mit dem Wert " \_ f".</span><span class="sxs-lookup"><span data-stu-id="7ee95-121">The presence of FUNCFLAG\_FDEFAULTCOLLELEM or VARFLAG\_FDEFAULTCOLLELEM.</span></span>

## <a name="examples"></a><span data-ttu-id="7ee95-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ee95-122">Examples</span></span>

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a><span data-ttu-id="7ee95-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ee95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee95-124">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="7ee95-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7ee95-125">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="7ee95-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7ee95-126">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="7ee95-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 