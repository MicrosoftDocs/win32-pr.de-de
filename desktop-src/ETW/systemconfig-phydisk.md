---
description: 'SystemConfig_PhyDisk Klasse: Diese Klasse ist die Ereignistypklasse für physische Datenträgerkonfigurationsereignisse.'
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: SystemConfig_PhyDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: 52ab249ab5087a1528317687d90f6d8fa665bc1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106098"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="8e836-103">SystemConfig \_ PhyDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e836-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="8e836-104">Diese Klasse ist die Ereignistypklasse für physische Datenträgerkonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="8e836-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="8e836-105">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="8e836-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e836-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e836-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a><span data-ttu-id="8e836-107">Member</span><span class="sxs-lookup"><span data-stu-id="8e836-107">Members</span></span>

<span data-ttu-id="8e836-108">Die **SystemConfig \_ PhyDisk-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="8e836-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="8e836-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e836-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e836-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e836-110">Properties</span></span>

<span data-ttu-id="8e836-111">Die **SystemConfig \_ PhyDisk-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e836-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e836-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="8e836-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-113">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="8e836-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e836-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-115">Qualifizierer: **WmiDataId** (14), **Max** (3), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="8e836-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8e836-116">Laufwerkbuchstaben des Startlaufwerks im Folgenden: <letter> ":".</span><span class="sxs-lookup"><span data-stu-id="8e836-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="8e836-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="8e836-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-118">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-120">Qualifizierer: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="8e836-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-121">Anzahl von Bytes in jedem Sektor für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="8e836-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-122">**Zylinder**</span><span class="sxs-lookup"><span data-stu-id="8e836-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-123">Datentyp: **uint64**</span><span class="sxs-lookup"><span data-stu-id="8e836-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-125">Qualifizierer: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="8e836-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-126">Gesamtanzahl der Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="8e836-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="8e836-127">Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt.</span><span class="sxs-lookup"><span data-stu-id="8e836-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="8e836-128">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8e836-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="8e836-129">Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e836-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="8e836-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-131">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-133">Qualifizierer: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="8e836-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-134">Indexnummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="8e836-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-135">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="8e836-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-136">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="8e836-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e836-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-138">Qualifizierer: **WmiDataId** (10), **Max** (256), **Format(s)**</span><span class="sxs-lookup"><span data-stu-id="8e836-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8e836-139">Name des Laufwerkherstellers.</span><span class="sxs-lookup"><span data-stu-id="8e836-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-140">**Pad**</span><span class="sxs-lookup"><span data-stu-id="8e836-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-141">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="8e836-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-143">Qualifizierer: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="8e836-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-144">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e836-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="8e836-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-146">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-148">Qualifizierer: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="8e836-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-149">Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="8e836-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="8e836-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-151">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-153">Qualifizierer: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="8e836-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-154">SCSI Logical Unit Number (LUN) des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="8e836-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="8e836-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-156">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-158">Qualifizierer: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="8e836-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-159">SCSI-Busnummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="8e836-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="8e836-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-161">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-163">Qualifizierer: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="8e836-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-164">SCSI-Nummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="8e836-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="8e836-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-166">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-168">Qualifizierer: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="8e836-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-169">Enthält die Nummer des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="8e836-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="8e836-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-171">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-173">Qualifizierer: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="8e836-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-174">Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="8e836-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-175">**Ersatz**</span><span class="sxs-lookup"><span data-stu-id="8e836-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-176">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="8e836-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e836-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-178">Qualifizierer: **WmiDataId** (15), **Max** (2), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="8e836-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="8e836-179">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e836-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="8e836-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-181">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8e836-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-183">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="8e836-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-184">Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="8e836-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="8e836-185">Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt.</span><span class="sxs-lookup"><span data-stu-id="8e836-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="8e836-186">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8e836-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="8e836-187">Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e836-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="8e836-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="8e836-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e836-189">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="8e836-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8e836-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8e836-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e836-191">Qualifizierer: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="8e836-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="8e836-192">True, wenn der Schreibcache aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8e836-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e836-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e836-193">Requirements</span></span>



| <span data-ttu-id="8e836-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e836-194">Requirement</span></span> | <span data-ttu-id="8e836-195">Wert</span><span class="sxs-lookup"><span data-stu-id="8e836-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e836-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e836-196">Minimum supported client</span></span><br/> | <span data-ttu-id="8e836-197">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e836-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8e836-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e836-198">Minimum supported server</span></span><br/> | <span data-ttu-id="8e836-199">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e836-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e836-200">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e836-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e836-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="8e836-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




