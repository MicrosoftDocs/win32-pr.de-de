---
description: Ein "taubempropertyset"-Objekt ist eine Sammlung von "Swap Property"-Objekten.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Taubempropertyset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351096"
---
# <a name="swbempropertyset-object"></a><span data-ttu-id="917be-103">Swap-PropertySet-Objekt</span><span class="sxs-lookup"><span data-stu-id="917be-103">SWbemPropertySet object</span></span>

<span data-ttu-id="917be-104">Ein " **taubempropertyset** "-Objekt ist eine Sammlung von " [**Swap Property**](swbemproperty.md) "-Objekten.</span><span class="sxs-lookup"><span data-stu-id="917be-104">An **SWbemPropertySet** object is a collection of [**SWbemProperty**](swbemproperty.md) objects.</span></span> <span data-ttu-id="917be-105">Sie können der Auflistung Elemente mithilfe der [**Add**](swbempropertyset-add.md) -Methode hinzufügen, Elemente aus der Auflistung mithilfe der- [**Element**](swbempropertyset-item.md) Methode abrufen und mithilfe der [**Remove**](swbempropertyset-remove.md) -Methode Elemente aus der Auflistung entfernen.</span><span class="sxs-lookup"><span data-stu-id="917be-105">You can add items to the collection using the [**Add**](swbempropertyset-add.md) method, retrieve items from the collection using the [**Item**](swbempropertyset-item.md) method, and remove items from the collection using the [**Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="917be-106">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="917be-106">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="917be-107">Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="917be-107">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="917be-108">Die " [**Swap Property**](swbemproperty.md) "-Objekte, aus denen eine " **Swap PropertySet** "-Auflistung besteht, werden verwendet, um die Eigenschaften einer einzelnen WMI-Klasse oder-Instanz zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="917be-108">The [**SWbemProperty**](swbemproperty.md) objects that make up an **SWbemPropertySet** collection are used to describe the properties of a single WMI class or instance.</span></span>

## <a name="members"></a><span data-ttu-id="917be-109">Member</span><span class="sxs-lookup"><span data-stu-id="917be-109">Members</span></span>

<span data-ttu-id="917be-110">Das Objekt " **Swap PropertySet** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="917be-110">The **SWbemPropertySet** object has these types of members:</span></span>

-   [<span data-ttu-id="917be-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="917be-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="917be-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="917be-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="917be-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="917be-113">Methods</span></span>

<span data-ttu-id="917be-114">Das Objekt " **Swap PropertySet** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="917be-114">The **SWbemPropertySet** object has these methods.</span></span>



| <span data-ttu-id="917be-115">Methode</span><span class="sxs-lookup"><span data-stu-id="917be-115">Method</span></span>                                    | <span data-ttu-id="917be-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="917be-116">Description</span></span>                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="917be-117">**Eren**</span><span class="sxs-lookup"><span data-stu-id="917be-117">**Add**</span></span>](swbempropertyset-add.md)       | <span data-ttu-id="917be-118">Fügt der Auflistung von " **gobempropertyset** " ein " [**gotenproperty**](swbemproperty.md) "-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="917be-118">Adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span><br/>                        |
| [<span data-ttu-id="917be-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="917be-119">**Item**</span></span>](swbempropertyset-item.md)     | <span data-ttu-id="917be-120">Ruft eine benannte " [**taubemproperty**](swbemproperty.md) " aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="917be-120">Gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="917be-121">Dies ist die Standardmethode für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="917be-121">This is the default method for this object.</span></span><br/> |
| [<span data-ttu-id="917be-122">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="917be-122">**Remove**</span></span>](swbempropertyset-remove.md) | <span data-ttu-id="917be-123">Löscht ein [**-**](swbemproperty.md) Objekt aus der-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="917be-123">Deletes an [**SWbemProperty**](swbemproperty.md) object from the collection.</span></span><br/>                                        |



 

### <a name="properties"></a><span data-ttu-id="917be-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="917be-124">Properties</span></span>

<span data-ttu-id="917be-125">Das Objekt " **Swap PropertySet** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="917be-125">The **SWbemPropertySet** object has these properties.</span></span>



| <span data-ttu-id="917be-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="917be-126">Property</span></span>                                           | <span data-ttu-id="917be-127">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="917be-127">Access type</span></span>          | <span data-ttu-id="917be-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="917be-128">Description</span></span>                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="917be-129">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="917be-129">**Count**</span></span>](swbempropertyset-count.md)<br/> | <span data-ttu-id="917be-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="917be-130">Read-only</span></span><br/> | <span data-ttu-id="917be-131">Die Anzahl der Elemente in der **Swap** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="917be-131">The number of items in the **SWbemPropertySet** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="917be-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="917be-132">Examples</span></span>

<span data-ttu-id="917be-133">Das folgende VBScript-Beispiel veranschaulicht, wie " [**taubempropertyset. Remove**](swbempropertyset-remove.md) " **wbemErrResetToDefault** zurückgeben kann, wenn die Eigenschaft überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="917be-133">The following VBScript sample demonstrates how [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) can return **wbemErrResetToDefault** if the property is overridden.</span></span>


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a><span data-ttu-id="917be-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="917be-134">Requirements</span></span>



| <span data-ttu-id="917be-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="917be-135">Requirement</span></span> | <span data-ttu-id="917be-136">Wert</span><span class="sxs-lookup"><span data-stu-id="917be-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="917be-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="917be-137">Minimum supported client</span></span><br/> | <span data-ttu-id="917be-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="917be-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="917be-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="917be-139">Minimum supported server</span></span><br/> | <span data-ttu-id="917be-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="917be-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="917be-141">Header</span><span class="sxs-lookup"><span data-stu-id="917be-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="917be-142"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="917be-142"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="917be-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="917be-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="917be-144"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="917be-144"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="917be-145">DLL</span><span class="sxs-lookup"><span data-stu-id="917be-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="917be-146"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="917be-146"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="917be-147">CLSID</span><span class="sxs-lookup"><span data-stu-id="917be-147">CLSID</span></span><br/>                    | <span data-ttu-id="917be-148">CLSID- \_ Swap-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="917be-148">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="917be-149">IID</span><span class="sxs-lookup"><span data-stu-id="917be-149">IID</span></span><br/>                      | <span data-ttu-id="917be-150">IID \_ iswbempropertyset</span><span class="sxs-lookup"><span data-stu-id="917be-150">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="917be-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="917be-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917be-152">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="917be-152">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




