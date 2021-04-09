---
description: Stellt die Funktionen und die Verwaltungskapazität eines partitionierten Bereichs eines physischen Datenträgers auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Win32_DiskPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4f9a9c16f58d0119c8027848c481479985e7505e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861508"
---
# <a name="win32_diskpartition-class"></a><span data-ttu-id="f6445-103">Win32 \_ Diskpartition-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6445-103">Win32\_DiskPartition class</span></span>

<span data-ttu-id="f6445-104">Die **Win32 \_ Diskpartition** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Funktionen und die Verwaltungskapazität eines partitionierten Bereichs eines physischen Datenträgers auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-104">The **Win32\_DiskPartition** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a partitioned area of a physical disk on a computer system running Windows.</span></span> <span data-ttu-id="f6445-105">Beispiel: Datenträger \# 0, Partition \# 1.</span><span class="sxs-lookup"><span data-stu-id="f6445-105">Example: Disk \#0, Partition \#1.</span></span>

<span data-ttu-id="f6445-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6445-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f6445-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f6445-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6445-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6445-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a><span data-ttu-id="f6445-109">Member</span><span class="sxs-lookup"><span data-stu-id="f6445-109">Members</span></span>

<span data-ttu-id="f6445-110">Die **Win32 \_ Diskpartition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f6445-110">The **Win32\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="f6445-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f6445-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6445-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6445-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6445-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="f6445-113">Methods</span></span>

<span data-ttu-id="f6445-114">Die **Win32 \_ Diskpartition** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f6445-114">The **Win32\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="f6445-115">Methode</span><span class="sxs-lookup"><span data-stu-id="f6445-115">Method</span></span>                                                     | <span data-ttu-id="f6445-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6445-116">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6445-117">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="f6445-117">**Reset**</span></span>](win32-diskpartition-reset.md)                 | <span data-ttu-id="f6445-118">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f6445-118">Requests a reset of the logical device.</span></span><br/>                                                            |
| [<span data-ttu-id="f6445-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f6445-119">**SetPowerState**</span></span>](win32-diskpartition-setpowerstate.md) | <span data-ttu-id="f6445-120">Legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6445-120">Sets the desired power state for a logical device and when a device should be put into that state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f6445-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6445-121">Properties</span></span>

<span data-ttu-id="f6445-122">Die **Win32 \_ Diskpartition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6445-122">The **Win32\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6445-123">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="f6445-123">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-124">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6445-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-126">Der Medien Zugriff ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6445-126">Media access available.</span></span>

<span data-ttu-id="f6445-127">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-127">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6445-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f6445-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="f6445-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="f6445-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="f6445-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="f6445-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-131">Schreibbar</span><span class="sxs-lookup"><span data-stu-id="f6445-131">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="f6445-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="f6445-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="f6445-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="f6445-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6445-134">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="f6445-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-135">Datentyp: **unit16**</span><span class="sxs-lookup"><span data-stu-id="f6445-135">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-136">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-136">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-137">Zusätzliche Verfügbarkeit und Status des Geräts, über das hinaus, das in der Availability-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f6445-137">Additional availability and status of the Device, beyond that specified in the Availability property.</span></span> <span data-ttu-id="f6445-138">Die **Availability** -Eigenschaft gibt den primären Status und die Verfügbarkeit des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f6445-138">The **Availability** property denotes the primary status and availability of the Device.</span></span> <span data-ttu-id="f6445-139">In einigen Fällen reicht dies nicht aus, um den gesamten Status des Geräts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f6445-139">In some cases, this will not be sufficient to denote the complete status of the Device.</span></span> <span data-ttu-id="f6445-140">In diesen Fällen kann die **additionalavailability** -Eigenschaft verwendet werden, um weitere Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f6445-140">In those cases, the **AdditionalAvailability** property can be used to provide further information.</span></span> <span data-ttu-id="f6445-141">Beispielsweise ist die primäre **Verfügbarkeit** eines Geräts möglicherweise offline (Wert = 8), kann sich aber auch in einem niedrigen Energiezustand (**additonalavailability** Value = 14) befinden, oder das Gerät kann die Diagnose (**additionalavailability** Value = 5, in Test) ausführen. "</span><span class="sxs-lookup"><span data-stu-id="f6445-141">For example, a Device's primary **Availability** may be Off line (value=8), but it may also be in a low power state (**AdditonalAvailability** value=14), or the Device could be running Diagnostics (**AdditionalAvailability** value=5, In Test)."</span></span>

<span data-ttu-id="f6445-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6445-143">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f6445-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6445-144">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f6445-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f6445-145">**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="f6445-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f6445-146">**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="f6445-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f6445-147">**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="f6445-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f6445-148">**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="f6445-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f6445-149">**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="f6445-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f6445-150">**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="f6445-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f6445-151">**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f6445-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f6445-152">Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="f6445-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f6445-153">**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="f6445-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f6445-154">**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="f6445-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f6445-155">**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="f6445-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f6445-156">**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="f6445-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f6445-157">**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f6445-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f6445-158">**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="f6445-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f6445-159">**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="f6445-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f6445-160">**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="f6445-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f6445-161">**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="f6445-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f6445-162">**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="f6445-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f6445-163">Still **legung (21** )</span><span class="sxs-lookup"><span data-stu-id="f6445-163">**Quiesce** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6445-164">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="f6445-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6445-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-167">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="f6445-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-168">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f6445-168">Availability and status of the device.</span></span>

