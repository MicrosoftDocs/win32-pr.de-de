---
description: Stellt einen Referenzpunkt für ein virtuelles System dar.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Msvm_VirtualSystemReferencePoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353256"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a><span data-ttu-id="2a1f1-103">MSVM \_ virtualsystemreferencepoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="2a1f1-103">Msvm\_VirtualSystemReferencePoint class</span></span>

<span data-ttu-id="2a1f1-104">Stellt einen Referenzpunkt für ein virtuelles System dar.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-104">Represents a reference point for a virtual system.</span></span>

<span data-ttu-id="2a1f1-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1f1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a1f1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="2a1f1-107">Member</span><span class="sxs-lookup"><span data-stu-id="2a1f1-107">Members</span></span>

<span data-ttu-id="2a1f1-108">Die **MSVM \_ virtualsystemreferencepoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2a1f1-108">The **Msvm\_VirtualSystemReferencePoint** class has these types of members:</span></span>

-   [<span data-ttu-id="2a1f1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a1f1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a1f1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a1f1-110">Properties</span></span>

<span data-ttu-id="2a1f1-111">Die **MSVM \_ virtualsystemreferencepoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-111">The **Msvm\_VirtualSystemReferencePoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a1f1-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a1f1-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a1f1-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a1f1-115">Die Konsistenz Ebene des Bezugspunkts.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-115">The consistency level of the reference point.</span></span>

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="2a1f1-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Anwendungs konsistent** (1)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2a1f1-117">Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Anwendungs konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-117">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="2a1f1-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Absturz konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a1f1-119">Der Bezugspunkt gibt einen Zeitpunkt an, an dem sich das virtuelle System in einem Absturz konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-119">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a1f1-120">**Hasassociateddata**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-120">**HasAssociatedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a1f1-121">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2a1f1-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a1f1-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a1f1-123">Auf **true** festgelegt, wenn der Verweis Punkt über zugeordnete Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-123">Set to **true** if the reference point has associated data.</span></span> <span data-ttu-id="2a1f1-124">Dies gilt nur für Protokoll basierte Referenzpunkte.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-124">This is valid only for log based reference points.</span></span> <span data-ttu-id="2a1f1-125">Bei RCT-basierten Bezugspunkten wird **hasassociateddata** auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-125">For RCT-based reference points, **HasAssociatedData** is set to **false**.</span></span> <span data-ttu-id="2a1f1-126">Bei Protokoll basierten Referenzpunkten wird **hasassociateddata** , sobald das Protokoll verworfen wird, **false**.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-126">For log based reference points, once the log is discarded **HasAssociatedData** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2a1f1-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a1f1-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a1f1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-130">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2a1f1-131">Eindeutige Identifikation eines Referenzpunkt Objekts.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-131">Unique identification of a reference point object.</span></span>

</dd> <dt>

<span data-ttu-id="2a1f1-132">**Referencepointtype**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-132">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a1f1-133">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a1f1-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a1f1-135">Gibt den Typ des Bezugspunkts an.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-135">Indicates the type of the reference point.</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="2a1f1-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Protokoll basiert** (1)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2a1f1-137">Protokoll Nachverfolgung für Hyper-V-Replikate.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-137">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="2a1f1-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basiert** (2)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a1f1-139">Basierend auf robusten Änderungsnachverfolgung von virtuellen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-139">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a1f1-140">**Resilientchangetrackingidentifier**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-140">**ResilientChangeTrackingIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a1f1-141">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2a1f1-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a1f1-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a1f1-143">Ein Array von RCT-IDs, die den virtuellen Datenträgern der VM zum Zeitpunkt der Erstellung dieses Bezugspunkts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-143">An array of RCT IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="2a1f1-144">Dieses Feld ist nur für RCT-basierte Referenzpunkte gültig.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-144">This field is valid only for RCT-based reference points.</span></span>

</dd> <dt>

<span data-ttu-id="2a1f1-145">**Virtualdiskidentifier**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-145">**VirtualDiskIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a1f1-146">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2a1f1-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a1f1-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a1f1-148">Ein Array von WMI-Instanz-IDs, die den virtuellen Datenträgern der VM zum Zeitpunkt der Erstellung dieses Bezugspunkts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-148">An array of WMI instance IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="2a1f1-149">Diesen virtuellen Datenträgern sind RCT-IDs zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-149">These virtual disks have RCT IDs associated with them.</span></span>

</dd> <dt>

<span data-ttu-id="2a1f1-150">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-150">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a1f1-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a1f1-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a1f1-153">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="2a1f1-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="2a1f1-154">Der Name des [**CIM- \_ Computer Systems**](cim-computersystem.md) , zu dem dieser Bezugspunkt gehört.</span><span class="sxs-lookup"><span data-stu-id="2a1f1-154">The name of the [**CIM\_ComputerSystem**](cim-computersystem.md) to which this reference point belongs</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a1f1-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a1f1-155">Requirements</span></span>



| <span data-ttu-id="2a1f1-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a1f1-156">Requirement</span></span> | <span data-ttu-id="2a1f1-157">Wert</span><span class="sxs-lookup"><span data-stu-id="2a1f1-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1f1-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-158">Minimum supported client</span></span><br/> | <span data-ttu-id="2a1f1-159">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a1f1-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2a1f1-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a1f1-160">Minimum supported server</span></span><br/> | <span data-ttu-id="2a1f1-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2a1f1-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2a1f1-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a1f1-162">Namespace</span></span><br/>                | <span data-ttu-id="2a1f1-163">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a1f1-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2a1f1-164">MOF</span><span class="sxs-lookup"><span data-stu-id="2a1f1-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a1f1-165"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a1f1-166">DLL</span><span class="sxs-lookup"><span data-stu-id="2a1f1-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a1f1-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a1f1-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a1f1-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a1f1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a1f1-169">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="2a1f1-169">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

