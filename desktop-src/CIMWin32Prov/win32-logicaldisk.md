---
description: Stellt eine Datenquelle dar, die in ein tatsächliches lokales Speichergerät auf einem Computersystem aufgelöst wird, auf dem Windows ausgeführt wird.
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Win32_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338889"
---
# <a name="win32_logicaldisk-class"></a><span data-ttu-id="946cf-103">Win32 \_ LogicalDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="946cf-103">Win32\_LogicalDisk class</span></span>

<span data-ttu-id="946cf-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ LogicalDisk** " stellt eine Datenquelle dar, die in ein tatsächliches lokales Speichergerät auf einem Computersystem mit Windows aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-104">The **Win32\_LogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a data source that resolves to an actual local storage device on a computer system running Windows.</span></span>

<span data-ttu-id="946cf-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="946cf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="946cf-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="946cf-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="946cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="946cf-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="946cf-108">Member</span><span class="sxs-lookup"><span data-stu-id="946cf-108">Members</span></span>

<span data-ttu-id="946cf-109">Die **Win32 \_ LogicalDisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="946cf-109">The **Win32\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="946cf-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="946cf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="946cf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="946cf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="946cf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="946cf-112">Methods</span></span>

<span data-ttu-id="946cf-113">Die **Win32 \_ LogicalDisk** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="946cf-113">The **Win32\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="946cf-114">Methode</span><span class="sxs-lookup"><span data-stu-id="946cf-114">Method</span></span>                                                                             | <span data-ttu-id="946cf-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="946cf-115">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="946cf-116">**CHKDSK**</span><span class="sxs-lookup"><span data-stu-id="946cf-116">**Chkdsk**</span></span>](chkdsk-method-in-class-win32-logicaldisk.md)                         | <span data-ttu-id="946cf-117">Ruft den [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) -Vorgang auf dem Datenträger auf.</span><span class="sxs-lookup"><span data-stu-id="946cf-117">Invokes the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation on the disk.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="946cf-118">**Excludefromautochk**</span><span class="sxs-lookup"><span data-stu-id="946cf-118">**ExcludeFromAutochk**</span></span>](excludefromautochk-method-in-class-win32-logicaldisk.md) | <span data-ttu-id="946cf-119">Schließt Datenträger aus dem [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) -Vorgang aus, der beim nächsten Neustart ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="946cf-119">Excludes disks from the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation to be run at the next restart.</span></span><br/>                                                                                      |
| <span data-ttu-id="946cf-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="946cf-120">**Reset**</span></span>                                                                          | <span data-ttu-id="946cf-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="946cf-121">Not implemented.</span></span> <span data-ttu-id="946cf-122">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDisk**](cim-logicaldisk.md) (Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="946cf-122">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md) for documentation.</span></span><br/> |
| [<span data-ttu-id="946cf-123">**Scheduleautochk**</span><span class="sxs-lookup"><span data-stu-id="946cf-123">**ScheduleAutoChk**</span></span>](scheduleautochk-method-in-class-win32-logicaldisk.md)       | <span data-ttu-id="946cf-124">Plant das Ausführen von [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) beim nächsten Neustart, wenn das änderungsbit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="946cf-124">Schedules [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart if the dirty bit has been set.</span></span><br/>                                                                                |
| <span data-ttu-id="946cf-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="946cf-125">**SetPowerState**</span></span>                                                                  | <span data-ttu-id="946cf-126">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="946cf-126">Not implemented.</span></span> <span data-ttu-id="946cf-127">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="946cf-127">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="946cf-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="946cf-128">Properties</span></span>

<span data-ttu-id="946cf-129">Die **Win32 \_ LogicalDisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="946cf-129">The **Win32\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="946cf-130">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="946cf-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="946cf-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-133">Typ des verfügbaren Medien Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="946cf-133">Type of media access available.</span></span>

<span data-ttu-id="946cf-134">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="946cf-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="946cf-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="946cf-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="946cf-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="946cf-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="946cf-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-138">Schreibbar</span><span class="sxs-lookup"><span data-stu-id="946cf-138">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="946cf-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="946cf-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="946cf-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="946cf-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-141">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="946cf-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-142">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="946cf-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="946cf-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-145">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="946cf-145">Availability and status of the device.</span></span>

<span data-ttu-id="946cf-146">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="946cf-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="946cf-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="946cf-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="946cf-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="946cf-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="946cf-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-150">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="946cf-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="946cf-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="946cf-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="946cf-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="946cf-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="946cf-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="946cf-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="946cf-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="946cf-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="946cf-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="946cf-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-156">Offline</span><span class="sxs-lookup"><span data-stu-id="946cf-156">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="946cf-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="946cf-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="946cf-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="946cf-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="946cf-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="946cf-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="946cf-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="946cf-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="946cf-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="946cf-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-162">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="946cf-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="946cf-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="946cf-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-164">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="946cf-164">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="946cf-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="946cf-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-166">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="946cf-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="946cf-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="946cf-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="946cf-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-169">Das Gerät befindet sich in einem Warn Status, aber auch in einem Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="946cf-169">The device is in a warning state, but also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="946cf-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="946cf-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-171">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="946cf-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="946cf-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="946cf-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-173">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="946cf-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="946cf-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="946cf-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-175">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="946cf-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="946cf-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="946cf-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-177">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="946cf-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-178">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="946cf-178">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-179">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="946cf-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-181">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="946cf-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-182">Größe (in Bytes) der Blöcke, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="946cf-182">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="946cf-183">Wenn unbekannt oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 ein.</span><span class="sxs-lookup"><span data-stu-id="946cf-183">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter 1.</span></span>

<span data-ttu-id="946cf-184">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="946cf-185">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="946cf-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-186">**Caption**</span><span class="sxs-lookup"><span data-stu-id="946cf-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-189">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="946cf-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-190">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="946cf-190">Short description of the object a one-line string.</span></span>

<span data-ttu-id="946cf-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-192">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="946cf-192">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-193">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-195">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ Vol \_ ist \_ komprimiert")</span><span class="sxs-lookup"><span data-stu-id="946cf-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-196">**True** gibt an, dass das logische Volume als einzelne komprimierte Entität, z. b. ein Double Space-Volume, vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-196">If **True**, the logical volume exists as a single compressed entity, such as a DoubleSpace volume.</span></span> <span data-ttu-id="946cf-197">Wenn eine dateibasierte Komprimierung unterstützt wird, z. b. auf NTFS, lautet diese Eigenschaft **false**.</span><span class="sxs-lookup"><span data-stu-id="946cf-197">If file based compression is supported, such as on NTFS, this property is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-198">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="946cf-198">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-199">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="946cf-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-201">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="946cf-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-202">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="946cf-202">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="946cf-203">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-203">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="946cf-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="946cf-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="946cf-205"> (0)</span><span class="sxs-lookup"><span data-stu-id="946cf-205">(0)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-206">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="946cf-206">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="946cf-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="946cf-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="946cf-208">(1)</span><span class="sxs-lookup"><span data-stu-id="946cf-208">(1)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-209">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="946cf-209">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="946cf-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="946cf-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="946cf-211">(2)</span><span class="sxs-lookup"><span data-stu-id="946cf-211">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="946cf-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="946cf-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="946cf-213">(3)</span><span class="sxs-lookup"><span data-stu-id="946cf-213">(3)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-214">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="946cf-214">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="946cf-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="946cf-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="946cf-216">(4)</span><span class="sxs-lookup"><span data-stu-id="946cf-216">(4)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-217">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="946cf-217">Device is not working properly.</span></span> <span data-ttu-id="946cf-218">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="946cf-218">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="946cf-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="946cf-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="946cf-220">(5)</span><span class="sxs-lookup"><span data-stu-id="946cf-220">(5)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-221">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="946cf-221">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="946cf-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="946cf-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="946cf-223"> (6)</span><span class="sxs-lookup"><span data-stu-id="946cf-223">(6)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-224">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="946cf-224">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="946cf-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="946cf-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="946cf-226">(7)</span><span class="sxs-lookup"><span data-stu-id="946cf-226">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="946cf-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="946cf-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="946cf-228">(8)</span><span class="sxs-lookup"><span data-stu-id="946cf-228">(8)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-229">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="946cf-229">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="946cf-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="946cf-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="946cf-231">(9)</span><span class="sxs-lookup"><span data-stu-id="946cf-231">(9)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-232">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="946cf-232">Device is not working properly.</span></span> <span data-ttu-id="946cf-233">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="946cf-233">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="946cf-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="946cf-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="946cf-235">(10)</span><span class="sxs-lookup"><span data-stu-id="946cf-235">(10)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-236">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-236">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="946cf-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="946cf-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="946cf-238">(11)</span><span class="sxs-lookup"><span data-stu-id="946cf-238">(11)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-239">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="946cf-239">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="946cf-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="946cf-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="946cf-241">(12)</span><span class="sxs-lookup"><span data-stu-id="946cf-241">(12)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-242">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="946cf-242">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="946cf-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="946cf-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="946cf-244">(13)</span><span class="sxs-lookup"><span data-stu-id="946cf-244">(13)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-245">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-245">Windows cannot verify the device resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="946cf-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="946cf-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="946cf-247">(14)</span><span class="sxs-lookup"><span data-stu-id="946cf-247">(14)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-248">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-248">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="946cf-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="946cf-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="946cf-250">(15)</span><span class="sxs-lookup"><span data-stu-id="946cf-250">(15)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-251">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="946cf-251">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="946cf-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="946cf-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="946cf-253">(16)</span><span class="sxs-lookup"><span data-stu-id="946cf-253">(16)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-254">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-254">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="946cf-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="946cf-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="946cf-256">(17)</span><span class="sxs-lookup"><span data-stu-id="946cf-256">(17)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-257">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="946cf-257">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="946cf-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="946cf-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="946cf-259">(18)</span><span class="sxs-lookup"><span data-stu-id="946cf-259">(18)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-260">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-260">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="946cf-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="946cf-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="946cf-262">(19)</span><span class="sxs-lookup"><span data-stu-id="946cf-262">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="946cf-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="946cf-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="946cf-264">(20)</span><span class="sxs-lookup"><span data-stu-id="946cf-264">(20)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-265">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="946cf-265">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="946cf-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="946cf-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="946cf-267">(21)</span><span class="sxs-lookup"><span data-stu-id="946cf-267">(21)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-268">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="946cf-268">System failure.</span></span> <span data-ttu-id="946cf-269">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="946cf-269">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="946cf-270">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="946cf-270">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="946cf-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="946cf-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="946cf-272">(22)</span><span class="sxs-lookup"><span data-stu-id="946cf-272">(22)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-273">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="946cf-273">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="946cf-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="946cf-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="946cf-275">(23)</span><span class="sxs-lookup"><span data-stu-id="946cf-275">(23)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-276">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="946cf-276">System failure.</span></span> <span data-ttu-id="946cf-277">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="946cf-277">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="946cf-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="946cf-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="946cf-279">(24)</span><span class="sxs-lookup"><span data-stu-id="946cf-279">(24)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-280">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="946cf-280">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="946cf-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="946cf-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="946cf-282">(25)</span><span class="sxs-lookup"><span data-stu-id="946cf-282">(25)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-283">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="946cf-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="946cf-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="946cf-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="946cf-285">(26)</span><span class="sxs-lookup"><span data-stu-id="946cf-285">(26)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-286">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="946cf-286">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="946cf-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="946cf-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="946cf-288">(27)</span><span class="sxs-lookup"><span data-stu-id="946cf-288">(27)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-289">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="946cf-289">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="946cf-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="946cf-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="946cf-291">(28)</span><span class="sxs-lookup"><span data-stu-id="946cf-291">(28)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-292">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="946cf-292">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="946cf-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="946cf-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="946cf-294">(29)</span><span class="sxs-lookup"><span data-stu-id="946cf-294">(29)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-295">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="946cf-295">Device is disabled.</span></span> <span data-ttu-id="946cf-296">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="946cf-296">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="946cf-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="946cf-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="946cf-298">(30)</span><span class="sxs-lookup"><span data-stu-id="946cf-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-299">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="946cf-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="946cf-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="946cf-301">31,5</span><span class="sxs-lookup"><span data-stu-id="946cf-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-302">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="946cf-302">Device is not working properly.</span></span> <span data-ttu-id="946cf-303">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-303">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-304">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="946cf-304">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-305">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-307">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="946cf-307">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-308">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="946cf-308">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="946cf-309">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-310">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="946cf-310">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-311">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-313">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="946cf-313">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="946cf-314">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-314">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="946cf-315">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-315">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="946cf-316">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-317">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="946cf-317">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-320">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="946cf-320">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-321">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="946cf-321">Description of the object.</span></span>

<span data-ttu-id="946cf-322">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-323">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="946cf-323">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-326">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="946cf-326">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-327">Eindeutiger Bezeichner des logischen Datenträgers von anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="946cf-327">Unique identifier of the logical disk from other devices on the system.</span></span>

<span data-ttu-id="946cf-328">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="946cf-329">Ein Codebeispiel, in dem diese Eigenschaft abgerufen wird, finden Sie unten im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="946cf-329">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-330">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="946cf-330">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-331">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="946cf-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-333">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| filefunctions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="946cf-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|FileFunctions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-334">Numerischer Wert, der dem Typ des Laufwerks entspricht, das dieser logische Datenträger darstellt.</span><span class="sxs-lookup"><span data-stu-id="946cf-334">Numeric value that corresponds to the type of disk drive this logical disk represents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="946cf-335">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="946cf-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

<span data-ttu-id="946cf-336">**Kein Stammverzeichnis** (1)</span><span class="sxs-lookup"><span data-stu-id="946cf-336">**No Root Directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

<span data-ttu-id="946cf-337">Wechsel Datenträger **(2** )</span><span class="sxs-lookup"><span data-stu-id="946cf-337">**Removable Disk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

<span data-ttu-id="946cf-338">**Lokaler** Datenträger (3)</span><span class="sxs-lookup"><span data-stu-id="946cf-338">**Local Disk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

<span data-ttu-id="946cf-339">**Netzwerklaufwerk** (4)</span><span class="sxs-lookup"><span data-stu-id="946cf-339">**Network Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

<span data-ttu-id="946cf-340">**Compact Disk** (5)</span><span class="sxs-lookup"><span data-stu-id="946cf-340">**Compact Disc** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

<span data-ttu-id="946cf-341">**RAM** -Datenträger (6)</span><span class="sxs-lookup"><span data-stu-id="946cf-341">**RAM Disk** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-342">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="946cf-342">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-343">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-345">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-345">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="946cf-346">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-347">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="946cf-347">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-350">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. getroffenen Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="946cf-350">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="946cf-351">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-352">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="946cf-352">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-355">Typ der Fehlererkennung und-Korrektur, der von diesem Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-355">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="946cf-356">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-356">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-357">**Verwendet**</span><span class="sxs-lookup"><span data-stu-id="946cf-357">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-360">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="946cf-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="946cf-361">Dateisystem auf dem logischen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="946cf-361">File system on the logical disk.</span></span>

<span data-ttu-id="946cf-362">Beispiel: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="946cf-362">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="946cf-363">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="946cf-363">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-364">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="946cf-364">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-366">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="946cf-366">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-367">Auf dem logischen Datenträger verfügbarer Speicherplatz (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="946cf-367">Space, in bytes, available on the logical disk.</span></span>

<span data-ttu-id="946cf-368">Diese Eigenschaft wird von [**CIM \_ LogicalDisk**](cim-logicaldisk.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-368">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="946cf-369">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="946cf-369">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="946cf-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-371">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="946cf-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-373">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="946cf-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-374">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="946cf-374">Date and time the object was installed.</span></span> <span data-ttu-id="946cf-375">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-375">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="946cf-376">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="946cf-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-378">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="946cf-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-380">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="946cf-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="946cf-381">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-382">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="946cf-382">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-383">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="946cf-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-385">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="946cf-385">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="946cf-386">Maximale Länge einer vom Windows-Laufwerk unterstützten Dateinamen Komponente.</span><span class="sxs-lookup"><span data-stu-id="946cf-386">Maximum length of a filename component supported by the Windows drive.</span></span> <span data-ttu-id="946cf-387">Eine Dateinamen Komponente ist dieser Teil eines Datei namens zwischen umgekehrten Schrägstrichen.</span><span class="sxs-lookup"><span data-stu-id="946cf-387">A filename component is that portion of a filename between backslashes.</span></span> <span data-ttu-id="946cf-388">Der Wert kann verwendet werden, um anzugeben, dass lange Namen vom angegebenen Dateisystem unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-388">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="946cf-389">Beispielsweise speichert die Funktion für ein FAT-Dateisystem, das lange Namen unterstützt, den Wert 255 und nicht den vorherigen 8,3-Indikator.</span><span class="sxs-lookup"><span data-stu-id="946cf-389">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="946cf-390">Lange Namen können auch auf Systemen unterstützt werden, die das NTFS-Dateisystem verwenden.</span><span class="sxs-lookup"><span data-stu-id="946cf-390">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="946cf-391">Beispiel: 255</span><span class="sxs-lookup"><span data-stu-id="946cf-391">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="946cf-392">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="946cf-392">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-393">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="946cf-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-395">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="946cf-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-396">Typ der Medien, die derzeit auf dem logischen Laufwerk vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="946cf-396">Type of media currently present in the logical drive.</span></span> <span data-ttu-id="946cf-397">Dieser Wert ist einer der Werte der \_ Medientyp-Enumeration, der in winioctl. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-397">This value will be one of the values of the MEDIA\_TYPE enumeration defined in Winioctl.h.</span></span> <span data-ttu-id="946cf-398">Der Wert ist möglicherweise für Wechsel Datenträger nicht exakt, wenn das Laufwerk derzeit keine Medien enthält.</span><span class="sxs-lookup"><span data-stu-id="946cf-398">The value may not be exact for removable drives if currently there is no media in the drive.</span></span>

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span data-ttu-id="946cf-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>Das **Format ist unbekannt** (0).</span><span class="sxs-lookup"><span data-stu-id="946cf-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Format is unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (1)</span><span class="sxs-lookup"><span data-stu-id="946cf-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (1)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-401">5 1/4-Zoll-Diskette-1,2 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-401">5 1/4-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (2)</span><span class="sxs-lookup"><span data-stu-id="946cf-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (2)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-403">3 1/2-Zoll-Diskette-1,44 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-403">3 1/2-Inch Floppy Disk - 1.44 MB -512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (3)</span><span class="sxs-lookup"><span data-stu-id="946cf-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (3)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-405">3 1/2-Zoll-Diskette-2,88 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-405">3 1/2-Inch Floppy Disk - 2.88 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (4)</span><span class="sxs-lookup"><span data-stu-id="946cf-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-407">3 1/2-Zoll-Diskette-20,8 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-407">3 1/2-Inch Floppy Disk - 20.8 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (5)</span><span class="sxs-lookup"><span data-stu-id="946cf-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (5)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-409">3 1/2-Zoll-Diskette-720 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-409">3 1/2-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (6)</span><span class="sxs-lookup"><span data-stu-id="946cf-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (6)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-411">5 1/4-Zoll-Diskette-360 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-411">5 1/4-Inch Floppy Disk - 360 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="946cf-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (7)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-413">5 1/4-Zoll-Diskette-320 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-413">5 1/4-Inch Floppy Disk - 320 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (8)</span><span class="sxs-lookup"><span data-stu-id="946cf-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (8)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-415">5 1/4-Zoll-Diskette-320 KB-1024 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-415">5 1/4-Inch Floppy Disk - 320 KB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (9)</span><span class="sxs-lookup"><span data-stu-id="946cf-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (9)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-417">5 1/4-Zoll-Diskette-180 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-417">5 1/4-Inch Floppy Disk - 180 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (10)</span><span class="sxs-lookup"><span data-stu-id="946cf-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (10)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-419">5 1/4-Zoll-Diskette-160 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-419">5 1/4-Inch Floppy Disk - 160 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span data-ttu-id="946cf-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>Wechsel Datenträger außer **Diskette** (11)</span><span class="sxs-lookup"><span data-stu-id="946cf-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Removable media other than floppy** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span data-ttu-id="946cf-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Festes Festplatten Medium** (12)</span><span class="sxs-lookup"><span data-stu-id="946cf-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Fixed hard disk media** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (13)</span><span class="sxs-lookup"><span data-stu-id="946cf-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (13)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-423">3 1/2-Zoll-Diskette-120 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-423">3 1/2-Inch Floppy Disk - 120 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (14)</span><span class="sxs-lookup"><span data-stu-id="946cf-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (14)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-425">3 1/2-Zoll-Diskette-640 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-425">3 1/2-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (15)</span><span class="sxs-lookup"><span data-stu-id="946cf-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (15)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-427">5 1/4-Zoll-Diskette-640 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-427">5 1/4-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (16)</span><span class="sxs-lookup"><span data-stu-id="946cf-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (16)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-429">5 1/4-Zoll-Diskette-720 KB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-429">5 1/4-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (17)</span><span class="sxs-lookup"><span data-stu-id="946cf-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (17)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-431">3 1/2-Zoll-Diskette-1,2 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-431">3 1/2-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (18)</span><span class="sxs-lookup"><span data-stu-id="946cf-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (18)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-433">3 1/2-Zoll-Diskette-1,23 MB-1024 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-433">3 1/2-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-Zoll-Diskette** (19)</span><span class="sxs-lookup"><span data-stu-id="946cf-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (19)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-435">5 1/4-Zoll-Diskette-1,23 MB-1024 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-435">5 1/4-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (20)</span><span class="sxs-lookup"><span data-stu-id="946cf-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (20)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-437">3 1/2-Zoll-Diskette-128 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-437">3 1/2-Inch Floppy Disk - 128 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-Zoll-Diskette** (21)</span><span class="sxs-lookup"><span data-stu-id="946cf-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (21)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-439">3 1/2-Zoll-Diskette-230 MB-512 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-439">3 1/2-Inch Floppy Disk - 230 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="946cf-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Zoll-Diskette** (22)</span><span class="sxs-lookup"><span data-stu-id="946cf-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Inch Floppy Disk** (22)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-441">8-Zoll-Diskette-256 KB-128 Byte/Sektor</span><span class="sxs-lookup"><span data-stu-id="946cf-441">8-Inch Floppy Disk - 256 KB - 128 bytes/sector</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-442">**Name**</span><span class="sxs-lookup"><span data-stu-id="946cf-442">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-443">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-445">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="946cf-445">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-446">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-446">Label by which the object is known.</span></span> <span data-ttu-id="946cf-447">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-447">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="946cf-448">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-448">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-449">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="946cf-449">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-450">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="946cf-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-452">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="946cf-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-453">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="946cf-453">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="946cf-454">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-454">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="946cf-455">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="946cf-455">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="946cf-456">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-456">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="946cf-457">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="946cf-457">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-458">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="946cf-458">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-459">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-461">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="946cf-461">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-462">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="946cf-462">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="946cf-463">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="946cf-464">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="946cf-464">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="946cf-465">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="946cf-465">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-466">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="946cf-466">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="946cf-467">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-468">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="946cf-468">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="946cf-469">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-469">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="946cf-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="946cf-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="946cf-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="946cf-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="946cf-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="946cf-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="946cf-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="946cf-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-474">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="946cf-474">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="946cf-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="946cf-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-476">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="946cf-476">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="946cf-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="946cf-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-478">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="946cf-478">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="946cf-479">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-479">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="946cf-480">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="946cf-480">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="946cf-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="946cf-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-482">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-482">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="946cf-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="946cf-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="946cf-484">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="946cf-484">Timed Power-On Supported</span></span>

<span data-ttu-id="946cf-485">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-485">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-486">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="946cf-486">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-487">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-487">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-488">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-489">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="946cf-489">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="946cf-490">Diese Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-490">This property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="946cf-491">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-492">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="946cf-492">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-493">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-494">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-495">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows Networking Functions \| WNetGetConnection")</span><span class="sxs-lookup"><span data-stu-id="946cf-495">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-496">Der Netzwerkpfad zum logischen Gerät.</span><span class="sxs-lookup"><span data-stu-id="946cf-496">Network path to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-497">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="946cf-497">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-498">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-500">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="946cf-500">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="946cf-501">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-501">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-502">**Quotasdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="946cf-502">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-503">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-505">Gibt an, dass die Kontingent Verwaltung auf diesem System nicht aktiviert ist (true).</span><span class="sxs-lookup"><span data-stu-id="946cf-505">Indicates that quota management is not enabled (TRUE) on this system.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-506">**Quotasunvollständig**</span><span class="sxs-lookup"><span data-stu-id="946cf-506">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-507">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-507">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-508">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-509">Gibt an, dass die Kontingent Verwaltung verwendet wurde, aber deaktiviert wurde (**true**).</span><span class="sxs-lookup"><span data-stu-id="946cf-509">Indicates that the quota management was used but has been disabled (**True**).</span></span> <span data-ttu-id="946cf-510">Unvollständig bezieht sich auf die im Dateisystem verbleibenden Informationen, nachdem die Kontingent Verwaltung deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="946cf-510">Incomplete refers to the information left in the file system after quota management was disabled.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-511">**Quotasrebuild**</span><span class="sxs-lookup"><span data-stu-id="946cf-511">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-512">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-512">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-514">**True** gibt an, dass das Dateisystem den aktiven Prozess zum Kompilieren von Informationen und Festlegen des Datenträgers für die Kontingent Verwaltung durchläuft.</span><span class="sxs-lookup"><span data-stu-id="946cf-514">If **True**, indicates that the file system is in the active process of compiling information and setting the disk up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-515">**Größe**</span><span class="sxs-lookup"><span data-stu-id="946cf-515">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-516">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-517">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-518">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="946cf-518">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-519">Größe des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="946cf-519">Size of the disk drive.</span></span>

<span data-ttu-id="946cf-520">Diese Eigenschaft wird von [**CIM \_ LogicalDisk**](cim-logicaldisk.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-520">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="946cf-521">Ein Codebeispiel, in dem diese Eigenschaft abgerufen wird, finden Sie unten im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="946cf-521">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="946cf-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-525">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="946cf-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-526">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="946cf-526">Current status of the object.</span></span> <span data-ttu-id="946cf-527">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="946cf-528">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="946cf-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="946cf-529">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="946cf-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="946cf-530">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="946cf-531">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="946cf-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="946cf-532">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="946cf-533">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="946cf-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="946cf-534">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="946cf-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="946cf-535">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="946cf-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="946cf-536">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="946cf-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="946cf-537">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="946cf-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="946cf-538">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="946cf-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="946cf-539">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="946cf-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="946cf-540">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="946cf-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="946cf-541">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="946cf-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="946cf-542">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="946cf-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="946cf-543">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="946cf-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="946cf-544">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="946cf-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="946cf-545">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="946cf-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="946cf-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-547">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="946cf-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-549">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="946cf-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-550">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="946cf-550">State of the logical device.</span></span> <span data-ttu-id="946cf-551">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="946cf-552">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="946cf-553">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="946cf-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="946cf-554">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="946cf-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="946cf-555">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="946cf-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="946cf-556">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="946cf-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="946cf-557">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="946cf-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="946cf-558">**Supportsdiskkontingenten**</span><span class="sxs-lookup"><span data-stu-id="946cf-558">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-559">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-559">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-560">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-560">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="946cf-561">**True** gibt an, dass dieses Volume Datenträger Kontingente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="946cf-561">If **True**, this volume supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-562">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="946cf-562">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-563">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-564">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-565">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ file \_ Compression")</span><span class="sxs-lookup"><span data-stu-id="946cf-565">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-566">**True** gibt an, dass die logische Datenträger Partition dateibasierte Komprimierung unterstützt, wie z. b. bei dem NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="946cf-566">If **True**, the logical disk partition supports file-based compression, such as is the case with the NTFS file system.</span></span> <span data-ttu-id="946cf-567">Diese Eigenschaft ist **false** , wenn die **komprimierte** Eigenschaft den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="946cf-567">This property is **False** when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-568">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="946cf-568">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-569">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-569">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-570">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-570">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-571">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="946cf-571">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="946cf-572">Der Wert **der Eigenschaft "** Eigenschaft des Bereichs Computers".</span><span class="sxs-lookup"><span data-stu-id="946cf-572">Value of the scoping computer **CreationClassName** property.</span></span>

<span data-ttu-id="946cf-573">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-574">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="946cf-574">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-575">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-575">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-576">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-577">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="946cf-577">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="946cf-578">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="946cf-578">Name of the scoping system.</span></span>

<span data-ttu-id="946cf-579">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="946cf-579">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="946cf-580">**VolumeDirty**</span><span class="sxs-lookup"><span data-stu-id="946cf-580">**VolumeDirty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-581">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-581">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-582">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-582">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-583">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("das \_ Volume ist fehlerhaft \_ \_ ")</span><span class="sxs-lookup"><span data-stu-id="946cf-583">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL\_IS\_VOLUME\_DIRTY")</span></span>
</dt> </dl>

<span data-ttu-id="946cf-584">**True** gibt an, dass der Datenträger beim nächsten Neustart [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="946cf-584">If **True**, the disk requires [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart.</span></span> <span data-ttu-id="946cf-585">Diese Eigenschaft gilt nur für die Instanzen von logischen Datenträgern, die einen physischen Datenträger auf dem Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="946cf-585">This property is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="946cf-586">Sie ist nicht auf zugeordnete logische Laufwerke anwendbar.</span><span class="sxs-lookup"><span data-stu-id="946cf-586">It is not applicable to mapped logical drives.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-587">**Volumename**</span><span class="sxs-lookup"><span data-stu-id="946cf-587">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-588">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-589">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="946cf-589">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="946cf-590">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="946cf-590">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="946cf-591">Der Volumename des logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="946cf-591">Volume name of the logical disk.</span></span>

<span data-ttu-id="946cf-592">Einschränkungen: maximale Länge von 32 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="946cf-592">Constraints: Maximum 32 characters.</span></span>

<span data-ttu-id="946cf-593">Ein Codebeispiel, in dem diese Eigenschaft abgerufen wird, finden Sie unten im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="946cf-593">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="946cf-594">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="946cf-594">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946cf-595">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="946cf-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="946cf-596">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="946cf-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946cf-597">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="946cf-597">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="946cf-598">Seriennummer des logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="946cf-598">Volume serial number of the logical disk.</span></span>

<span data-ttu-id="946cf-599">Einschränkungen: maximal 11 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="946cf-599">Constraints: Maximum 11 characters.</span></span>

<span data-ttu-id="946cf-600">Beispiel: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="946cf-600">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="946cf-601">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="946cf-601">Remarks</span></span>

<span data-ttu-id="946cf-602">Die **Win32 \_ LogicalDisk** -Klasse wird von [**CIM \_ LogicalDisk**](cim-logicaldisk.md) abgeleitet, der von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-602">The **Win32\_LogicalDisk** class is derived from [**CIM\_LogicalDisk**](cim-logicaldisk.md) which derives from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="946cf-603">Die **CIM \_ storageblock** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="946cf-603">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="946cf-604">Ein physisches Laufwerk ist der Eckpfeiler eines beliebigen Speicher Verwaltungssystems.</span><span class="sxs-lookup"><span data-stu-id="946cf-604">A physical disk drive is the cornerstone of any storage management system.</span></span> <span data-ttu-id="946cf-605">Nachdem jedoch ein physisches Laufwerk installiert wurde, behandeln weder Benutzer noch Systemadministratoren die Hardware in der Regel direkt.</span><span class="sxs-lookup"><span data-stu-id="946cf-605">However, after a physical disk drive has been installed, neither users nor system administrators typically deal with the hardware directly.</span></span> <span data-ttu-id="946cf-606">Stattdessen interagieren sowohl Benutzer als auch Systemadministratoren mit den logischen Laufwerken, die auf dem Datenträger erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="946cf-606">Instead, both users and system administrators interact with the logical drives that have been created on the disk.</span></span>

<span data-ttu-id="946cf-607">Bei einem logischen Laufwerk handelt es sich um eine Unterteilung einer Partition, der ein eigener Laufwerk Buchstabe zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="946cf-607">A logical drive is a subdivision of a partition that has been assigned its own drive letter.</span></span> <span data-ttu-id="946cf-608">(Es ist möglich, dass eine Partition vorhanden ist, der kein Laufwerk Buchstabe zugewiesen wurde.) Wenn Sie über Laufwerk C oder Laufwerk D sprechen, verweisen Sie auf ein logisches Laufwerk und nicht auf ein physisches Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="946cf-608">(It is possible to have a partition that has not been assigned a drive letter.) When you talk about drive C or drive D, you are referring to a logical drive rather than to a physical disk drive.</span></span> <span data-ttu-id="946cf-609">Wenn Sie ein Dokument auf Laufwerk E speichern, speichern Sie es auf dem logischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="946cf-609">Likewise, when you save a document to drive E, you are saving it to the logical drive.</span></span> <span data-ttu-id="946cf-610">Physische Datenträger bilden die Hardware, die ein Laufwerk bildet, einschließlich Komponenten wie Köpfen, Sektoren und Zylinder.</span><span class="sxs-lookup"><span data-stu-id="946cf-610">Physical disks compose the hardware that makes up a drive, including such components as heads, sectors, and cylinders.</span></span> <span data-ttu-id="946cf-611">Logische Laufwerke haben dagegen Eigenschaften wie Speicherplatz, verfügbarer Speicherplatz und Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="946cf-611">Logical drives, by contrast, have properties such as disk space, available disk space, and drive letters.</span></span>

> [!Note]  
> <span data-ttu-id="946cf-612">Die **Win32 \_ LogicalDisk** -Klasse kann nur zum Auflisten der Eigenschaften lokaler Laufwerke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="946cf-612">The **Win32\_LogicalDisk** class can be used only to enumerate the properties of local disk drives.</span></span> <span data-ttu-id="946cf-613">Sie können jedoch die [**Win32 \_ mappedlogicaldisk**](win32-mappedlogicaldisk.md) -Klasse verwenden, um die Eigenschaften von zugeordneten Netzwerklaufwerken aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="946cf-613">However, you can use the [**Win32\_MappedLogicalDisk**](win32-mappedlogicaldisk.md) class to enumerate the properties of mapped network drives.</span></span>

 

## <a name="examples"></a><span data-ttu-id="946cf-614">Beispiele</span><span class="sxs-lookup"><span data-stu-id="946cf-614">Examples</span></span>

<span data-ttu-id="946cf-615">Weitere Beispiele finden Sie unter Verwenden von **Win32 \_ LogicalDisk** zum Abrufen von Datenträger-oder Volumedaten im Thema [WMI-Tasks: Datenträger und Dateisysteme](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) .</span><span class="sxs-lookup"><span data-stu-id="946cf-615">You can find other examples using **Win32\_LogicalDisk** to obtain disk or volume data in the [WMI Tasks: Disks and File Systems](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) topic.</span></span>

<span data-ttu-id="946cf-616">Das Codebeispiel für den [WMI-Informations](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) Abruf im VBScript-Code in der TechNet Gallery verwendet die **Win32 \_ LogicalDisk** -Klasse, um Hardwareinformationen von einer Reihe von Remote Computern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="946cf-616">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_LogicalDisk** class to retrieve hardware information from a number of remote computers.</span></span>

<span data-ttu-id="946cf-617">Die Datenträger [Informationen werden mithilfe von WMI/CIM erhalten...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell-Codebeispiel in der TechNet Gallery **verwendet Win32 \_ LogicalDisk** zum Abrufen von " **DeviceID**", " **Volumename**" und " **size** " von einem Zielgerät.</span><span class="sxs-lookup"><span data-stu-id="946cf-617">The [Get Disk info using wmi/cim...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell code example on the TechNet Gallery uses **Win32\_LogicalDisk** to retrieve **DeviceID**, **VolumeName**, and **Size** from a target device.</span></span> <span data-ttu-id="946cf-618">Insbesondere enthält dieses Beispiel eine strikte Ausnahmebehandlung und gibt ein einzelnes Objekt pro Computer und nicht pro Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="946cf-618">In particular, this sample includes rigorous exception handling, and returns a single object per computer, rather than per disk.</span></span>

<span data-ttu-id="946cf-619">Unternehmens Skripts umfassen häufig die Konfiguration von Hardware und Software auf Remote Computern. Dies erfordert wiederum, dass Sie im Voraus wissen, welche Art von Festplatten Laufwerken auf einem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-619">Enterprise scripting often involves configuring hardware and software on remote computers; in turn, this requires you to know, in advance, the type of disk drives installed on a computer.</span></span> <span data-ttu-id="946cf-620">Beispielsweise funktioniert ein Skript, das eine Anwendung auf Laufwerk e installiert, nur, wenn Laufwerk e eine Festplatte ist.</span><span class="sxs-lookup"><span data-stu-id="946cf-620">For example, a script that installs an application on drive E works only if drive E is a hard disk.</span></span> <span data-ttu-id="946cf-621">Wenn Laufwerk E ein Diskettenlaufwerk oder ein CD-ROM-Laufwerk darstellt, schlägt das Skript fehl.</span><span class="sxs-lookup"><span data-stu-id="946cf-621">If drive E happens to represent a floppy disk or a CD-ROM drive, the script fails.</span></span> <span data-ttu-id="946cf-622">Mit dem folgenden Code werden die auf einem Computer installierten Laufwerke und Laufwerkstypen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="946cf-622">The following code identifies the drives and drive types installed on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





<span data-ttu-id="946cf-623">In den folgenden Beispielen wird der freie Speicherplatz auf allen Festplatten Laufwerken eines Computers aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="946cf-623">The following samples enumerate the free space on all the hard disk drives on a computer.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





<span data-ttu-id="946cf-624">Im folgenden Codebeispiel wird der Typ des Dateisystems (FAT, NTFS, FAT32 usw.) zurückgegeben, das auf jedem Laufwerk eines Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="946cf-624">The following code example returns the type of file system (FAT, NTFS, FAT32, and so on) used on each drive in a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





<span data-ttu-id="946cf-625">Im folgenden PowerShell-Codebeispiel werden zusätzliche Informationen zu den logischen lokalen Datenträgern abgerufen.</span><span class="sxs-lookup"><span data-stu-id="946cf-625">The following PowerShell code sample retrieves additional information about the logical local disks.</span></span>


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="946cf-626">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="946cf-626">Requirements</span></span>



| <span data-ttu-id="946cf-627">Anforderung</span><span class="sxs-lookup"><span data-stu-id="946cf-627">Requirement</span></span> | <span data-ttu-id="946cf-628">Wert</span><span class="sxs-lookup"><span data-stu-id="946cf-628">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="946cf-629">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="946cf-629">Minimum supported client</span></span><br/> | <span data-ttu-id="946cf-630">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="946cf-630">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="946cf-631">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="946cf-631">Minimum supported server</span></span><br/> | <span data-ttu-id="946cf-632">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="946cf-632">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="946cf-633">Namespace</span><span class="sxs-lookup"><span data-stu-id="946cf-633">Namespace</span></span><br/>                | <span data-ttu-id="946cf-634">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="946cf-634">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="946cf-635">MOF</span><span class="sxs-lookup"><span data-stu-id="946cf-635">MOF</span></span><br/>                      | <dl> <span data-ttu-id="946cf-636"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="946cf-636"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="946cf-637">DLL</span><span class="sxs-lookup"><span data-stu-id="946cf-637">DLL</span></span><br/>                      | <dl> <span data-ttu-id="946cf-638"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="946cf-638"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="946cf-639">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="946cf-639">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946cf-640">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="946cf-640">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="946cf-641">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="946cf-641">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="946cf-642">WMI-Tasks: Datenträger und Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="946cf-642">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

