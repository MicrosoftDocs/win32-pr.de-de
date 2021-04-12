---
description: Bietet zusätzliche Informationen, die mit der Methode "kreatesnapshot" der MSVM- \_ Klasse "virtualsystemsnapshotservice" verwendet werden können.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Msvm_VirtualSystemSnapshotSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393418"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a><span data-ttu-id="115f4-103">MSVM \_ virtualsystemsnapshotsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="115f4-103">Msvm\_VirtualSystemSnapshotSettingData class</span></span>

<span data-ttu-id="115f4-104">Bietet zusätzliche Informationen, die mit der Methode " [**kreatesnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) " der [**MSVM-Klasse " \_ virtualsystemsnapshotservice**](msvm-virtualsystemsnapshotservice.md) " verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="115f4-104">Provides additional information to be used with the [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) method of the [**Msvm\_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) class.</span></span>

<span data-ttu-id="115f4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="115f4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="115f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="115f4-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a><span data-ttu-id="115f4-107">Member</span><span class="sxs-lookup"><span data-stu-id="115f4-107">Members</span></span>

<span data-ttu-id="115f4-108">Die **MSVM \_ virtualsystemsnapshotsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="115f4-108">The **Msvm\_VirtualSystemSnapshotSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="115f4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="115f4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="115f4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="115f4-110">Properties</span></span>

<span data-ttu-id="115f4-111">Die **MSVM \_ virtualsystemsnapshotsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="115f4-111">The **Msvm\_VirtualSystemSnapshotSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="115f4-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="115f4-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="115f4-113">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="115f4-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="115f4-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="115f4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="115f4-115">Die Konsistenz Ebene der Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="115f4-115">The consistency level of the snapshot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="115f4-116">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="115f4-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="115f4-117">**Anwendungs konsistent** (1)</span><span class="sxs-lookup"><span data-stu-id="115f4-117">**Application Consistent** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="115f4-118">**Absturz konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="115f4-118">**Crash Consistent** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="115f4-119">**Guestbackuptype**</span><span class="sxs-lookup"><span data-stu-id="115f4-119">**GuestBackupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="115f4-120">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="115f4-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="115f4-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="115f4-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="115f4-122">Der im Gast zu verwendende Sicherungstyp.</span><span class="sxs-lookup"><span data-stu-id="115f4-122">Backup type to be used inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="115f4-123">In Windows 10, Version 1703, hinzugefügte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="115f4-123">Property added in Windows 10, version 1703</span></span>

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="115f4-124">**Nicht definiert** (0)</span><span class="sxs-lookup"><span data-stu-id="115f4-124">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="115f4-125">**Vollständig** (1)</span><span class="sxs-lookup"><span data-stu-id="115f4-125">**Full** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="115f4-126">**Kopieren** (2)</span><span class="sxs-lookup"><span data-stu-id="115f4-126">**Copy** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="115f4-127">**Ignoronsnapshottabledisks**</span><span class="sxs-lookup"><span data-stu-id="115f4-127">**IgnoreNonSnapshottableDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="115f4-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="115f4-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="115f4-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="115f4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="115f4-130">Gibt an, ob nicht snapsho\datenträger wie Pass-Through-Datenträger und Fibre Channel-Datenträger beim Erstellen der Momentaufnahme ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="115f4-130">Specifies if non-snapshottable disks like passthrough disks and Fibre Channel Disks are to be ignored while creating the snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="115f4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="115f4-131">Requirements</span></span>



| <span data-ttu-id="115f4-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="115f4-132">Requirement</span></span> | <span data-ttu-id="115f4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="115f4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="115f4-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="115f4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="115f4-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="115f4-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="115f4-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="115f4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="115f4-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="115f4-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="115f4-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="115f4-138">Namespace</span></span><br/>                | <span data-ttu-id="115f4-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="115f4-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="115f4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="115f4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="115f4-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="115f4-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="115f4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="115f4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="115f4-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="115f4-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="115f4-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="115f4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="115f4-145">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="115f4-145">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




