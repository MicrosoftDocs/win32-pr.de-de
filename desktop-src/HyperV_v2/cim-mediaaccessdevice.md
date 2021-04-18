---
description: Stellt ein Gerät dar, das Medien zum Speichern und Abrufen von Daten verwenden kann.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: CIM_MediaAccessDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351195"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a><span data-ttu-id="5a712-103">CIM_MediaAccessDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="5a712-103">CIM_MediaAccessDevice class (Hyper-V management)</span></span>

<span data-ttu-id="5a712-104">Stellt ein Gerät dar, das Medien zum Speichern und Abrufen von Daten verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="5a712-104">Represents a device that can use media to store and retrieve data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a712-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a712-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a><span data-ttu-id="5a712-106">Member</span><span class="sxs-lookup"><span data-stu-id="5a712-106">Members</span></span>

<span data-ttu-id="5a712-107">Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5a712-107">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5a712-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a712-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a712-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a712-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a712-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a712-110">Methods</span></span>

<span data-ttu-id="5a712-111">Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5a712-111">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="5a712-112">Methode</span><span class="sxs-lookup"><span data-stu-id="5a712-112">Method</span></span>                                               | <span data-ttu-id="5a712-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a712-113">Description</span></span>                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="5a712-114">**Lockmedia**</span><span class="sxs-lookup"><span data-stu-id="5a712-114">**LockMedia**</span></span>](cim-mediaaccessdevice-lockmedia.md) | <span data-ttu-id="5a712-115">Sperrt und entsperrt Wechselmedien in einem Medien Zugriffsgerät.</span><span class="sxs-lookup"><span data-stu-id="5a712-115">Locks and unlocks removable media in a media access device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5a712-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a712-116">Properties</span></span>

<span data-ttu-id="5a712-117">Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5a712-117">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a712-118">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="5a712-118">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-119">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="5a712-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a712-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-121">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "," MIF. DMTF-Host Datenträger \| \| 001,2 "," MIF. DMTF-Host Datenträger \| \| 001,4 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="5a712-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7", "MIF.DMTF\|Host Disk\|001.2", "MIF.DMTF\|Host Disk\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-122">Ein Array, das die Funktionen des Medien Zugriffs Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="5a712-122">An array that contains the capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a712-123">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5a712-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a712-124">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="5a712-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="5a712-125">**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="5a712-125">**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="5a712-126">**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="5a712-126">**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="5a712-127">**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="5a712-127">**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="5a712-128">**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="5a712-128">**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="5a712-129">**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="5a712-129">**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="5a712-130">**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="5a712-130">**Supports Removeable Media** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="5a712-131">**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="5a712-131">**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="5a712-132">**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="5a712-132">**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="5a712-133">**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="5a712-133">**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="5a712-134">**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="5a712-134">**Supports Dual Sided Media** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="5a712-135">**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="5a712-135">**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a712-136">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="5a712-136">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-137">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="5a712-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a712-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-139">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="5a712-139">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-140">Ein Array von Featurebeschreibungen für die Elemente im **Funktions Array.**</span><span class="sxs-lookup"><span data-stu-id="5a712-140">An array of feature descriptions for the items in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-141">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="5a712-141">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a712-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-144">Der Name des Algorithmus oder Tools, der vom Gerät verwendet wird, um die Komprimierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5a712-144">The name of the algorithm or tool used by the device to support compression.</span></span>

<span data-ttu-id="5a712-145">Wenn kein Komprimierungstyp angegeben ist, kann einer der folgenden Werte verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="5a712-145">If a compression type is not specified, one of the following values can be used:</span></span>

