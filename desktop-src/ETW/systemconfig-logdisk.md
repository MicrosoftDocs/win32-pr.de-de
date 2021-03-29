---
description: Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: SystemConfig_LogDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3bff1cf526dfb7bf1ddd36fcb887e8a4b837be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977585"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="04641-103">SystemConfig \_ logdisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="04641-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="04641-104">Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.</span><span class="sxs-lookup"><span data-stu-id="04641-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="04641-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="04641-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="04641-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="04641-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="04641-107">Member</span><span class="sxs-lookup"><span data-stu-id="04641-107">Members</span></span>

<span data-ttu-id="04641-108">Die **SystemConfig \_ logdisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="04641-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="04641-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04641-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04641-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04641-110">Properties</span></span>

<span data-ttu-id="04641-111">Die **SystemConfig \_ logdisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="04641-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04641-112">**Bytespersektor**</span><span class="sxs-lookup"><span data-stu-id="04641-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-115">Qualifizierer: **wmidataid** (10)</span><span class="sxs-lookup"><span data-stu-id="04641-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="04641-116">Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="04641-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="04641-117">**Disknumber**</span><span class="sxs-lookup"><span data-stu-id="04641-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-120">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="04641-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="04641-121">Index Nummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="04641-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="04641-122">**Driveletterstring**</span><span class="sxs-lookup"><span data-stu-id="04641-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-123">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="04641-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="04641-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-125">Qualifizierer: **wmidataid** (6), **Max** (4), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="04641-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="04641-126">Laufwerk Buchstabe des Datenträgers in der Form " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="04641-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="04641-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="04641-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-130">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="04641-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="04641-131">Der Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="04641-131">Type of disk drive.</span></span> <span data-ttu-id="04641-132">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="04641-132">Possible values are:</span></span>



| <span data-ttu-id="04641-133">Wert</span><span class="sxs-lookup"><span data-stu-id="04641-133">Value</span></span>                                                                        | <span data-ttu-id="04641-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="04641-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="04641-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04641-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="04641-136">Partition</span><span class="sxs-lookup"><span data-stu-id="04641-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="04641-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04641-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="04641-138">Volume</span><span class="sxs-lookup"><span data-stu-id="04641-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="04641-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="04641-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="04641-140">Erweiterte Partition auf mehreren Datenträgern</span><span class="sxs-lookup"><span data-stu-id="04641-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="04641-141">**Verwendet**</span><span class="sxs-lookup"><span data-stu-id="04641-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-142">Datentyp: **char16**</span><span class="sxs-lookup"><span data-stu-id="04641-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="04641-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-144">Qualifizierer: **wmidataid** (14), **Max** (16), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="04641-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="04641-145">Dateisystem auf dem logischen Datenträger, z. b. NTFS.</span><span class="sxs-lookup"><span data-stu-id="04641-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="04641-146">**"Numoffreeclusters"**</span><span class="sxs-lookup"><span data-stu-id="04641-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-147">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="04641-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="04641-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-149">Qualifizierer: **wmidataid** (12)</span><span class="sxs-lookup"><span data-stu-id="04641-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="04641-150">Anzahl der freien Cluster im angegebenen Volume.</span><span class="sxs-lookup"><span data-stu-id="04641-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="04641-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="04641-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-154">Qualifizierer: **wmidataid** (7)</span><span class="sxs-lookup"><span data-stu-id="04641-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="04641-155">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="04641-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="04641-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="04641-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-159">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="04641-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="04641-160">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="04641-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="04641-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="04641-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-164">Qualifizierer: **wmidataid** (16)</span><span class="sxs-lookup"><span data-stu-id="04641-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="04641-165">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="04641-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="04641-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="04641-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-169">Qualifizierer: **wmidataid** (8)</span><span class="sxs-lookup"><span data-stu-id="04641-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="04641-170">Index Nummer der Partition.</span><span class="sxs-lookup"><span data-stu-id="04641-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="04641-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="04641-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-172">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04641-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04641-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-174">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="04641-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="04641-175">Gesamtgröße der Partition in Bytes.</span><span class="sxs-lookup"><span data-stu-id="04641-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="04641-176">**Sector-Cluster**</span><span class="sxs-lookup"><span data-stu-id="04641-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-177">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-179">Qualifizierer: **wmidataid** (9)</span><span class="sxs-lookup"><span data-stu-id="04641-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="04641-180">Anzahl der Sektoren auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="04641-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="04641-181">**Größe**</span><span class="sxs-lookup"><span data-stu-id="04641-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-184">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="04641-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="04641-185">Größe des Laufwerks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="04641-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="04641-186">**Starto ffset**</span><span class="sxs-lookup"><span data-stu-id="04641-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-187">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04641-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04641-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-189">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="04641-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="04641-190">Start Offset (in Bytes) der Partition vom Anfang des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="04641-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="04641-191">**Totalnummeriofclusters**</span><span class="sxs-lookup"><span data-stu-id="04641-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-192">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="04641-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="04641-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-194">Qualifizierer: **wmidataid** (13)</span><span class="sxs-lookup"><span data-stu-id="04641-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="04641-195">Anzahl der verwendeten und freien Cluster im Volume.</span><span class="sxs-lookup"><span data-stu-id="04641-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="04641-196">**Volumeext**</span><span class="sxs-lookup"><span data-stu-id="04641-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04641-197">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04641-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04641-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04641-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04641-199">Qualifizierer: **wmidataid** (15)</span><span class="sxs-lookup"><span data-stu-id="04641-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="04641-200">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="04641-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04641-201">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="04641-201">Requirements</span></span>



| <span data-ttu-id="04641-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04641-202">Requirement</span></span> | <span data-ttu-id="04641-203">Wert</span><span class="sxs-lookup"><span data-stu-id="04641-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04641-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04641-204">Minimum supported client</span></span><br/> | <span data-ttu-id="04641-205">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04641-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04641-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04641-206">Minimum supported server</span></span><br/> | <span data-ttu-id="04641-207">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04641-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04641-208">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="04641-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04641-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="04641-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




