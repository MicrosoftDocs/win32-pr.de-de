---
description: Ein "taubemqualifierset"-Objekt ist eine Sammlung von "taubemqualifier"-Objekten.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Taubemqualifierset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050510"
---
# <a name="swbemqualifierset-object"></a><span data-ttu-id="1552b-103">Taubemqualifierset-Objekt</span><span class="sxs-lookup"><span data-stu-id="1552b-103">SWbemQualifierSet object</span></span>

<span data-ttu-id="1552b-104">Ein " **taubemqualifierset** "-Objekt ist eine Sammlung von " [**taubemqualifier**](swbemqualifier.md) "-Objekten.</span><span class="sxs-lookup"><span data-stu-id="1552b-104">An **SWbemQualifierSet** object is a collection of [**SWbemQualifier**](swbemqualifier.md) objects.</span></span> <span data-ttu-id="1552b-105">Der Auflistung werden Elemente mithilfe der [**Add**](swbemqualifierset-add.md) -Methode hinzugefügt, die mithilfe der- [**Element**](swbemqualifierset-item.md) Methode aus der Auflistung abgerufen und mithilfe der [**Remove**](swbemqualifierset-remove.md) -Methode aus der Auflistung entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1552b-105">Items are added to the collection using the [**Add**](swbemqualifierset-add.md) method, retrieved from the collection using the [**Item**](swbemqualifierset-item.md) method, and removed from the collection using the [**Remove**](swbemqualifierset-remove.md) method.</span></span> <span data-ttu-id="1552b-106">Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1552b-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="1552b-107">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1552b-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="1552b-108">Die [**austaubemqualifier**](swbemqualifier.md) -Objekte, aus denen sich eine **Swap** -Auflistung besteht, beschreiben die Qualifizierer, die an eine WMI-Klasse, eine Instanz, eine Methode oder einen Methoden Parameter angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="1552b-108">The [**SWbemQualifier**](swbemqualifier.md) objects that make up an **SWbemQualifierSet** collection describe the qualifiers attached to a WMI class, instance, method, or method parameter.</span></span>

## <a name="members"></a><span data-ttu-id="1552b-109">Member</span><span class="sxs-lookup"><span data-stu-id="1552b-109">Members</span></span>

<span data-ttu-id="1552b-110">Das Objekt " **taubemqualifierset** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1552b-110">The **SWbemQualifierSet** object has these types of members:</span></span>

-   [<span data-ttu-id="1552b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1552b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1552b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1552b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1552b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="1552b-113">Methods</span></span>

<span data-ttu-id="1552b-114">Das **taubemqualifierset** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1552b-114">The **SWbemQualifierSet** object has these methods.</span></span>



| <span data-ttu-id="1552b-115">Methode</span><span class="sxs-lookup"><span data-stu-id="1552b-115">Method</span></span>                                     | <span data-ttu-id="1552b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1552b-116">Description</span></span>                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1552b-117">**Eren**</span><span class="sxs-lookup"><span data-stu-id="1552b-117">**Add**</span></span>](swbemqualifierset-add.md)       | <span data-ttu-id="1552b-118">Fügt der Auflistung von " **taubemqualifierset** " ein " [**taubemqualifier**](swbemqualifier.md) "-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="1552b-118">Adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span><br/> |
| [<span data-ttu-id="1552b-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="1552b-119">**Item**</span></span>](swbemqualifierset-item.md)     | <span data-ttu-id="1552b-120">Gibt [**ein benanntes**](swbemqualifier.md) -Objekt aus der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="1552b-120">Returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span><br/>             |
| [<span data-ttu-id="1552b-121">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="1552b-121">**Remove**</span></span>](swbemqualifierset-remove.md) | <span data-ttu-id="1552b-122">Löscht einen benannten Qualifizierer aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1552b-122">Deletes a named qualifier from the collection.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="1552b-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1552b-123">Properties</span></span>

<span data-ttu-id="1552b-124">Das **taubemqualifierset** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1552b-124">The **SWbemQualifierSet** object has these properties.</span></span>



| <span data-ttu-id="1552b-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1552b-125">Property</span></span>                                            | <span data-ttu-id="1552b-126">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1552b-126">Access type</span></span>          | <span data-ttu-id="1552b-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1552b-127">Description</span></span>                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="1552b-128">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="1552b-128">**Count**</span></span>](swbemqualifierset-count.md)<br/> | <span data-ttu-id="1552b-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1552b-129">Read-only</span></span><br/> | <span data-ttu-id="1552b-130">Enthält die Anzahl der Elemente in einer Auflistung von " **taubemqualifierset** ".</span><span class="sxs-lookup"><span data-stu-id="1552b-130">Contains the number of items in an **SWbemQualifierSet** collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1552b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1552b-131">Requirements</span></span>



| <span data-ttu-id="1552b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1552b-132">Requirement</span></span> | <span data-ttu-id="1552b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1552b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1552b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1552b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1552b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1552b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1552b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1552b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1552b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1552b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1552b-138">Header</span><span class="sxs-lookup"><span data-stu-id="1552b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1552b-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1552b-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1552b-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1552b-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="1552b-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1552b-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1552b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1552b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1552b-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1552b-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1552b-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="1552b-144">CLSID</span></span><br/>                    | <span data-ttu-id="1552b-145">CLSID- \_ Swap-Gruppe</span><span class="sxs-lookup"><span data-stu-id="1552b-145">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="1552b-146">IID</span><span class="sxs-lookup"><span data-stu-id="1552b-146">IID</span></span><br/>                      | <span data-ttu-id="1552b-147">IID \_ iswbemqualifierset</span><span class="sxs-lookup"><span data-stu-id="1552b-147">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="1552b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1552b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1552b-149">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="1552b-149">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




