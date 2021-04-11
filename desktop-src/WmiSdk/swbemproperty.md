---
description: Das taubemproperty-Objekt stellt eine einzelne WMI-Eigenschaft eines verwalteten Objekts dar. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Taubemproperty-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218482"
---
# <a name="swbemproperty-object"></a><span data-ttu-id="a1b4f-104">Swap Property-Objekt</span><span class="sxs-lookup"><span data-stu-id="a1b4f-104">SWbemProperty object</span></span>

<span data-ttu-id="a1b4f-105">Das **taubemproperty** -Objekt stellt eine einzelne WMI-Eigenschaft eines verwalteten Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-105">The **SWbemProperty** object represents a single WMI property of a managed object.</span></span> <span data-ttu-id="a1b4f-106">Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="a1b4f-107">Member</span><span class="sxs-lookup"><span data-stu-id="a1b4f-107">Members</span></span>

<span data-ttu-id="a1b4f-108">Das Objekt " **Swap Property** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a1b4f-108">The **SWbemProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="a1b4f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1b4f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1b4f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1b4f-110">Properties</span></span>

<span data-ttu-id="a1b4f-111">Das **taubemproperty** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-111">The **SWbemProperty** object has these properties.</span></span>



| <span data-ttu-id="a1b4f-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a1b4f-112">Property</span></span>                                                     | <span data-ttu-id="a1b4f-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a1b4f-113">Access type</span></span>           | <span data-ttu-id="a1b4f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1b4f-114">Description</span></span>                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1b4f-115">**CimType**</span><span class="sxs-lookup"><span data-stu-id="a1b4f-115">**CIMType**</span></span>](swbemproperty-cimtype.md)<br/>          | <span data-ttu-id="a1b4f-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1b4f-116">Read-only</span></span><br/>  | <span data-ttu-id="a1b4f-117">Der Typ dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-117">Type of this property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="a1b4f-118">**IsArray**</span><span class="sxs-lookup"><span data-stu-id="a1b4f-118">**IsArray**</span></span>](swbemproperty-isarray.md)<br/>          | <span data-ttu-id="a1b4f-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1b4f-119">Read-only</span></span><br/>  | <span data-ttu-id="a1b4f-120">Boolescher Wert, der angibt, ob diese Eigenschaft einen Arraytyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-120">Boolean value that indicates if this property has an array type.</span></span><br/>                                                   |
| [<span data-ttu-id="a1b4f-121">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="a1b4f-121">**IsLocal**</span></span>](swbemproperty-islocal.md)<br/>          | <span data-ttu-id="a1b4f-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1b4f-122">Read-only</span></span><br/>  | <span data-ttu-id="a1b4f-123">Boolescher Wert, der angibt, ob diese Eigenschaft lokal ist.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-123">Boolean value that indicates if this property is local.</span></span><br/>                                                            |
| [<span data-ttu-id="a1b4f-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="a1b4f-124">**Name**</span></span>](swbemproperty-name.md)<br/>                | <span data-ttu-id="a1b4f-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1b4f-125">Read-only</span></span><br/>  | <span data-ttu-id="a1b4f-126">Der Name dieser WMI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-126">Name of this WMI property.</span></span><br/>                                                                                         |
| [<span data-ttu-id="a1b4f-127">**Entstehungs**</span><span class="sxs-lookup"><span data-stu-id="a1b4f-127">**Origin**</span></span>](swbemproperty-origin.md)<br/>            | <span data-ttu-id="a1b4f-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1b4f-128">Read-only</span></span><br/>  | <span data-ttu-id="a1b4f-129">Enthält die Ursprungs Klasse dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-129">Contains the originating class of this property.</span></span><br/>                                                                   |
| [<span data-ttu-id="a1b4f-130">**Qualifikation\_**</span><span class="sxs-lookup"><span data-stu-id="a1b4f-130">**Qualifiers\_**</span></span>](swbemproperty-qualifiers-.md)<br/> | <span data-ttu-id="a1b4f-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a1b4f-131">Read-only</span></span><br/>  | <span data-ttu-id="a1b4f-132">Ein " [**taubemqualifierset**](swbemqualifierset.md) "-Objekt, das die Auflistung der Qualifizierer für diese Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-132">An [**SWbemQualifierSet**](swbemqualifierset.md) object, which is the collection of qualifiers for this property.</span></span><br/> |
| [<span data-ttu-id="a1b4f-133">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a1b4f-133">**Value**</span></span>](swbemproperty-value.md)<br/>              | <span data-ttu-id="a1b4f-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a1b4f-134">Read/write</span></span><br/> | <span data-ttu-id="a1b4f-135">Tatsächlicher Wert dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-135">Actual value of this property.</span></span> <span data-ttu-id="a1b4f-136">Dies ist die standardmäßige Automatisierungs Eigenschaft dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1b4f-136">This is the default automation property of this object.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="a1b4f-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1b4f-137">Requirements</span></span>



| <span data-ttu-id="a1b4f-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1b4f-138">Requirement</span></span> | <span data-ttu-id="a1b4f-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a1b4f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b4f-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1b4f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b4f-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1b4f-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1b4f-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1b4f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b4f-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1b4f-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1b4f-144">Header</span><span class="sxs-lookup"><span data-stu-id="a1b4f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b4f-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b4f-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1b4f-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a1b4f-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1b4f-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1b4f-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1b4f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a1b4f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1b4f-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1b4f-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1b4f-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="a1b4f-150">CLSID</span></span><br/>                    | <span data-ttu-id="a1b4f-151">CLSID- \_ Swap-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a1b4f-151">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="a1b4f-152">IID</span><span class="sxs-lookup"><span data-stu-id="a1b4f-152">IID</span></span><br/>                      | <span data-ttu-id="a1b4f-153">IID \_ iswbemproperty</span><span class="sxs-lookup"><span data-stu-id="a1b4f-153">IID\_ISWbemProperty</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a1b4f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1b4f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b4f-155">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="a1b4f-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




