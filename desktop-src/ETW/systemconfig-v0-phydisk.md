---
description: 'SystemConfig_V0_PhyDisk-Klasse: Diese Klasse ist die Ereignistypklasse für Physische Datenträgerkonfigurationsereignisse.'
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: SystemConfig_V0_PhyDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdb12fac8b2b902f21258fd4c7cfe9846d0456eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105958"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="e2082-103">SystemConfig \_ V0 \_ PhyDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2082-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="e2082-104">Diese Klasse ist die Ereignistypklasse für Physische Datenträgerkonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="e2082-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="e2082-105">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e2082-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2082-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2082-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a><span data-ttu-id="e2082-107">Member</span><span class="sxs-lookup"><span data-stu-id="e2082-107">Members</span></span>

<span data-ttu-id="e2082-108">Die **SystemConfig \_ V0 \_ PhyDisk-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e2082-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="e2082-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2082-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2082-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2082-110">Properties</span></span>

<span data-ttu-id="e2082-111">Die **SystemConfig \_ V0 \_ PhyDisk-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2082-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2082-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="e2082-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-113">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="e2082-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2082-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-115">Qualifizierer: **WmiDataId** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="e2082-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-116">Laufwerkbuchstabe des Startlaufwerks im Format <letter> ":".</span><span class="sxs-lookup"><span data-stu-id="e2082-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="e2082-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="e2082-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-118">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-120">Qualifizierer: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="e2082-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-121">Anzahl der Bytes in jedem Sektor für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="e2082-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-122">**Zylinder**</span><span class="sxs-lookup"><span data-stu-id="e2082-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-123">Datentyp: **uint64**</span><span class="sxs-lookup"><span data-stu-id="e2082-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-125">Qualifizierer: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="e2082-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-126">Gesamtanzahl der Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="e2082-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="e2082-127">Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e2082-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="e2082-128">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e2082-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="e2082-129">Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2082-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="e2082-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-131">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-133">Qualifizierer: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="e2082-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-134">Indexnummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="e2082-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-135">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="e2082-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-136">Datentyp: **char16-Array**</span><span class="sxs-lookup"><span data-stu-id="e2082-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2082-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-138">Qualifizierer: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="e2082-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-139">Name des Laufwerkherstellers.</span><span class="sxs-lookup"><span data-stu-id="e2082-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="e2082-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-141">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-143">Qualifizierer: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="e2082-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-144">Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="e2082-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="e2082-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-146">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-148">Qualifizierer: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="e2082-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-149">SCSI-LUN (Logical Unit Number) des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="e2082-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="e2082-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-151">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-153">Qualifizierer: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="e2082-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-154">SCSI-Busnummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="e2082-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="e2082-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-156">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-158">Qualifizierer: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="e2082-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-159">SCSI-Nummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="e2082-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="e2082-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-161">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-163">Qualifizierer: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="e2082-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-164">Enthält die Nummer des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="e2082-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="e2082-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-166">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-168">Qualifizierer: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="e2082-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-169">Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="e2082-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="e2082-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-171">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2082-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-173">Qualifizierer: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="e2082-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-174">Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="e2082-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="e2082-175">Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e2082-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="e2082-176">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e2082-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="e2082-177">Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2082-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="e2082-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="e2082-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2082-179">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="e2082-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2082-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2082-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2082-181">Qualifizierer: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="e2082-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="e2082-182">True, wenn der Schreibcache aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e2082-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2082-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2082-183">Requirements</span></span>



| <span data-ttu-id="e2082-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2082-184">Requirement</span></span> | <span data-ttu-id="e2082-185">Wert</span><span class="sxs-lookup"><span data-stu-id="e2082-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2082-186">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2082-186">Minimum supported client</span></span><br/> | <span data-ttu-id="e2082-187">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e2082-187">None supported</span></span><br/>                            |
| <span data-ttu-id="e2082-188">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2082-188">Minimum supported server</span></span><br/> | <span data-ttu-id="e2082-189">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2082-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2082-190">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2082-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2082-191">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="e2082-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