-   <span data-ttu-id="5a712-146">Die "unbekannte" Komprimierungs Unterstützung ist unbekannt oder nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="5a712-146">"Unknown"   compression support is unknown or not specified.</span></span>
-   <span data-ttu-id="5a712-147">Komprimierte Komprimierung wird unterstützt, aber der Typ ist unbekannt oder nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="5a712-147">"Compressed"   compression is supported but the type is unknown or unspecified.</span></span>
-   <span data-ttu-id="5a712-148">"Nicht komprimiert": das Gerät unterstützt keine Komprimierungs Funktionen.</span><span class="sxs-lookup"><span data-stu-id="5a712-148">"Not Compressed"   the device does not support compression capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-149">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="5a712-149">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-150">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-152">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="5a712-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-153">Die Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="5a712-153">The default block size, in bytes, for the device.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-154">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="5a712-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a712-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-157">Der Typ der Fehlererkennung und-Korrektur, der vom Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5a712-157">The type of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-158">**Lastbereinigt**</span><span class="sxs-lookup"><span data-stu-id="5a712-158">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-159">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a712-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-161">Das Datum und die Uhrzeit der letzten Bereinigung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="5a712-161">The date and time when the device was last cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-162">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="5a712-162">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-163">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-165">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="5a712-165">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-166">Die Zeit in Millisekunden, die das Gerät zum Lesen oder Schreiben eines Mediums benötigt, nachdem das Gerät geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="5a712-166">The time it takes, in milliseconds, for the device to be able to read or write a media after the device starts loading.</span></span> <span data-ttu-id="5a712-167">Beispielsweise ist dies das Intervall für Laufwerke zwischen einem Datenträger, der nicht auf die Festplatte zeigt, dass er für Lese-/Schreibvorgänge bereit ist.</span><span class="sxs-lookup"><span data-stu-id="5a712-167">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write operations.</span></span> <span data-ttu-id="5a712-168">Bei Bandlaufwerken beginnt dies, wenn Medien eingefügt werden und endet, wenn das Laufwerk meldet, dass es für eine Anwendung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="5a712-168">For tape drives, this starts when media is inserted and ends when the drive reports that it is ready for an application.</span></span> <span data-ttu-id="5a712-169">Dies erfolgt in der Regel am Anfang des Bands (bot).</span><span class="sxs-lookup"><span data-stu-id="5a712-169">This is usually at the tape's beginning-of-tape (BOT) area.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-170">**Maxaccesstime**</span><span class="sxs-lookup"><span data-stu-id="5a712-170">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-171">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-173">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="5a712-173">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-174">Die maximale Zugriffszeit des Mediums in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="5a712-174">The maximum access time of the media, in milliseconds.</span></span> <span data-ttu-id="5a712-175">Bei einem Laufwerk stellt dies eine vollständige Suche und eine vollständige Rotationsverzögerung dar.</span><span class="sxs-lookup"><span data-stu-id="5a712-175">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="5a712-176">Bei Bandlaufwerken stellt dies eine Suche zwischen dem Anfang des Bands und dem physisch entfernten Punkt dar.</span><span class="sxs-lookup"><span data-stu-id="5a712-176">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-177">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="5a712-177">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-178">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-180">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="5a712-180">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-181">Die maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="5a712-181">The maximum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-182">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="5a712-182">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-183">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-185">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| sequenzieller Zugriffsgeräte \| 001,2 "," MIF. DMTF-Host Datenträger \| \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5a712-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2", "MIF.DMTF\|Host Disk\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-186">Die maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="5a712-186">The maximum size, in kilobytes, of media supported by this device.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-187">**Maxunitionbeforecforec**</span><span class="sxs-lookup"><span data-stu-id="5a712-187">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-188">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-190">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Uni-Description**")</span><span class="sxs-lookup"><span data-stu-id="5a712-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-191">Die maximale Anzahl von Einheiten, die verwendet werden können, bevor das Gerät bereinigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a712-191">The maximum number of units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="5a712-192">**Unitdescription** definiert, wie der Typ der Einheit ist.</span><span class="sxs-lookup"><span data-stu-id="5a712-192">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-193">**Mediaislocked**</span><span class="sxs-lookup"><span data-stu-id="5a712-193">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-194">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5a712-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-196">**true** , wenn die Medien im Gerät gesperrt sind und nicht ausgewiesen werden können. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5a712-196">**true** if the media is locked in the device and can not be ejected; otherwise, **false**.</span></span> <span data-ttu-id="5a712-197">Bei nicht Wechsel Datenträgern sollte dieser Wert " **true**" lauten.</span><span class="sxs-lookup"><span data-stu-id="5a712-197">For non-removable devices, this value should be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-198">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="5a712-198">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-199">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-201">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="5a712-201">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-202">Die minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="5a712-202">The minimum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-203">**Mountcount**</span><span class="sxs-lookup"><span data-stu-id="5a712-203">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-204">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-206">Qualifizierer: **Counter**</span><span class="sxs-lookup"><span data-stu-id="5a712-206">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="5a712-207">Gibt an, wie oft Medien für die Datenübertragung bereitgestellt oder das Gerät bereinigt wurden.</span><span class="sxs-lookup"><span data-stu-id="5a712-207">The number of times that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="5a712-208">Wenn das Gerät Wechselmedien nicht unterstützt, sollte diese Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5a712-208">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-209">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="5a712-209">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-210">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5a712-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-212">" **true** ", wenn das Gerät bereinigt werden muss. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5a712-212">**true** if the device needs cleaning; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="5a712-213">Mit der Eigenschaft **Funktionen** wird angegeben, ob eine manuelle oder automatische Bereinigung möglich ist.</span><span class="sxs-lookup"><span data-stu-id="5a712-213">The **Capabilities** property indicates whether manual or automatic cleaning is possible.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a712-214">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="5a712-214">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-215">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a712-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-217">Wenn das Gerät mehrere einzelne Medien unterstützt, definiert diese Eigenschaft die maximale Zahl, die unterstützt oder eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a712-217">If the device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-218">**Security**</span><span class="sxs-lookup"><span data-stu-id="5a712-218">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-219">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a712-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-221">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF-Datenträger \| \| 003,22 ")</span><span class="sxs-lookup"><span data-stu-id="5a712-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Disks\|003.22")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-222">Die Betriebssicherheit für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="5a712-222">The operational security for the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a712-223">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="5a712-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a712-224">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="5a712-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5a712-225">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="5a712-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

