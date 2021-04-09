---
title: nonbrowsable-Attribut
description: Verwenden Sie das \ NonBrowsable \-Attribut, um eine Schnittstelle oder einen dispinterface-Member zu kennzeichnen, der nicht in einem Eigenschaften Browser angezeigt werden soll.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- nicht durchsuchbares Attribut, Mittel l
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948639"
---
# <a name="nonbrowsable-attribute"></a><span data-ttu-id="eec46-104">nonbrowsable-Attribut</span><span class="sxs-lookup"><span data-stu-id="eec46-104">nonbrowsable attribute</span></span>

<span data-ttu-id="eec46-105">Verwenden Sie das nicht **\[ \] browsefähige** Attribut, um eine Schnittstelle oder einen dispinterface-Member zu kennzeichnen, der nicht in einem Eigenschaften Browser angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eec46-105">Use the **\[nonbrowsable\]** attribute to tag an interface or dispinterface member that should not be displayed in a properties browser.</span></span>

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="eec46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eec46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec46-107">*Property-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="eec46-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="eec46-108">Andere Attribute, die auf die-Eigenschaft angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="eec46-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="eec46-109">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="eec46-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="eec46-110">Der Typ der Daten, die von der-Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eec46-110">The type of the data returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="eec46-111">*Eigenschaftsname*</span><span class="sxs-lookup"><span data-stu-id="eec46-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="eec46-112">Der Name der Eigenschaft oder Methode.</span><span class="sxs-lookup"><span data-stu-id="eec46-112">The name of the property or method.</span></span>

</dd> <dt>

<span data-ttu-id="eec46-113">*Prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="eec46-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="eec46-114">NULL oder mehr Parameter, die an die Methode weitergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eec46-114">Zero or more parameters to be passed to the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eec46-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eec46-115">Remarks</span></span>

<span data-ttu-id="eec46-116">Bestimmte Eigenschaften sollten nicht in einem Eigenschaften Browser angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="eec46-116">Certain properties should not be displayed in a properties browser.</span></span> <span data-ttu-id="eec46-117">Dies liegt möglicherweise daran, dass das Abrufen des Werts sehr viel Zeit in Anspruch nehmen würde.</span><span class="sxs-lookup"><span data-stu-id="eec46-117">This may be because retrieving the value would take a very long time.</span></span> <span data-ttu-id="eec46-118">Im Beispiel wird verhindert, dass der Benutzer versucht, die *count* -Eigenschaft abzurufen, die die Anzahl der Zeilen im Dynaset zurückgibt. Diese Zahl kann die Ergebnisse einer sehr großen Abfrage darstellen.</span><span class="sxs-lookup"><span data-stu-id="eec46-118">The example prevents the user from attempting to retrieve the *Count* property, which returns the number of rows in the dynaset.This number may represent the results of a very large query.</span></span>

<span data-ttu-id="eec46-119">Andere Eigenschaften können unerwartete Auswirkungen auf den Browser haben.</span><span class="sxs-lookup"><span data-stu-id="eec46-119">Other properties may have unexpected effects on the browser.</span></span> <span data-ttu-id="eec46-120">Stellen Sie sich z. b. ein Steuerelement mit der Eigenschaft "issselected" vor, um zu bestimmen, ob das Steuerelement ausgewählt ist</span><span class="sxs-lookup"><span data-stu-id="eec46-120">For example, consider a control with the property "IsSelected" to tell whether the control is selected.</span></span> <span data-ttu-id="eec46-121">Wenn "issgewählt" auf "false" festgelegt ist, durchsucht ein Auswahl basierter Eigenschaften Browser ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="eec46-121">If "IsSelected" is set to false, a selection-based properties browser will browse a different object.</span></span>

<span data-ttu-id="eec46-122">Beachten Sie, dass eine Eigenschaft, die als **\[ nicht \]** suchbar markiert ist, immer noch in einem Objektkatalog angezeigt wird, in dem keine Eigenschaftswerte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="eec46-122">Note that a property tagged as **\[nonbrowsable\]** will still appear in an object browser, which does not show property values.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="eec46-123">TYPEFLAG-Darstellung</span><span class="sxs-lookup"><span data-stu-id="eec46-123">Typeflag Representation</span></span>

<span data-ttu-id="eec46-124">Das vorhanden sein von funkflag, das \_ nicht browsetierbar ist, oder das varflag-Element \_ .</span><span class="sxs-lookup"><span data-stu-id="eec46-124">The presence of FUNCFLAG\_FNONBROWSABLE or VARFLAG\_FNONBROWSABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="eec46-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eec46-125">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a><span data-ttu-id="eec46-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eec46-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec46-127">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="eec46-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="eec46-128">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="eec46-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="eec46-129">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="eec46-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 