<span data-ttu-id="f6445-169">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-169">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6445-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f6445-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6445-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f6445-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f6445-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="f6445-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f6445-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="f6445-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f6445-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="f6445-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f6445-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="f6445-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f6445-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="f6445-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f6445-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="f6445-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f6445-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f6445-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f6445-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="f6445-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f6445-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="f6445-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f6445-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="f6445-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f6445-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="f6445-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-183">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f6445-183">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f6445-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="f6445-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-185">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f6445-185">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f6445-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f6445-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-187">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-187">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f6445-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="f6445-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f6445-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="f6445-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-190">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="f6445-190">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f6445-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="f6445-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-192">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="f6445-192">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f6445-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="f6445-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-194">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="f6445-194">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f6445-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="f6445-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-196">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f6445-196">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f6445-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="f6445-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-198">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="f6445-198">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6445-199">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="f6445-199">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-200">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-202">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="f6445-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-203">Größe in Byte der Blöcke, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="f6445-203">Size in bytes of the blocks which form this storage extent.</span></span> <span data-ttu-id="f6445-204">Wenn unbekannt oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 ein.</span><span class="sxs-lookup"><span data-stu-id="f6445-204">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="f6445-205">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f6445-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f6445-206">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-207">**Startbare**</span><span class="sxs-lookup"><span data-stu-id="f6445-207">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-208">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-210">Gibt an, ob der Computer von dieser Partition gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6445-210">Indicates whether the computer can be booted from this partition.</span></span>

