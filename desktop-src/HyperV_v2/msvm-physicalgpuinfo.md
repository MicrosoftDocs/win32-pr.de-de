---
description: Enthält Informationen zu einer physischen remotefx-Grafikverarbeitungseinheit (GPU).
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Msvm_PhysicalGPUInfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353957"
---
# <a name="msvm_physicalgpuinfo-class"></a><span data-ttu-id="e5d58-103">MSVM \_ physicalgpuinfo-Klasse</span><span class="sxs-lookup"><span data-stu-id="e5d58-103">Msvm\_PhysicalGPUInfo class</span></span>

<span data-ttu-id="e5d58-104">Enthält Informationen zu einer physischen remotefx-Grafikverarbeitungseinheit (GPU).</span><span class="sxs-lookup"><span data-stu-id="e5d58-104">Contains information about a RemoteFX physical graphics processing unit (GPU).</span></span>

<span data-ttu-id="e5d58-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e5d58-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d58-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5d58-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a><span data-ttu-id="e5d58-107">Member</span><span class="sxs-lookup"><span data-stu-id="e5d58-107">Members</span></span>

<span data-ttu-id="e5d58-108">Die **MSVM \_ physicalgpuinfo** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e5d58-108">The **Msvm\_PhysicalGPUInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="e5d58-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5d58-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5d58-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5d58-110">Properties</span></span>

<span data-ttu-id="e5d58-111">Die **MSVM \_ physicalgpuinfo** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e5d58-111">The **Msvm\_PhysicalGPUInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5d58-112">**Availablevideomemory**</span><span class="sxs-lookup"><span data-stu-id="e5d58-112">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-113">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5d58-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-115">Die Menge des nicht verwendeten Grafik Speichers in Bytes auf der physischen GPU, die von remotefx verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5d58-115">The amount of unused video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="e5d58-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e5d58-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e5d58-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-119">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e5d58-119">A short description of the object.</span></span> <span data-ttu-id="e5d58-120">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e5d58-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5d58-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5d58-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e5d58-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-124">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e5d58-124">A description of the object.</span></span> <span data-ttu-id="e5d58-125">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e5d58-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5d58-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e5d58-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e5d58-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-129">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e5d58-129">A display name for the object.</span></span> <span data-ttu-id="e5d58-130">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e5d58-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5d58-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="e5d58-131">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e5d58-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-134">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="e5d58-134">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-135">Der eindeutige Bezeichner der physischen GPU.</span><span class="sxs-lookup"><span data-stu-id="e5d58-135">The unique identifier of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="e5d58-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e5d58-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e5d58-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-139">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e5d58-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-140">Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e5d58-140">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e5d58-141">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e5d58-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5d58-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5d58-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e5d58-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-145">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="e5d58-145">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-146">Der Anzeige Name der physischen GPU.</span><span class="sxs-lookup"><span data-stu-id="e5d58-146">The display name of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="e5d58-147">**Totalvideomemory**</span><span class="sxs-lookup"><span data-stu-id="e5d58-147">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5d58-148">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5d58-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5d58-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e5d58-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5d58-150">Die Gesamtmenge des Video Speichers in Bytes auf der physischen GPU, die von remotefx verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5d58-150">The total amount of video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5d58-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5d58-151">Requirements</span></span>



| <span data-ttu-id="e5d58-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5d58-152">Requirement</span></span> | <span data-ttu-id="e5d58-153">Wert</span><span class="sxs-lookup"><span data-stu-id="e5d58-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d58-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5d58-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d58-155">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5d58-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e5d58-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5d58-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d58-157">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5d58-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5d58-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5d58-158">Namespace</span></span><br/>                | <span data-ttu-id="e5d58-159">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e5d58-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e5d58-160">MOF</span><span class="sxs-lookup"><span data-stu-id="e5d58-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5d58-161"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e5d58-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5d58-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e5d58-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5d58-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5d58-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5d58-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5d58-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d58-165">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="e5d58-165">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

