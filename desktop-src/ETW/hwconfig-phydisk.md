---
description: Die Klasse hwconfig \_ phydisk ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: HWConfig_PhyDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977656"
---
# <a name="hwconfig_phydisk-class"></a><span data-ttu-id="aa9bf-104">Hwconfig- \_ Klasse "phydisk"</span><span class="sxs-lookup"><span data-stu-id="aa9bf-104">HWConfig\_PhyDisk class</span></span>

<span data-ttu-id="aa9bf-105">Die Klasse **hwconfig \_ phydisk** ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-105">The **HWConfig\_PhyDisk** class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="aa9bf-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa9bf-107">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a><span data-ttu-id="aa9bf-108">Member</span><span class="sxs-lookup"><span data-stu-id="aa9bf-108">Members</span></span>

<span data-ttu-id="aa9bf-109">Die Klasse **hwconfig \_ phydisk** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aa9bf-109">The **HWConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="aa9bf-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa9bf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa9bf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa9bf-111">Properties</span></span>

<span data-ttu-id="aa9bf-112">Die Klasse **hwconfig \_ phydisk** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-112">The **HWConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa9bf-113">Bytespersektor</span><span class="sxs-lookup"><span data-stu-id="aa9bf-113">BytesPerSector</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-116">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-117">Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-117">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-118">Rad</span><span class="sxs-lookup"><span data-stu-id="aa9bf-118">Cylinders</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-119">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-121">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-122">Die Gesamtanzahl der Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-122">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="aa9bf-123">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-123">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aa9bf-124">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-124">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="aa9bf-125">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-125">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-126">Disknumber</span><span class="sxs-lookup"><span data-stu-id="aa9bf-126">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-127">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-129">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-129">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-130">Index Nummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-130">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-131">Hersteller</span><span class="sxs-lookup"><span data-stu-id="aa9bf-131">Manufacturer</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-134">Qualifizierer: wmidataid (10), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="aa9bf-134">Qualifiers: WmiDataId(10), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-135">Der Name des Laufwerks Herstellers.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-135">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-136">Scsilun</span><span class="sxs-lookup"><span data-stu-id="aa9bf-136">SCSILun</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-139">Qualifizierer: wmidataid (9)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-139">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-140">SCSI-logische Gerätenummer (LUN) des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-140">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-141">Scsipath</span><span class="sxs-lookup"><span data-stu-id="aa9bf-141">SCSIPath</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-144">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-144">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-145">SCSI-Busnummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-145">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-146">SCSIPort</span><span class="sxs-lookup"><span data-stu-id="aa9bf-146">SCSIPort</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-149">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-149">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-150">SCSI-Nummer des SCSI-Adapters.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-150">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-151">Scsitarget</span><span class="sxs-lookup"><span data-stu-id="aa9bf-151">SCSITarget</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-154">Qualifizierer: wmidataid (8)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-154">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-155">Enthält die Nummer des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-155">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-156">Sector-Spur</span><span class="sxs-lookup"><span data-stu-id="aa9bf-156">SectorsPerTrack</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-159">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-159">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-160">Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-160">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="aa9bf-161">TracksPerCylinder</span><span class="sxs-lookup"><span data-stu-id="aa9bf-161">TracksPerCylinder</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9bf-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9bf-164">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-164">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="aa9bf-165">Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-165">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="aa9bf-166">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-166">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aa9bf-167">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-167">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="aa9bf-168">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="aa9bf-168">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa9bf-169">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-169">Requirements</span></span>



| <span data-ttu-id="aa9bf-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa9bf-170">Requirement</span></span> | <span data-ttu-id="aa9bf-171">Wert</span><span class="sxs-lookup"><span data-stu-id="aa9bf-171">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="aa9bf-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-172">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9bf-173">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa9bf-173">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aa9bf-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa9bf-174">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9bf-175">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa9bf-175">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="aa9bf-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa9bf-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9bf-177">**Hwconfig**</span><span class="sxs-lookup"><span data-stu-id="aa9bf-177">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




