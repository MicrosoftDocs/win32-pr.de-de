---
description: Sie können die Eigenschaften des "taubemqualifier"-Objekts verwenden, um einen einzelnen Qualifizierer für eine WMI-Klasse, eine Instanz, eine Eigenschaft oder einen Methoden Parameter darzustellen. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Taubemqualifiziererobjekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215312"
---
# <a name="swbemqualifier-object"></a><span data-ttu-id="fde20-104">Taubemqualifiziererobjekt</span><span class="sxs-lookup"><span data-stu-id="fde20-104">SWbemQualifier object</span></span>

<span data-ttu-id="fde20-105">Sie können die Eigenschaften des " **taubemqualifier** "-Objekts verwenden, um einen einzelnen Qualifizierer für eine WMI-Klasse, eine Instanz, eine Eigenschaft oder einen Methoden Parameter darzustellen.</span><span class="sxs-lookup"><span data-stu-id="fde20-105">You can use the properties of the **SWbemQualifier** object to represent a single qualifier of a WMI class, instance, property, or method parameter.</span></span> <span data-ttu-id="fde20-106">Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fde20-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="fde20-107">Member</span><span class="sxs-lookup"><span data-stu-id="fde20-107">Members</span></span>

<span data-ttu-id="fde20-108">Das Objekt " **Swap-Qualifizierer** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fde20-108">The **SWbemQualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="fde20-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fde20-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fde20-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fde20-110">Properties</span></span>

<span data-ttu-id="fde20-111">Das **taubemqualifier** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fde20-111">The **SWbemQualifier** object has these properties.</span></span>



| <span data-ttu-id="fde20-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fde20-112">Property</span></span>                                                                       | <span data-ttu-id="fde20-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="fde20-113">Access type</span></span>           | <span data-ttu-id="fde20-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fde20-114">Description</span></span>                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fde20-115">**Isänderte**</span><span class="sxs-lookup"><span data-stu-id="fde20-115">**IsAmended**</span></span>](swbemqualifier-isamended.md)<br/>                       | <span data-ttu-id="fde20-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fde20-116">Read-only</span></span><br/>  | <span data-ttu-id="fde20-117">Boolescher Wert, der angibt, ob dieser Qualifizierer mit einem Zusammenarbeits Vorgang lokalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fde20-117">Boolean value that indicates if this qualifier has been localized using a merge operation.</span></span><br/> |
| [<span data-ttu-id="fde20-118">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="fde20-118">**IsLocal**</span></span>](swbemqualifier-islocal.md)<br/>                           | <span data-ttu-id="fde20-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fde20-119">Read-only</span></span><br/>  | <span data-ttu-id="fde20-120">Boolescher Wert, der angibt, ob dieser Qualifizierer lokal ist.</span><span class="sxs-lookup"><span data-stu-id="fde20-120">Boolean value that indicates if this qualifier is local.</span></span><br/>                                   |
| [<span data-ttu-id="fde20-121">**Isoverridable**</span><span class="sxs-lookup"><span data-stu-id="fde20-121">**IsOverridable**</span></span>](swbemqualifier-isoverridable.md)<br/>               | <span data-ttu-id="fde20-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fde20-122">Read/write</span></span><br/> | <span data-ttu-id="fde20-123">Boolescher Wert, der angibt, ob dieser Qualifizierer bei der Weitergabe überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fde20-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span><br/>          |
| [<span data-ttu-id="fde20-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="fde20-124">**Name**</span></span>](swbemqualifier-name.md)<br/>                                 | <span data-ttu-id="fde20-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fde20-125">Read-only</span></span><br/>  | <span data-ttu-id="fde20-126">Der Name dieses Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="fde20-126">Name of this qualifier.</span></span><br/>                                                                    |
| [<span data-ttu-id="fde20-127">**Propagatestoinstance**</span><span class="sxs-lookup"><span data-stu-id="fde20-127">**PropagatesToInstance**</span></span>](swbemqualifier-propagatestoinstance.md)<br/> | <span data-ttu-id="fde20-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fde20-128">Read/write</span></span><br/> | <span data-ttu-id="fde20-129">Boolescher Wert, der angibt, ob dieser Qualifizierer an eine-Instanz weitergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fde20-129">Boolean value that indicates if this qualifier can be propagated to an instance.</span></span><br/>           |
| [<span data-ttu-id="fde20-130">**Propagatestosubclass**</span><span class="sxs-lookup"><span data-stu-id="fde20-130">**PropagatesToSubClass**</span></span>](swbemqualifier-propagatestosubclass.md)<br/> | <span data-ttu-id="fde20-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fde20-131">Read-only</span></span><br/>  | <span data-ttu-id="fde20-132">Boolescher Wert, der angibt, ob dieser Qualifizierer an eine Unterklasse weitergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fde20-132">Boolean value that indicates if this qualifier can be propagated to a subclass.</span></span><br/>            |
| [<span data-ttu-id="fde20-133">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fde20-133">**Value**</span></span>](swbemqualifier-value.md)<br/>                               | <span data-ttu-id="fde20-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fde20-134">Read/write</span></span><br/> | <span data-ttu-id="fde20-135">Der Variant-Wert dieses Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="fde20-135">Variant value of this qualifier.</span></span> <span data-ttu-id="fde20-136">Dies ist die Standard Eigenschaft dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="fde20-136">This is the default property of this object.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="fde20-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fde20-137">Requirements</span></span>



| <span data-ttu-id="fde20-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fde20-138">Requirement</span></span> | <span data-ttu-id="fde20-139">Wert</span><span class="sxs-lookup"><span data-stu-id="fde20-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fde20-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fde20-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fde20-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fde20-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fde20-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fde20-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fde20-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fde20-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fde20-144">Header</span><span class="sxs-lookup"><span data-stu-id="fde20-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde20-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde20-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fde20-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fde20-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="fde20-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fde20-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fde20-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fde20-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fde20-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde20-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fde20-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="fde20-150">CLSID</span></span><br/>                    | <span data-ttu-id="fde20-151">CLSID- \_ Austausch Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="fde20-151">CLSID\_SWbemQualifier</span></span><br/>                                                        |
| <span data-ttu-id="fde20-152">IID</span><span class="sxs-lookup"><span data-stu-id="fde20-152">IID</span></span><br/>                      | <span data-ttu-id="fde20-153">IID \_ iswbemqualifizierer</span><span class="sxs-lookup"><span data-stu-id="fde20-153">IID\_ISWbemQualifier</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="fde20-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fde20-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde20-155">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="fde20-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




