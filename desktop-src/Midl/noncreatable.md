---
title: noncreatable-Attribut
description: Das Attribut \ nicht erstellbar \ definiert ein Objekt, das nicht allein instanziiert werden kann.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- nicht mit einem Attribut in der Mitte
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314810"
---
# <a name="noncreatable-attribute"></a><span data-ttu-id="d8f16-104">noncreatable-Attribut</span><span class="sxs-lookup"><span data-stu-id="d8f16-104">noncreatable attribute</span></span>

<span data-ttu-id="d8f16-105">Das **\[ nicht \]** Erstell Bare Attribut definiert ein Objekt, das nicht allein instanziiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8f16-105">The **\[noncreatable\]** attribute defines an object that cannot be instantiated by itself.</span></span>

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="d8f16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f16-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d8f16-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d8f16-108">Andere Attribute, die auf die-Klasse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8f16-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="d8f16-109">*Name der Co-Klasse*</span><span class="sxs-lookup"><span data-stu-id="d8f16-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d8f16-110">Der Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="d8f16-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="d8f16-111">*coclass-Interface-List*</span><span class="sxs-lookup"><span data-stu-id="d8f16-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d8f16-112">Eine Liste der Schnittstellen für die-Klasse.</span><span class="sxs-lookup"><span data-stu-id="d8f16-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8f16-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8f16-113">Remarks</span></span>

<span data-ttu-id="d8f16-114">Verwenden Sie das **\[ nicht \]** Erstell Bare Attribut in einer [**Co-Klasse**](coclass.md) -Anweisung, um Benutzern mitzuteilen, dass Sie kein neues Objekt dieser Klasse auf oberster Ebene erstellen können – d. h. durch Aufrufen von **CreateInstance** oder **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d8f16-114">Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**.</span></span> <span data-ttu-id="d8f16-115">Die Instanziierung eines Objekts dieser Klasse erfordert einen Methoden aufrufan ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="d8f16-115">Instantiation of an object of this class requires a method call to another object.</span></span> <span data-ttu-id="d8f16-116">In Microsoft Excel ist das "Cell"-Objekt z. b. nicht Erstell Bar und muss von einem Microsoft Excel-Arbeitsblatt Objekt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d8f16-116">For example, in Microsoft Excel, the "Cell" object is noncreatable and must be obtained from a Microsoft Excel Worksheet object.</span></span>

<span data-ttu-id="d8f16-117">Methoden, die Instanzen von nicht erstellbar baren Klassen zurückgeben, sollten den exakten Typ des Objekts anstelle von **Variant** -oder **IDispatch** -Typen zurückgeben \* .</span><span class="sxs-lookup"><span data-stu-id="d8f16-117">Methods that return instances of noncreatable classes should return the exact type of the object, rather than **VARIANT** or **IDispatch**\* types.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="d8f16-118">TYPEFLAG-Darstellung:</span><span class="sxs-lookup"><span data-stu-id="d8f16-118">Typeflag Representation:</span></span>

<span data-ttu-id="d8f16-119">Das Fehlen von TYPEFLAG " \_ f".</span><span class="sxs-lookup"><span data-stu-id="d8f16-119">The absence of TYPEFLAG\_FCANCREATE.</span></span>

## <a name="examples"></a><span data-ttu-id="d8f16-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8f16-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="d8f16-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d8f16-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f16-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="d8f16-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="d8f16-123">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="d8f16-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d8f16-124">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="d8f16-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d8f16-125">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="d8f16-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 