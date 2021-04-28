---
description: 'SystemConfig_V0_LogDisk Klasse: Diese Klasse ist die Ereignistypklasse für logische Datenträgerkonfigurationsereignisse.'
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
ms.openlocfilehash: eb0ad959d637a38a03b77bd8d7a812ff608ddc04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105978"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="72b04-103">SystemConfig \_ V0 \_ LogDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="72b04-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="72b04-104">Diese Klasse ist die Ereignistypklasse für Logische Datenträgerkonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="72b04-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="72b04-105">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="72b04-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b04-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="72b04-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="72b04-107">Member</span><span class="sxs-lookup"><span data-stu-id="72b04-107">Members</span></span>

<span data-ttu-id="72b04-108">Die **\_ \_ LogDisk-Klasse SystemConfig V0** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="72b04-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="72b04-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72b04-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72b04-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72b04-110">Properties</span></span>

<span data-ttu-id="72b04-111">Die **\_ \_ LogDisk-Klasse SystemConfig V0** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="72b04-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72b04-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="72b04-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-113">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-115">Qualifizierer: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="72b04-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-116">Anzahl von Bytes in jedem Sektor für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="72b04-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="72b04-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-118">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-120">Qualifizierer: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="72b04-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-121">Indexnummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="72b04-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="72b04-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-123">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="72b04-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="72b04-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-125">Qualifizierer: **WmiDataId** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="72b04-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-126">Laufwerkbuchstaben des Datenträgers im Formular " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="72b04-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="72b04-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="72b04-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-128">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-130">Qualifizierer: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="72b04-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-131">Typ des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="72b04-131">Type of disk drive.</span></span> <span data-ttu-id="72b04-132">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="72b04-132">Possible values are:</span></span>



| <span data-ttu-id="72b04-133">Wert</span><span class="sxs-lookup"><span data-stu-id="72b04-133">Value</span></span>                                                                        | <span data-ttu-id="72b04-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="72b04-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="72b04-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="72b04-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="72b04-136">Partition</span><span class="sxs-lookup"><span data-stu-id="72b04-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="72b04-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="72b04-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="72b04-138">Volume</span><span class="sxs-lookup"><span data-stu-id="72b04-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="72b04-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="72b04-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="72b04-140">Erweiterte Partition auf mehreren Datenträgern</span><span class="sxs-lookup"><span data-stu-id="72b04-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="72b04-141">**Dateisystem**</span><span class="sxs-lookup"><span data-stu-id="72b04-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-142">Datentyp: **char16**</span><span class="sxs-lookup"><span data-stu-id="72b04-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-144">Qualifizierer: **WmiDataId** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="72b04-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-145">Dateisystem auf dem logischen Datenträger, z. B. NTFS.</span><span class="sxs-lookup"><span data-stu-id="72b04-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="72b04-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-147">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="72b04-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-149">Qualifizierer: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="72b04-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-150">Anzahl der freien Cluster im angegebenen Volume.</span><span class="sxs-lookup"><span data-stu-id="72b04-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-151">**Pad**</span><span class="sxs-lookup"><span data-stu-id="72b04-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-152">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-154">Qualifizierer: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="72b04-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-155">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="72b04-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="72b04-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-157">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-159">Qualifizierer: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="72b04-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-160">Indexnummer der Partition.</span><span class="sxs-lookup"><span data-stu-id="72b04-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="72b04-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-162">Datentyp: **uint64**</span><span class="sxs-lookup"><span data-stu-id="72b04-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-164">Qualifizierer: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="72b04-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-165">Gesamtgröße der Partition in Bytes.</span><span class="sxs-lookup"><span data-stu-id="72b04-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-166">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="72b04-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-167">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-169">Qualifizierer: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="72b04-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-170">Anzahl der Sektoren im Volume.</span><span class="sxs-lookup"><span data-stu-id="72b04-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-171">**Größe**</span><span class="sxs-lookup"><span data-stu-id="72b04-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-172">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-174">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="72b04-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-175">Größe des Laufwerks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="72b04-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-176">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="72b04-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-177">Datentyp: **uint64**</span><span class="sxs-lookup"><span data-stu-id="72b04-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-179">Qualifizierer: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="72b04-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-180">Startoffset (in Bytes) der Partition vom Anfang des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="72b04-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="72b04-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-182">Datentyp: **sint64**</span><span class="sxs-lookup"><span data-stu-id="72b04-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-184">Qualifizierer: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="72b04-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-185">Anzahl der verwendeten und kostenlosen Cluster im Volume.</span><span class="sxs-lookup"><span data-stu-id="72b04-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="72b04-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="72b04-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b04-187">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="72b04-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b04-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72b04-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b04-189">Qualifizierer: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="72b04-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="72b04-190">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="72b04-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72b04-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72b04-191">Requirements</span></span>



| <span data-ttu-id="72b04-192">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72b04-192">Requirement</span></span> | <span data-ttu-id="72b04-193">Wert</span><span class="sxs-lookup"><span data-stu-id="72b04-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72b04-194">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72b04-194">Minimum supported client</span></span><br/> | <span data-ttu-id="72b04-195">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="72b04-195">None supported</span></span><br/>                            |
| <span data-ttu-id="72b04-196">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72b04-196">Minimum supported server</span></span><br/> | <span data-ttu-id="72b04-197">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72b04-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72b04-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72b04-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b04-199">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="72b04-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




