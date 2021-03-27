---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.
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
ms.openlocfilehash: 2f7eab1cec90630e25ee5968e5740f787acb8662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980544"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="ab1a9-103">SystemConfig \_ v0 \_ phydisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="ab1a9-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="ab1a9-104">Diese Klasse ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="ab1a9-105">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab1a9-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="ab1a9-107">Member</span><span class="sxs-lookup"><span data-stu-id="ab1a9-107">Members</span></span>

<span data-ttu-id="ab1a9-108">Die Klasse " **SystemConfig \_ v0 \_ phydisk** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ab1a9-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="ab1a9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1a9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab1a9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1a9-110">Properties</span></span>

<span data-ttu-id="ab1a9-111">Die **System config \_ v0 \_ phydisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab1a9-112">**Bootdriveletter**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-113">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="ab1a9-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-115">Qualifizierer: **wmidataid** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-116">Laufwerk Buchstabe des Start Laufwerks in der Form " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="ab1a9-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-117">**Bytespersektor**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-120">Qualifizierer: **wmidataid** (2)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-121">Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-122">**Rad**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-123">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-125">Qualifizierer: **wmidataid** (5)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-126">Die Gesamtanzahl der Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="ab1a9-127">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="ab1a9-128">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="ab1a9-129">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-130">**Disknumber**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-133">Qualifizierer: **wmidataid** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-134">Index Nummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-135">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-136">Datentyp: **char16** Array</span><span class="sxs-lookup"><span data-stu-id="ab1a9-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-138">Qualifizierer: **wmidataid** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-139">Der Name des Laufwerks Herstellers.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-143">Qualifizierer: **wmidataid** (11)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-144">Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-145">**Scsilun**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-148">Qualifizierer: **wmidataid** (9)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-149">SCSI-logische Gerätenummer (LUN) des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-150">**Scsipath**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-153">Qualifizierer: **wmidataid** (7)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-154">SCSI-Busnummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-156">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-158">Qualifizierer: **wmidataid** (6)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-159">SCSI-Nummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-160">**Scsitarget**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-163">Qualifizierer: **wmidataid** (8)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-164">Enthält die Nummer des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-165">**Sector-Spur**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-166">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-168">Qualifizierer: **wmidataid** (3)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-169">Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-173">Qualifizierer: **wmidataid** (4)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-174">Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="ab1a9-175">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="ab1a9-176">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="ab1a9-177">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a9-178">**Schreibzugriff aktiviert**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1a9-179">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ab1a9-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1a9-181">Qualifizierer: **wmidataid** (12)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="ab1a9-182">True, wenn der Schreib Cache aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1a9-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab1a9-183">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-183">Requirements</span></span>



| <span data-ttu-id="ab1a9-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab1a9-184">Requirement</span></span> | <span data-ttu-id="ab1a9-185">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1a9-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab1a9-186">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-186">Minimum supported client</span></span><br/> | <span data-ttu-id="ab1a9-187">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ab1a9-187">None supported</span></span><br/>                            |
| <span data-ttu-id="ab1a9-188">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab1a9-188">Minimum supported server</span></span><br/> | <span data-ttu-id="ab1a9-189">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab1a9-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab1a9-190">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab1a9-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1a9-191">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="ab1a9-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




