---
description: Exportieren von Einstellungsdaten, die an die exportsnapshot-Methode der MSVM \_ collectionsnapshotservice-Klasse übermittelt werden sollen.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344432"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a><span data-ttu-id="880ed-103">MSVM \_ collectionsnapshotexportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="880ed-103">Msvm\_CollectionSnapshotExportSettingData class</span></span>

<span data-ttu-id="880ed-104">Exportieren von Einstellungsdaten, die an die exportsnapshot-Methode der [**MSVM \_ collectionsnapshotservice**](msvm-collectionsnapshotservice.md) -Klasse übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="880ed-104">Export setting data to be passed in to the ExportSnapshot method of [**Msvm\_CollectionSnapshotService**](msvm-collectionsnapshotservice.md) class.</span></span>

<span data-ttu-id="880ed-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="880ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="880ed-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="880ed-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a><span data-ttu-id="880ed-107">Member</span><span class="sxs-lookup"><span data-stu-id="880ed-107">Members</span></span>

<span data-ttu-id="880ed-108">Die **MSVM \_ collectionsnapshotexportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="880ed-108">The **Msvm\_CollectionSnapshotExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="880ed-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="880ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="880ed-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="880ed-110">Properties</span></span>

<span data-ttu-id="880ed-111">Die **MSVM \_ collectionsnapshotexportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="880ed-111">The **Msvm\_CollectionSnapshotExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="880ed-112">**Backupintent**</span><span class="sxs-lookup"><span data-stu-id="880ed-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880ed-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="880ed-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="880ed-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="880ed-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="880ed-115">Gibt die Absicht an, wie die exportierten Sicherungs Sätze verwendet werden sollen:</span><span class="sxs-lookup"><span data-stu-id="880ed-115">Indicates the intent how the exported backup sets would be used:</span></span>

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="880ed-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Backupintentpreservechain** (1)</span><span class="sxs-lookup"><span data-stu-id="880ed-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span></span>


</dt> <dd>

<span data-ttu-id="880ed-117">Alle exportierten vollständigen und differenziellen Sicherungs Sätze werden unverändert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="880ed-117">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="880ed-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Backupintentmerge** (2)</span><span class="sxs-lookup"><span data-stu-id="880ed-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span></span>


</dt> <dd>

<span data-ttu-id="880ed-119">Die exportierten vollständigen und differenziellen Sicherungs Sätze werden zusammengeführt, um vollständige Sicherungs Sätze zu synthetisieren.</span><span class="sxs-lookup"><span data-stu-id="880ed-119">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="880ed-120">**Copyvmstorage**</span><span class="sxs-lookup"><span data-stu-id="880ed-120">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880ed-121">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="880ed-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="880ed-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="880ed-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="880ed-123">Wenn der Wert **true** ist, wird der VM-Speicher beim Exportieren des virtuellen Computers kopiert.</span><span class="sxs-lookup"><span data-stu-id="880ed-123">if **true**, the VM storage will be copied when the VM is exported.</span></span> <span data-ttu-id="880ed-124">Andernfalls **false.**</span><span class="sxs-lookup"><span data-stu-id="880ed-124">Otherwise, **false.**</span></span>

</dd> <dt>

<span data-ttu-id="880ed-125">**Differenalbackupbase**</span><span class="sxs-lookup"><span data-stu-id="880ed-125">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="880ed-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="880ed-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="880ed-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="880ed-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="880ed-128">Basis für differenziellen Export.</span><span class="sxs-lookup"><span data-stu-id="880ed-128">Base for differential export.</span></span> <span data-ttu-id="880ed-129">Dies ist entweder ein Pfad zu einer [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) -Instanz, die den Verweis Punkt darstellt, oder ein Pfad zu einer [**MSVM- \_ snapshotcollection**](msvm-snapshotcollection.md) -Instanz, die die Momentaufnahme darstellt, die als Basis für den differenziellen Export verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="880ed-129">This is either path to an [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the reference point, or path to an [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) instance that represents the snapshot to be used as a base for differential export.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="880ed-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="880ed-130">Requirements</span></span>



| <span data-ttu-id="880ed-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="880ed-131">Requirement</span></span> | <span data-ttu-id="880ed-132">Wert</span><span class="sxs-lookup"><span data-stu-id="880ed-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="880ed-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="880ed-133">Minimum supported client</span></span><br/> | <span data-ttu-id="880ed-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="880ed-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="880ed-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="880ed-135">Minimum supported server</span></span><br/> | <span data-ttu-id="880ed-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="880ed-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="880ed-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="880ed-137">Namespace</span></span><br/>                | <span data-ttu-id="880ed-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="880ed-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="880ed-139">MOF</span><span class="sxs-lookup"><span data-stu-id="880ed-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="880ed-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="880ed-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="880ed-141">DLL</span><span class="sxs-lookup"><span data-stu-id="880ed-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="880ed-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="880ed-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="880ed-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="880ed-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880ed-144">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="880ed-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




