---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.
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
ms.openlocfilehash: d868e3943f22a71b4513f4f77841ddea9204ffea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977480"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="2f52f-103">SystemConfig- \_ Klasse "phydisk"</span><span class="sxs-lookup"><span data-stu-id="2f52f-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="2f52f-104">Diese Klasse ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="2f52f-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="2f52f-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="2f52f-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f52f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f52f-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="2f52f-107">Member</span><span class="sxs-lookup"><span data-stu-id="2f52f-107">Members</span></span>

<span data-ttu-id="2f52f-108">Die Klasse " **SystemConfig \_ phydisk** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2f52f-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="2f52f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f52f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f52f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f52f-110">Properties</span></span>

<span data-ttu-id="2f52f-111">Die Klasse " **SystemConfig \_ phydisk** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f52f-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f52f-112">**Bootdriveletter**</span><span class="sxs-lookup"><span data-stu-id="2f52f-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-113">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="2f52f-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-115">Qualifizierer: **wmidataid** (14), **Max** (3), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="2f52f-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-116">Laufwerk Buchstabe des Start Laufwerks in der Form " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="2f52f-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-117">**Bytespersektor**</span><span class="sxs-lookup"><span data-stu-id="2f52f-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-120">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="2f52f-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-121">Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="2f52f-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-122">**Rad**</span><span class="sxs-lookup"><span data-stu-id="2f52f-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-123">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2f52f-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-125">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="2f52f-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-126">Die Gesamtanzahl der Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="2f52f-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="2f52f-127">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2f52f-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="2f52f-128">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2f52f-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="2f52f-129">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2f52f-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-130">**Disknumber**</span><span class="sxs-lookup"><span data-stu-id="2f52f-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-133">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="2f52f-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-134">Index Nummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="2f52f-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-135">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="2f52f-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-136">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="2f52f-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-138">Qualifizierer: **wmidataid** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="2f52f-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-139">Der Name des Laufwerks Herstellers.</span><span class="sxs-lookup"><span data-stu-id="2f52f-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-140">**Pad**</span><span class="sxs-lookup"><span data-stu-id="2f52f-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-141">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2f52f-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-143">Qualifizierer: **wmidataid** (13)</span><span class="sxs-lookup"><span data-stu-id="2f52f-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-144">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f52f-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="2f52f-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-148">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="2f52f-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-149">Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="2f52f-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-150">**Scsilun**</span><span class="sxs-lookup"><span data-stu-id="2f52f-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-153">Qualifizierer: **wmidataid** (9)</span><span class="sxs-lookup"><span data-stu-id="2f52f-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-154">SCSI-logische Gerätenummer (LUN) des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="2f52f-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-155">**Scsipath**</span><span class="sxs-lookup"><span data-stu-id="2f52f-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-156">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-158">Qualifizierer: **wmidataid** (7)</span><span class="sxs-lookup"><span data-stu-id="2f52f-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-159">SCSI-Busnummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="2f52f-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="2f52f-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-163">Qualifizierer: **wmidataid** (6)</span><span class="sxs-lookup"><span data-stu-id="2f52f-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-164">SCSI-Nummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="2f52f-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-165">**Scsitarget**</span><span class="sxs-lookup"><span data-stu-id="2f52f-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-166">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-168">Qualifizierer: **wmidataid** (8)</span><span class="sxs-lookup"><span data-stu-id="2f52f-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-169">Enthält die Nummer des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="2f52f-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-170">**Sector-Spur**</span><span class="sxs-lookup"><span data-stu-id="2f52f-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-173">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="2f52f-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-174">Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="2f52f-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-175">**Schonen**</span><span class="sxs-lookup"><span data-stu-id="2f52f-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-176">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="2f52f-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-178">Qualifizierer: **wmidataid** (15), **Max** (2), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="2f52f-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-179">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f52f-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="2f52f-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-181">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f52f-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-183">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="2f52f-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-184">Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="2f52f-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="2f52f-185">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2f52f-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="2f52f-186">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2f52f-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="2f52f-187">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2f52f-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="2f52f-188">**Schreibzugriff aktiviert**</span><span class="sxs-lookup"><span data-stu-id="2f52f-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f52f-189">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2f52f-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f52f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f52f-191">Qualifizierer: **wmidataid** (12)</span><span class="sxs-lookup"><span data-stu-id="2f52f-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="2f52f-192">True, wenn der Schreib Cache aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2f52f-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f52f-193">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2f52f-193">Requirements</span></span>



| <span data-ttu-id="2f52f-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f52f-194">Requirement</span></span> | <span data-ttu-id="2f52f-195">Wert</span><span class="sxs-lookup"><span data-stu-id="2f52f-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f52f-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f52f-196">Minimum supported client</span></span><br/> | <span data-ttu-id="2f52f-197">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f52f-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2f52f-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f52f-198">Minimum supported server</span></span><br/> | <span data-ttu-id="2f52f-199">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f52f-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f52f-200">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f52f-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f52f-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="2f52f-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




