---
description: Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980545"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="9ba9b-103">SystemConfig \_ v0 \_ logdisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="9ba9b-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="9ba9b-104">Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="9ba9b-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba9b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ba9b-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a><span data-ttu-id="9ba9b-107">Member</span><span class="sxs-lookup"><span data-stu-id="9ba9b-107">Members</span></span>

<span data-ttu-id="9ba9b-108">Die **SystemConfig \_ v0 \_ logdisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9ba9b-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="9ba9b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ba9b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ba9b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ba9b-110">Properties</span></span>

<span data-ttu-id="9ba9b-111">Die **SystemConfig \_ v0 \_ logdisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ba9b-112">**Bytespersektor**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-115">Qualifizierer: **wmidataid** (10)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-116">Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-117">**Disknumber**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-120">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-121">Index Nummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-122">**Driveletterstring**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-123">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="9ba9b-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-125">Qualifizierer: **wmidataid** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-126">Laufwerk Buchstabe des Datenträgers in der Form " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="9ba9b-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-130">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-131">Der Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-131">Type of disk drive.</span></span> <span data-ttu-id="9ba9b-132">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="9ba9b-132">Possible values are:</span></span>



| <span data-ttu-id="9ba9b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba9b-133">Value</span></span>                                                                        | <span data-ttu-id="9ba9b-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9ba9b-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9ba9b-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9ba9b-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="9ba9b-136">Partition</span><span class="sxs-lookup"><span data-stu-id="9ba9b-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="9ba9b-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9ba9b-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9ba9b-138">Volume</span><span class="sxs-lookup"><span data-stu-id="9ba9b-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="9ba9b-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9ba9b-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9ba9b-140">Erweiterte Partition auf mehreren Datenträgern</span><span class="sxs-lookup"><span data-stu-id="9ba9b-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9ba9b-141">**Verwendet**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-142">Datentyp: **char16**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-144">Qualifizierer: **wmidataid** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-145">Dateisystem auf dem logischen Datenträger, z. b. NTFS.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-146">**"Numoffreeclusters"**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-147">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-149">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-150">Anzahl der freien Cluster im angegebenen Volume.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-151">**Pad**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-154">Qualifizierer: **wmidataid** (7)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-155">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-159">Qualifizierer: **wmidataid** (8)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-160">Index Nummer der Partition.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-162">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-164">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-165">Gesamtgröße der Partition in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-166">**Sector-Cluster**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-169">Qualifizierer: **wmidataid** (9)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-170">Anzahl der Sektoren auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-171">**Größe**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-174">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-175">Größe des Laufwerks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-176">**Starto ffset**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-177">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-179">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-180">Start Offset (in Bytes) der Partition vom Anfang des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-181">**Totalnummeriofclusters**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-182">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-184">Qualifizierer: **wmidataid** (12)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-185">Anzahl der verwendeten und freien Cluster im Volume.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="9ba9b-186">**Volumeext**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba9b-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba9b-189">Qualifizierer: **wmidataid** (14)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="9ba9b-190">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="9ba9b-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ba9b-191">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-191">Requirements</span></span>



| <span data-ttu-id="9ba9b-192">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ba9b-192">Requirement</span></span> | <span data-ttu-id="9ba9b-193">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba9b-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9ba9b-194">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-194">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba9b-195">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ba9b-195">None supported</span></span><br/>                            |
| <span data-ttu-id="9ba9b-196">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ba9b-196">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba9b-197">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba9b-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ba9b-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9ba9b-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba9b-199">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="9ba9b-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




