---
description: 'SystemConfig_LogDisk Klasse: Diese Klasse ist die Ereignistypklasse für logische Datenträgerkonfigurationsereignisse.'
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
ms.openlocfilehash: 1d7ca8dc3f632e88c250715292a27e18ff36e3af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106108"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="1a317-103">SystemConfig \_ LogDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="1a317-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="1a317-104">Diese Klasse ist die Ereignistypklasse für Logische Datenträgerkonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="1a317-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="1a317-105">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1a317-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a317-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a317-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="1a317-107">Member</span><span class="sxs-lookup"><span data-stu-id="1a317-107">Members</span></span>

<span data-ttu-id="1a317-108">Die **\_ LogDisk-Klasse SystemConfig** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="1a317-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="1a317-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a317-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a317-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a317-110">Properties</span></span>

<span data-ttu-id="1a317-111">Die **\_ LogDisk-Klasse SystemConfig** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1a317-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a317-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="1a317-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-113">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-115">Qualifizierer: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="1a317-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-116">Anzahl von Bytes in jedem Sektor für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="1a317-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="1a317-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-118">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-120">Qualifizierer: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="1a317-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-121">Indexnummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="1a317-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="1a317-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-123">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="1a317-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="1a317-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-125">Qualifizierer: **WmiDataId** (6), **Max** (4), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="1a317-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="1a317-126">Laufwerkbuchstaben des Datenträgers im Formular " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="1a317-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="1a317-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="1a317-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-128">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-130">Qualifizierer: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="1a317-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-131">Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="1a317-131">Type of disk drive.</span></span> <span data-ttu-id="1a317-132">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="1a317-132">Possible values are:</span></span>



| <span data-ttu-id="1a317-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1a317-133">Value</span></span>                                                                        | <span data-ttu-id="1a317-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1a317-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1a317-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1a317-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1a317-136">Partition</span><span class="sxs-lookup"><span data-stu-id="1a317-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="1a317-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1a317-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1a317-138">Volume</span><span class="sxs-lookup"><span data-stu-id="1a317-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="1a317-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1a317-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1a317-140">Erweiterte Partition auf mehreren Datenträgern</span><span class="sxs-lookup"><span data-stu-id="1a317-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1a317-141">**Dateisystem**</span><span class="sxs-lookup"><span data-stu-id="1a317-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-142">Datentyp: **char16**</span><span class="sxs-lookup"><span data-stu-id="1a317-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-144">Qualifizierer: **WmiDataId** (14), **Max** (16), **Format(s)**</span><span class="sxs-lookup"><span data-stu-id="1a317-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="1a317-145">Dateisystem auf dem logischen Datenträger, z. B. NTFS.</span><span class="sxs-lookup"><span data-stu-id="1a317-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="1a317-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-147">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="1a317-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-149">Qualifizierer: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="1a317-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-150">Anzahl der freien Cluster im angegebenen Volume.</span><span class="sxs-lookup"><span data-stu-id="1a317-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="1a317-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-152">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-154">Qualifizierer: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="1a317-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-155">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a317-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="1a317-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-157">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-159">Qualifizierer: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="1a317-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-160">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a317-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="1a317-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-162">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-164">Qualifizierer: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="1a317-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-165">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a317-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="1a317-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-167">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-169">Qualifizierer: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="1a317-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-170">Indexnummer der Partition.</span><span class="sxs-lookup"><span data-stu-id="1a317-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="1a317-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-172">Datentyp: **uint64**</span><span class="sxs-lookup"><span data-stu-id="1a317-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-174">Qualifizierer: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="1a317-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-175">Gesamtgröße der Partition in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1a317-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="1a317-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-177">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-179">Qualifizierer: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="1a317-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-180">Anzahl der Sektoren im Volume.</span><span class="sxs-lookup"><span data-stu-id="1a317-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-181">**Größe**</span><span class="sxs-lookup"><span data-stu-id="1a317-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-182">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-184">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="1a317-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-185">Größe des Laufwerks in Byte.</span><span class="sxs-lookup"><span data-stu-id="1a317-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-186">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="1a317-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-187">Datentyp: **uint64**</span><span class="sxs-lookup"><span data-stu-id="1a317-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-189">Qualifizierer: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="1a317-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-190">Startoffset (in Bytes) der Partition vom Anfang des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="1a317-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="1a317-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-192">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="1a317-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-194">Qualifizierer: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="1a317-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-195">Anzahl der verwendeten und freien Cluster im Volume.</span><span class="sxs-lookup"><span data-stu-id="1a317-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="1a317-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="1a317-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a317-197">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a317-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a317-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a317-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a317-199">Qualifizierer: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="1a317-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="1a317-200">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1a317-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a317-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a317-201">Requirements</span></span>



| <span data-ttu-id="1a317-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a317-202">Requirement</span></span> | <span data-ttu-id="1a317-203">Wert</span><span class="sxs-lookup"><span data-stu-id="1a317-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a317-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a317-204">Minimum supported client</span></span><br/> | <span data-ttu-id="1a317-205">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a317-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a317-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a317-206">Minimum supported server</span></span><br/> | <span data-ttu-id="1a317-207">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a317-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a317-208">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a317-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a317-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="1a317-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