<span data-ttu-id="5a712-226">Schreib **geschützt (4** )</span><span class="sxs-lookup"><span data-stu-id="5a712-226">**Read Only** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

<span data-ttu-id="5a712-227">**Gesperrt** (5)</span><span class="sxs-lookup"><span data-stu-id="5a712-227">**Locked Out** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="5a712-228">**Start Umgehung** (6)</span><span class="sxs-lookup"><span data-stu-id="5a712-228">**Boot Bypass** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

<span data-ttu-id="5a712-229">**Start Umgehung und** schreibgeschützt (7)</span><span class="sxs-lookup"><span data-stu-id="5a712-229">**Boot Bypass and Read Only** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a712-230">**Timeoflastmount**</span><span class="sxs-lookup"><span data-stu-id="5a712-230">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-231">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a712-231">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-233">Das letzte Datum und die Uhrzeit, zu der die Medien auf dem Gerät bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5a712-233">The most recent date and time when media was mounted on the device.</span></span> <span data-ttu-id="5a712-234">Diese Eigenschaft wird nur von Geräten verwendet, von denen Wechselmedien unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5a712-234">This property is only used by devices that support removable media.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-235">**Totalmounttime**</span><span class="sxs-lookup"><span data-stu-id="5a712-235">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-236">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-236">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a712-238">Die Zeit (in Sekunden), die für die Datenübertragung bereitgestellt wurde, oder zum Bereinigen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="5a712-238">The time, in seconds, that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="5a712-239">Wenn das Gerät Wechselmedien nicht unterstützt, sollte diese Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5a712-239">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-240">**Uncompresseddatarate**</span><span class="sxs-lookup"><span data-stu-id="5a712-240">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-241">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a712-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-243">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte pro Sekunde"), **Punit** ("Byte/Sekunde \* 10 ^ 3")</span><span class="sxs-lookup"><span data-stu-id="5a712-243">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes per Second"), **PUnit** ("byte / second \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-244">Die dauerhafte Datenübertragungsrate in Kilobyte, bei der das Gerät Lese-und Schreibvorgänge für ein Medium durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="5a712-244">The sustained data transfer rate in kilobytes at which the device can read and write to a media.</span></span> <span data-ttu-id="5a712-245">Dies ist eine dauerhafte, Rohdaten Rate.</span><span class="sxs-lookup"><span data-stu-id="5a712-245">This is a sustained, raw data rate.</span></span> <span data-ttu-id="5a712-246">Die maximale Anzahl von Raten oder Raten mit Komprimierung sollte in dieser Eigenschaft nicht gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="5a712-246">Maximum rates or rates with compression should not be reported in this property.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-247">**Unitydescription**</span><span class="sxs-lookup"><span data-stu-id="5a712-247">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a712-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-250">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Maxunitionbeforecforec"**,"**CIM \_ mediaaccessdevice**.**Unitsused**")</span><span class="sxs-lookup"><span data-stu-id="5a712-250">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM\_MediaAccessDevice**.**UnitsUsed**")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-251">Beschreibt den Einheitentyp der **maxunitbeforecforecund** **unitsused** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5a712-251">Describes the unit type of the **MaxUnitsBeforeCleaning** and **UnitsUsed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-252">**Unitsused**</span><span class="sxs-lookup"><span data-stu-id="5a712-252">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-253">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-253">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-255">Qualifizierer: [**Messgerät**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Unittdescription**","**CIM \_ mediaaccessdevice**.**Maxunitionbeforecforec"**)</span><span class="sxs-lookup"><span data-stu-id="5a712-255">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**", "**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-256">Die Anzahl der Einheiten, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a712-256">The number of units used by the device.</span></span> <span data-ttu-id="5a712-257">Diese Eigenschaft wird verwendet, um zu bestimmen, wann das Gerät bereinigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a712-257">This property is used to determine when the device should be cleaned.</span></span> <span data-ttu-id="5a712-258">**Unitdescription** definiert, wie der Typ der Einheit ist.</span><span class="sxs-lookup"><span data-stu-id="5a712-258">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="5a712-259">**Unloadtime**</span><span class="sxs-lookup"><span data-stu-id="5a712-259">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a712-260">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a712-260">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a712-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a712-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a712-262">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden"), **Punit** ("Second \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="5a712-262">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="5a712-263">Die Zeit in Millisekunden, die das Gerät vom lesen oder Schreiben von Medien zum Entladen wechseln soll.</span><span class="sxs-lookup"><span data-stu-id="5a712-263">The time it takes, in milliseconds, for the device to transition from reading or writing media to unloading.</span></span> <span data-ttu-id="5a712-264">Beispielsweise ist das Intervall für Datenträger Laufwerke das Intervall zwischen dem Drehen eines Datenträgers mit nominaler Geschwindigkeit und einem Datenträger, der nicht spinnt ist.</span><span class="sxs-lookup"><span data-stu-id="5a712-264">For example, for disk drives, this is the interval between a disk spinning at nominal speeds and a disk not spinning.</span></span> <span data-ttu-id="5a712-265">Bei Bandlaufwerken ist dies der Zeitpunkt, an dem ein Medium von seinem bot zum vollständigen ausstehen und zum Zugriff auf ein Auswahl Element oder einen menschlichen Operator wechselt.</span><span class="sxs-lookup"><span data-stu-id="5a712-265">For tape drives, this is the time for a media to go from its BOT to being fully ejected and accessible to a picker element or human operator.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a712-266">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a712-266">Requirements</span></span>



| <span data-ttu-id="5a712-267">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a712-267">Requirement</span></span> | <span data-ttu-id="5a712-268">Wert</span><span class="sxs-lookup"><span data-stu-id="5a712-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a712-269">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a712-269">Minimum supported client</span></span><br/> | <span data-ttu-id="5a712-270">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5a712-270">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5a712-271">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a712-271">Minimum supported server</span></span><br/> | <span data-ttu-id="5a712-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a712-272">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5a712-273">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a712-273">Namespace</span></span><br/>                | <span data-ttu-id="5a712-274">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5a712-274">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5a712-275">MOF</span><span class="sxs-lookup"><span data-stu-id="5a712-275">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a712-276"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5a712-276"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a712-277">DLL</span><span class="sxs-lookup"><span data-stu-id="5a712-277">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a712-278"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a712-278"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a712-279">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a712-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a712-280">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="5a712-280">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