<span data-ttu-id="f6445-211">Diese Eigenschaft wird von [**CIM \_ Diskpartition**](cim-diskpartition.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-211">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-212">**Bootpartition**</span><span class="sxs-lookup"><span data-stu-id="f6445-212">**BootPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-213">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-215">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| Infofile")</span><span class="sxs-lookup"><span data-stu-id="f6445-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-216">Partition ist die aktive Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-216">Partition is the active partition.</span></span> <span data-ttu-id="f6445-217">Das Betriebssystem verwendet die aktive Partition beim Starten von einer Festplatte.</span><span class="sxs-lookup"><span data-stu-id="f6445-217">The operating system uses the active partition when booting from a hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="f6445-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f6445-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-219">Datentyp: **String.**</span><span class="sxs-lookup"><span data-stu-id="f6445-219">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-221">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f6445-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-222">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f6445-222">Short description of the object.</span></span>

<span data-ttu-id="f6445-223">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-224">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="f6445-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-225">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6445-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-227">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f6445-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-228">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f6445-228">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="f6445-229">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f6445-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="f6445-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f6445-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="f6445-231">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-232">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f6445-232">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f6445-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="f6445-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f6445-234">(1)</span><span class="sxs-lookup"><span data-stu-id="f6445-234">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f6445-235">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f6445-235">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6445-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="f6445-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f6445-237">(2)</span><span class="sxs-lookup"><span data-stu-id="f6445-237">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f6445-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="f6445-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f6445-239">(3)</span><span class="sxs-lookup"><span data-stu-id="f6445-239">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f6445-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f6445-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f6445-241">(4)</span><span class="sxs-lookup"><span data-stu-id="f6445-241">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f6445-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="f6445-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f6445-243">(5)</span><span class="sxs-lookup"><span data-stu-id="f6445-243">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f6445-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="f6445-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f6445-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="f6445-245">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f6445-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6445-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f6445-247">(7)</span><span class="sxs-lookup"><span data-stu-id="f6445-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f6445-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="f6445-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f6445-249">(8)</span><span class="sxs-lookup"><span data-stu-id="f6445-249">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f6445-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="f6445-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f6445-251">(9)</span><span class="sxs-lookup"><span data-stu-id="f6445-251">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f6445-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="f6445-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f6445-253">(10)</span><span class="sxs-lookup"><span data-stu-id="f6445-253">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f6445-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="f6445-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f6445-255">(11)</span><span class="sxs-lookup"><span data-stu-id="f6445-255">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f6445-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="f6445-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f6445-257">(12)</span><span class="sxs-lookup"><span data-stu-id="f6445-257">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f6445-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="f6445-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f6445-259">(13)</span><span class="sxs-lookup"><span data-stu-id="f6445-259">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f6445-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="f6445-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f6445-261">(14)</span><span class="sxs-lookup"><span data-stu-id="f6445-261">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f6445-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="f6445-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f6445-263">(15)</span><span class="sxs-lookup"><span data-stu-id="f6445-263">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f6445-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="f6445-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f6445-265">(16)</span><span class="sxs-lookup"><span data-stu-id="f6445-265">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f6445-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="f6445-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f6445-267">(17)</span><span class="sxs-lookup"><span data-stu-id="f6445-267">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6445-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="f6445-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f6445-269">(18)</span><span class="sxs-lookup"><span data-stu-id="f6445-269">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f6445-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="f6445-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f6445-271">(19)</span><span class="sxs-lookup"><span data-stu-id="f6445-271">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f6445-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f6445-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f6445-273">(20)</span><span class="sxs-lookup"><span data-stu-id="f6445-273">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f6445-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="f6445-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f6445-275">(21)</span><span class="sxs-lookup"><span data-stu-id="f6445-275">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f6445-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f6445-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f6445-277">(22)</span><span class="sxs-lookup"><span data-stu-id="f6445-277">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f6445-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="f6445-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f6445-279">(23)</span><span class="sxs-lookup"><span data-stu-id="f6445-279">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f6445-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="f6445-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f6445-281">(24)</span><span class="sxs-lookup"><span data-stu-id="f6445-281">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f6445-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f6445-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f6445-283">(25)</span><span class="sxs-lookup"><span data-stu-id="f6445-283">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f6445-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f6445-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f6445-285">(26)</span><span class="sxs-lookup"><span data-stu-id="f6445-285">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f6445-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="f6445-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f6445-287">(27)</span><span class="sxs-lookup"><span data-stu-id="f6445-287">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f6445-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="f6445-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f6445-289">(28)</span><span class="sxs-lookup"><span data-stu-id="f6445-289">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f6445-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="f6445-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f6445-291">(29)</span><span class="sxs-lookup"><span data-stu-id="f6445-291">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f6445-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="f6445-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f6445-293">(30)</span><span class="sxs-lookup"><span data-stu-id="f6445-293">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6445-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="f6445-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f6445-295">31,5</span><span class="sxs-lookup"><span data-stu-id="f6445-295">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6445-296">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="f6445-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-297">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-299">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f6445-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-300">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6445-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f6445-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-302">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f6445-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-303">Datentyp: **String.**</span><span class="sxs-lookup"><span data-stu-id="f6445-303">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-305">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6445-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6445-306">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f6445-307">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-307">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f6445-308">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-309">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6445-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-312">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f6445-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-313">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f6445-313">Description of the object.</span></span>

<span data-ttu-id="f6445-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f6445-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-318">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f6445-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-319">Eindeutiger Bezeichner des Laufwerks und der Partition vom Rest des Systems.</span><span class="sxs-lookup"><span data-stu-id="f6445-319">Unique identifier of the disk drive and partition, from the rest of the system.</span></span>

</dd> <dt>

<span data-ttu-id="f6445-320">**DiskIndex**</span><span class="sxs-lookup"><span data-stu-id="f6445-320">**DiskIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-321">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6445-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-323">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| Infofile")</span><span class="sxs-lookup"><span data-stu-id="f6445-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-324">Index Nummer des Datenträgers, der diese Partition enthält.</span><span class="sxs-lookup"><span data-stu-id="f6445-324">Index number of the disk containing this partition.</span></span>

<span data-ttu-id="f6445-325">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="f6445-325">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="f6445-326">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="f6445-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-327">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-329">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-329">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="f6445-330">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f6445-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-332">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-334">Informationen über den Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="f6445-334">Information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="f6445-335">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-336">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="f6445-336">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-339">Typ der Fehlererkennung und-Korrektur, der von diesem Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-339">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="f6445-340">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-340">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-341">**Hiddensektoren**</span><span class="sxs-lookup"><span data-stu-id="f6445-341">**HiddenSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-342">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6445-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-344">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span><span class="sxs-lookup"><span data-stu-id="f6445-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-345">Anzahl der ausgeblendeten Sektoren in der Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-345">Number of hidden sectors in the partition.</span></span>

<span data-ttu-id="f6445-346">Beispiel: 63</span><span class="sxs-lookup"><span data-stu-id="f6445-346">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="f6445-347">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f6445-347">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-348">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f6445-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6445-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-350">Ein Array von frei Form Zeichenfolgen, das Erläuterungen und Details hinter den Einträgen im "OtherIdentifyingInfo"-Array bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f6445-350">An array of free-form strings providing explanations and details behind the entries in the OtherIdentifyingInfo array.</span></span> <span data-ttu-id="f6445-351">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag in "OtherIdentifyingInfo" verknüpft ist, der sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="f6445-351">Note, each entry of this array is related to the entry in OtherIdentifyingInfo that is located at the same index.</span></span>

<span data-ttu-id="f6445-352">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-353">**Index**</span><span class="sxs-lookup"><span data-stu-id="f6445-353">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-354">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6445-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-356">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f6445-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-357">Index Nummer der Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-357">Index number of the partition.</span></span>

<span data-ttu-id="f6445-358">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="f6445-358">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="f6445-359">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f6445-359">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-360">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f6445-360">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-362">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f6445-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-363">Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f6445-363">Date the object was installed.</span></span> <span data-ttu-id="f6445-364">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f6445-364">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f6445-365">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-366">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f6445-366">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-367">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6445-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-369">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f6445-369">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f6445-370">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-371">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="f6445-371">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-372">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-372">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-374">Qualifizierer **: entfernt**</span><span class="sxs-lookup"><span data-stu-id="f6445-374">Qualifiers: **Depricated**</span></span>
</dt> </dl>

<span data-ttu-id="f6445-375">Maximale Zeit in Millisekunden, die ein Gerät in einem versetzen-Zustand ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6445-375">Maximum time in milliseconds, that a Device can run in a Quiesced state.</span></span> <span data-ttu-id="f6445-376">Der Status eines Geräts wird in den Eigenschaften "Availability" und "additionalavailability" definiert, bei denen der Wert "21" übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-376">A Device's state is defined in its Availability and AdditionalAvailability properties, where Quiesced is conveyed by the value 21.</span></span> <span data-ttu-id="f6445-377">Was am Ende des Zeitraums geschieht, ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="f6445-377">What occurs at the end of the time limit is device-specific.</span></span> <span data-ttu-id="f6445-378">Das Gerät kann nicht stillgelegt werden, kann offline geschaltet werden oder andere Aktionen durchführen.</span><span class="sxs-lookup"><span data-stu-id="f6445-378">The Device may unquiesce, may offline or take other action.</span></span> <span data-ttu-id="f6445-379">Der Wert 0 gibt an, dass ein Gerät unbegrenzt inaktiv bleiben kann.</span><span class="sxs-lookup"><span data-stu-id="f6445-379">A value of 0 indicates that a Device can remain quiesced indefinitely.</span></span>

> [!Note]
>
> <span data-ttu-id="f6445-380">"Die maxquiescetime-Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="f6445-380">"The MaxQuiesceTime property has been deprecated.</span></span> <span data-ttu-id="f6445-381">Bei der Auswertung der Verwendung von inesce wurde festgestellt, dass diese einzelne Eigenschaft nicht ausreichend ist, um zu beschreiben, wann ein Gerät automatisch einen inaktiven Zustand verlässt.</span><span class="sxs-lookup"><span data-stu-id="f6445-381">When evaluating the use of Quiesce, it was determine that this single property is not adequate for describing when a device will automatically exit a quiescent state.</span></span> <span data-ttu-id="f6445-382">Das wahrscheinlichste Szenario für ein Gerät, das einen inaktiven Zustand beendet, wurde so bestimmt, dass es auf der Anzahl der ausstehenden Anforderungen in der Warteschlange und nicht auf einer maximalen Zeit basiert.</span><span class="sxs-lookup"><span data-stu-id="f6445-382">In fact, the most likely scenario for a device to exit a quiescent state was determined to be based on the number of outstanding requests queued rather than on a maximum time.</span></span> <span data-ttu-id="f6445-383">Diese wird erneut ausgewertet und später neu positioniert.</span><span class="sxs-lookup"><span data-stu-id="f6445-383">This will be re-evaluated and repositioned later.</span></span> <span data-ttu-id="f6445-384">\\n</span><span class="sxs-lookup"><span data-stu-id="f6445-384">\\n</span></span>

 

<span data-ttu-id="f6445-385">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-386">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6445-386">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-389">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f6445-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-390">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f6445-390">Label by which the object is known.</span></span> <span data-ttu-id="f6445-391">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-391">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="f6445-392">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-393">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="f6445-393">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-394">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-396">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="f6445-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-397">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="f6445-397">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="f6445-398">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-398">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="f6445-399">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="f6445-399">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="f6445-400">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f6445-400">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f6445-401">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f6445-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-403">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-405">Array, das zusätzliche Daten erfasst, die über DeviceID-Informationen hinausgehen und zum Identifizieren eines LogicalDevice verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="f6445-405">Array that captures additional data, beyond DeviceID information, that could be used to identify a LogicalDevice.</span></span> <span data-ttu-id="f6445-406">Ein Beispiel wäre, den benutzerfreundlichen Namen des Betriebssystems für das Gerät in dieser Eigenschaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f6445-406">One example would be to hold the Operating System's user friendly name for the Device in this property.</span></span> <span data-ttu-id="f6445-407">Die maximale Länge beträgt 256.</span><span class="sxs-lookup"><span data-stu-id="f6445-407">Maximum length is 256.</span></span>

<span data-ttu-id="f6445-408">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-409">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f6445-409">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-410">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-412">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f6445-412">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-413">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f6445-413">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f6445-414">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f6445-414">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f6445-415">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-416">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f6445-416">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-417">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f6445-417">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6445-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-419">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f6445-419">Indicates the specific power-related capabilities of the logical device.</span></span> <span data-ttu-id="f6445-420">Die Array Werte 0 = "unknown", 1 = "nicht unterstützt" und 2 = "deaktiviert" sind selbsterklärend.</span><span class="sxs-lookup"><span data-stu-id="f6445-420">The array values, 0="Unknown", 1="Not Supported" and 2="Disabled" are self-explanatory.</span></span> <span data-ttu-id="f6445-421">Der Wert 3 = "aktiviert" zeigt an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, aber der genaue Featuresatz unbekannt ist oder die Informationen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f6445-421">The value, 3="Enabled" indicates that the power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span> <span data-ttu-id="f6445-422">"Automatisch eingegebene Energiespar Modi" (4) beschreibt, dass ein Gerät seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern kann.</span><span class="sxs-lookup"><span data-stu-id="f6445-422">"Power Saving Modes Entered Automatically" (4) describes that a device can change its power state based on usage or other criteria.</span></span> <span data-ttu-id="f6445-423">"Energie Zustands feststellbar" (5) gibt an, dass die SetPowerState-Methode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-423">"Power State Settable" (5) indicates that the SetPowerState method is supported.</span></span> <span data-ttu-id="f6445-424">"Power Cycle supported" (6) gibt an, dass die SetPowerState-Methode aufgerufen werden kann, wenn die PowerState-Eingabe Variable auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="f6445-424">"Power Cycling Supported" (6) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle").</span></span> <span data-ttu-id="f6445-425">"Getaktete Stromversorgung unterstützt" (7) gibt an, dass die SetPowerState-Methode aufgerufen werden kann, wenn die PowerState-Eingabe Variable auf 5 ("Power Cycle") festgelegt ist und der Zeitparameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f6445-425">"Timed Power On Supported" (7) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle") and the Time parameter set to a specific date and time, or interval, for power-on.</span></span>

<span data-ttu-id="f6445-426">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6445-427">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f6445-427">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f6445-428">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="f6445-428">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f6445-429">**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="f6445-429">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f6445-430">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f6445-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f6445-431">**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="f6445-431">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f6445-432">**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="f6445-432">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f6445-433">**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="f6445-433">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f6445-434">**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="f6445-434">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6445-435">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="f6445-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-436">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-438">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="f6445-438">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="f6445-439">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f6445-439">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="f6445-440">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-441">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="f6445-441">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-442">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-444">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="f6445-444">The number of consecutive hours that this Device has been powered, since its last power cycle.</span></span>

<span data-ttu-id="f6445-445">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-446">**Primäre Partition**</span><span class="sxs-lookup"><span data-stu-id="f6445-446">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-447">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-447">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-449">**True** gibt an, dass es sich hierbei um die primäre Partition handelt.</span><span class="sxs-lookup"><span data-stu-id="f6445-449">If **True**, this is the primary partition.</span></span>

<span data-ttu-id="f6445-450">Diese Eigenschaft wird von [**CIM \_ Diskpartition**](cim-diskpartition.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-450">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-451">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="f6445-451">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-452">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-454">Die Beschreibung der Medien und deren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="f6445-454">Description of the media and its use.</span></span>

<span data-ttu-id="f6445-455">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-455">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-456">**Rescriptepartition**</span><span class="sxs-lookup"><span data-stu-id="f6445-456">**RewritePartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-457">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-459">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Partition \_ Information**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| Rewrite Partition")</span><span class="sxs-lookup"><span data-stu-id="f6445-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RewritePartition")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-460">**True** gibt an, dass die Partitionsinformationen geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="f6445-460">If **True**, the partition information has changed.</span></span> <span data-ttu-id="f6445-461">Wenn Sie eine Partition (mit [**IOCTL \_ Disk \_ Set \_ \_ Layout Layout**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)) ändern, verwendet das System diese Eigenschaft, um zu bestimmen, welche Partitionen geändert wurden und dass Ihre Informationen umgeschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f6445-461">When you change a partition (with [**IOCTL\_DISK\_SET\_DRIVE\_LAYOUT**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), the system uses this property to determine which partitions have changed and need their information rewritten.</span></span> <span data-ttu-id="f6445-462">**True** gibt an, dass die Partition umgeschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="f6445-462">If **TRUE**, the partition must be rewritten.</span></span>

</dd> <dt>

<span data-ttu-id="f6445-463">**Größe**</span><span class="sxs-lookup"><span data-stu-id="f6445-463">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-464">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-466">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| Infofile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="f6445-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-467">Die Gesamtgröße der Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-467">Total size of the partition.</span></span>

<span data-ttu-id="f6445-468">Beispiel: 1059045376</span><span class="sxs-lookup"><span data-stu-id="f6445-468">Example: 1059045376</span></span>

<span data-ttu-id="f6445-469">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f6445-469">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-470">**Startingoffset**</span><span class="sxs-lookup"><span data-stu-id="f6445-470">**StartingOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-471">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-473">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| Infofile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="f6445-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-474">Start Offset (in Bytes) der Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-474">Starting offset (in bytes) of the partition.</span></span>

<span data-ttu-id="f6445-475">Beispiel: 32256</span><span class="sxs-lookup"><span data-stu-id="f6445-475">Example: 32256</span></span>

<span data-ttu-id="f6445-476">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f6445-476">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-477">**Status**</span><span class="sxs-lookup"><span data-stu-id="f6445-477">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-478">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-479">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-480">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f6445-480">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-481">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f6445-481">Current status of the object.</span></span> <span data-ttu-id="f6445-482">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-482">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f6445-483">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="f6445-483">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f6445-484">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="f6445-484">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f6445-485">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-485">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f6445-486">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f6445-486">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f6445-487">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-487">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f6445-488">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f6445-488">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f6445-489">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f6445-489">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f6445-490">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f6445-490">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f6445-491">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f6445-491">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6445-492">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f6445-492">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f6445-493">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f6445-493">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f6445-494">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f6445-494">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f6445-495">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f6445-495">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f6445-496">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f6445-496">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f6445-497">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f6445-497">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f6445-498">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f6445-498">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f6445-499">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f6445-499">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f6445-500">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f6445-500">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6445-501">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f6445-501">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-502">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6445-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-503">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-504">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f6445-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-505">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f6445-505">State of the logical device.</span></span> <span data-ttu-id="f6445-506">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-506">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="f6445-507">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6445-508">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f6445-508">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6445-509">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f6445-509">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f6445-510">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f6445-510">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f6445-511">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="f6445-511">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f6445-512">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="f6445-512">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6445-513">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f6445-513">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-514">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-515">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-516">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6445-516">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6445-517">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f6445-517">Creation class name of the scoping system.</span></span>

<span data-ttu-id="f6445-518">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-518">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-519">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f6445-519">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-520">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-521">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-522">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6445-522">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6445-523">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f6445-523">Name of the scoping system.</span></span>

<span data-ttu-id="f6445-524">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-525">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="f6445-525">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-526">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6445-526">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-527">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6445-528">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="f6445-528">The total number of hours that this device has been powered.</span></span>

<span data-ttu-id="f6445-529">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f6445-529">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6445-530">**Type**</span><span class="sxs-lookup"><span data-stu-id="f6445-530">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6445-531">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6445-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6445-532">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6445-532">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6445-533">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| partitionrecord \| dwpartitiontype")</span><span class="sxs-lookup"><span data-stu-id="f6445-533">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|PartitionRecord\|dwPartitionType")</span></span>
</dt> </dl>

<span data-ttu-id="f6445-534">Der Typ der Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-534">Type of the partition.</span></span>

<span data-ttu-id="f6445-535">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f6445-535">The values are:</span></span>

<dl> <dd><span data-ttu-id="f6445-536">Genutzt</span><span class="sxs-lookup"><span data-stu-id="f6445-536">"Unused"</span></span></dd> <dd><span data-ttu-id="f6445-537">"12-Bit-FAT"</span><span class="sxs-lookup"><span data-stu-id="f6445-537">"12-bit FAT"</span></span></dd> <dd><span data-ttu-id="f6445-538">"XENIX Type 1"</span><span class="sxs-lookup"><span data-stu-id="f6445-538">"Xenix Type 1"</span></span></dd> <dd><span data-ttu-id="f6445-539">"XENIX Type 2"</span><span class="sxs-lookup"><span data-stu-id="f6445-539">"Xenix Type 2"</span></span></dd> <dd><span data-ttu-id="f6445-540">"16-Bit-FAT"</span><span class="sxs-lookup"><span data-stu-id="f6445-540">"16-bit FAT"</span></span></dd> <dd><span data-ttu-id="f6445-541">"Erweiterte Partition"</span><span class="sxs-lookup"><span data-stu-id="f6445-541">"Extended Partition"</span></span></dd> <dd><span data-ttu-id="f6445-542">"MS-DOS V4 groß"</span><span class="sxs-lookup"><span data-stu-id="f6445-542">"MS-DOS V4 Huge"</span></span></dd> <dd><span data-ttu-id="f6445-543">"Installier bares Datei System"</span><span class="sxs-lookup"><span data-stu-id="f6445-543">"Installable File System"</span></span></dd> <dd><span data-ttu-id="f6445-544">"PowerPC Reference Platform"</span><span class="sxs-lookup"><span data-stu-id="f6445-544">"PowerPC Reference Platform"</span></span></dd> <dd><span data-ttu-id="f6445-545">UNIX</span><span class="sxs-lookup"><span data-stu-id="f6445-545">"UNIX"</span></span></dd> <dd><span data-ttu-id="f6445-546">NTFS</span><span class="sxs-lookup"><span data-stu-id="f6445-546">"NTFS"</span></span></dd> <dd><span data-ttu-id="f6445-547">"Win95 w/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="f6445-547">"Win95 w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="f6445-548">"Extended w/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="f6445-548">"Extended w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="f6445-549">"Logischer Datenträger-Manager"</span><span class="sxs-lookup"><span data-stu-id="f6445-549">"Logical Disk Manager"</span></span></dd> <dd><span data-ttu-id="f6445-550">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="f6445-550">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

<span data-ttu-id="f6445-551">Nicht **verwendet** ("nicht verwendet")</span><span class="sxs-lookup"><span data-stu-id="f6445-551">**Unused** ("Unused")</span></span>


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

<span data-ttu-id="f6445-552">**12-Bit-FAT** ("12-Bit-FAT")</span><span class="sxs-lookup"><span data-stu-id="f6445-552">**12-bit FAT** ("12-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

<span data-ttu-id="f6445-553">**XENIX Type 1** ("XENIX Type 1")</span><span class="sxs-lookup"><span data-stu-id="f6445-553">**Xenix Type 1** ("Xenix Type 1")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

<span data-ttu-id="f6445-554">**XENIX Type 2** ("XENIX Type 2")</span><span class="sxs-lookup"><span data-stu-id="f6445-554">**Xenix Type 2** ("Xenix Type 2")</span></span>


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

<span data-ttu-id="f6445-555">**16-Bit-FAT** ("16-Bit-FAT")</span><span class="sxs-lookup"><span data-stu-id="f6445-555">**16-bit FAT** ("16-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

<span data-ttu-id="f6445-556">**Erweiterte Partition** ("erweiterte Partition")</span><span class="sxs-lookup"><span data-stu-id="f6445-556">**Extended Partition** ("Extended Partition")</span></span>


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

<span data-ttu-id="f6445-557">**MS-DOS-groß** ("MS-DOS V4-groß")</span><span class="sxs-lookup"><span data-stu-id="f6445-557">**MS-DOS V4 Huge** ("MS-DOS V4 Huge")</span></span>


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

<span data-ttu-id="f6445-558">**Installier bares Dateisystem** ("installier bares Dateisystem")</span><span class="sxs-lookup"><span data-stu-id="f6445-558">**Installable File System** ("Installable File System")</span></span>


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

<span data-ttu-id="f6445-559">**PowerPC-Referenzplattform** ("PowerPC-Referenzplattform")</span><span class="sxs-lookup"><span data-stu-id="f6445-559">**PowerPC Reference Platform** ("PowerPC Reference Platform")</span></span>


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

<span data-ttu-id="f6445-560">**UNIX** ("Unix")</span><span class="sxs-lookup"><span data-stu-id="f6445-560">**UNIX** ("UNIX")</span></span>


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

<span data-ttu-id="f6445-561">**NTFS** ("NTFS")</span><span class="sxs-lookup"><span data-stu-id="f6445-561">**NTFS** ("NTFS")</span></span>


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

<span data-ttu-id="f6445-562">**Win95 w/Extended int 13** ("Win95 w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="f6445-562">**Win95 w/Extended Int 13** ("Win95 w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

<span data-ttu-id="f6445-563">**Extended w/Extended int 13** ("Extended w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="f6445-563">**Extended w/Extended Int 13** ("Extended w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

<span data-ttu-id="f6445-564">**Logical Disk Manager** ("logischer Datenträger-Manager")</span><span class="sxs-lookup"><span data-stu-id="f6445-564">**Logical Disk Manager** ("Logical Disk Manager")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6445-565">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f6445-565">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="f6445-566"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f6445-566"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f6445-567">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6445-567">Remarks</span></span>

<span data-ttu-id="f6445-568">Die **Win32 \_ Diskpartition** -Klasse wird von [**CIM \_ Diskpartition**](cim-diskpartition.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f6445-568">The **Win32\_DiskPartition** class is derived from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

<span data-ttu-id="f6445-569">Eine Partition ist eine strukturelle Division eines physischen Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="f6445-569">A partition is a structural division of a physical disk drive.</span></span> <span data-ttu-id="f6445-570">Obwohl ein Laufwerk eine einzelne Partition enthalten kann, sind größere Volumes häufig in mehrere Partitionen unterteilt.</span><span class="sxs-lookup"><span data-stu-id="f6445-570">Although a drive can contain a single partition, larger volumes are often divided into multiple partitions.</span></span> <span data-ttu-id="f6445-571">Daher haben Sie möglicherweise die Laufwerke C, D und E, auch wenn Ihr Computer nur über eine einzige physische Festplatte verfügt.</span><span class="sxs-lookup"><span data-stu-id="f6445-571">This is why you might have drives C, D, and E even though your computer has only a single physical hard disk.</span></span>

<span data-ttu-id="f6445-572">Windows unterstützt die folgenden Partitionstypen:</span><span class="sxs-lookup"><span data-stu-id="f6445-572">Windows supports the following partition types:</span></span>

-   <span data-ttu-id="f6445-573">Primäre Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-573">Primary partition.</span></span> <span data-ttu-id="f6445-574">Dies ist der einzige Typ der Partition, auf dem ein Betriebssystem installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6445-574">This is the only type of partition that can have an operating system installed.</span></span> <span data-ttu-id="f6445-575">Jedes Laufwerk kann über bis zu vier primäre Partitionen verfügen, von denen jeder einen anderen Laufwerk Buchstaben zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="f6445-575">Each drive can have as many as four primary partitions, each assigned a different drive letter.</span></span>
-   <span data-ttu-id="f6445-576">Erweiterte Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-576">Extended partition.</span></span> <span data-ttu-id="f6445-577">Eine zusätzliche Partition, die in mehrere logische Laufwerke unterteilt werden kann, wobei jedem ein eindeutiger Laufwerk Buchstabe zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-577">An additional partition that can be subdivided into multiple logical drives, each assigned a unique drive letter.</span></span> <span data-ttu-id="f6445-578">Ein Laufwerk kann nur über eine erweiterte Partition verfügen. Sie können diese Partition jedoch auf mehrere logische Laufwerke aufteilen.</span><span class="sxs-lookup"><span data-stu-id="f6445-578">A drive can have only one extended partition; however, you can divide this partition into multiple logical drives.</span></span> <span data-ttu-id="f6445-579">Dadurch kann ein Datenträger mehr als nur die vier zulässigen primären Partitionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f6445-579">This enables a disk to have more than just the four allowed primary partitions.</span></span>
-   <span data-ttu-id="f6445-580">System Partition.</span><span class="sxs-lookup"><span data-stu-id="f6445-580">System partition.</span></span> <span data-ttu-id="f6445-581">Alle primären Partitionen, die ein Betriebssystem enthalten.</span><span class="sxs-lookup"><span data-stu-id="f6445-581">Any primary partition containing an operating system.</span></span>

<span data-ttu-id="f6445-582">Partitionen können Ihnen mitteilen, wie ein physisches Laufwerk tatsächlich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6445-582">Partitions can tell you how a physical disk drive is actually being used.</span></span> <span data-ttu-id="f6445-583">Wenn Sie die physischen Partitionen auf einem Datenträger untersuchen, können Sie die folgenden Arten von Elementen ermitteln:</span><span class="sxs-lookup"><span data-stu-id="f6445-583">By examining the physical partitions on a disk, you can determine the following types of things:</span></span>

-   <span data-ttu-id="f6445-584">Gibt an, wie der Datenträger in logische Laufwerke aufgeteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="f6445-584">How the disk has been divided into logical drives.</span></span>
-   <span data-ttu-id="f6445-585">Wenn nicht partitionierter Speicherplatz auf dem Datenträger verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f6445-585">If there is unpartitioned space available on the disk.</span></span> <span data-ttu-id="f6445-586">Dies kann durch Subtraktion der Größe aller Partitionen auf einem Datenträger von der Größe des Datenträgers bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-586">This can be determined by subtracting the size of all the partitions on a disk from the size of the disk itself.</span></span>
-   <span data-ttu-id="f6445-587">Wenn Sie den Computer von diesem Datenträger aus starten können (d. h., der Datenträger enthält eine Start Partition).</span><span class="sxs-lookup"><span data-stu-id="f6445-587">If you can boot the computer from that disk (that is, does the disk contain a boot partition).</span></span>

<span data-ttu-id="f6445-588">Alle diese Fragen können mithilfe der Win32-Klasse **\_ Diskpartition** aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f6445-588">All these questions can be resolved by using the **Win32\_DiskPartition** class.</span></span>

## <a name="examples"></a><span data-ttu-id="f6445-589">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6445-589">Examples</span></span>

<span data-ttu-id="f6445-590">Im folgenden PowerShell-Codebeispiel wird die Ausrichtung der Datenträger auf einem Computer überprüft: Wenn der Offset eine Bruch Zahl ist, wird der Datenträger nicht ordnungsgemäß ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f6445-590">The following PowerShell code sample checks the alignment of disks on a computer: if the offset is fractional, the disk is not aligned correctly.</span></span>


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="f6445-591">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6445-591">Requirements</span></span>



| <span data-ttu-id="f6445-592">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6445-592">Requirement</span></span> | <span data-ttu-id="f6445-593">Wert</span><span class="sxs-lookup"><span data-stu-id="f6445-593">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6445-594">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6445-594">Minimum supported client</span></span><br/> | <span data-ttu-id="f6445-595">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6445-595">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6445-596">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6445-596">Minimum supported server</span></span><br/> | <span data-ttu-id="f6445-597">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6445-597">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6445-598">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6445-598">Namespace</span></span><br/>                | <span data-ttu-id="f6445-599">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f6445-599">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6445-600">MOF</span><span class="sxs-lookup"><span data-stu-id="f6445-600">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6445-601"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6445-601"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6445-602">DLL</span><span class="sxs-lookup"><span data-stu-id="f6445-602">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6445-603"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6445-603"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6445-604">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6445-604">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6445-605">**CIM \_ Diskpartition**</span><span class="sxs-lookup"><span data-stu-id="f6445-605">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

<span data-ttu-id="f6445-606">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6445-606">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6445-607">WMI-Tasks: Datenträger und Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="f6445-607">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

