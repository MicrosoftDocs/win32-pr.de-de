---
description: Die CIM \_ LogicalDisk-Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das DeviceID (Key)-Feld des Datenträgers identifiziert werden.
ms.assetid: 1c2fd0bf-a1e3-4706-9f84-5dd4d371a167
ms.tgt_platform: multiple
title: CIM_LogicalDisk-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.Access
- CIM_LogicalDisk.Availability
- CIM_LogicalDisk.BlockSize
- CIM_LogicalDisk.Caption
- CIM_LogicalDisk.ConfigManagerErrorCode
- CIM_LogicalDisk.ConfigManagerUserConfig
- CIM_LogicalDisk.CreationClassName
- CIM_LogicalDisk.Description
- CIM_LogicalDisk.DeviceID
- CIM_LogicalDisk.ErrorCleared
- CIM_LogicalDisk.ErrorDescription
- CIM_LogicalDisk.ErrorMethodology
- CIM_LogicalDisk.FreeSpace
- CIM_LogicalDisk.InstallDate
- CIM_LogicalDisk.LastErrorCode
- CIM_LogicalDisk.Name
- CIM_LogicalDisk.NumberOfBlocks
- CIM_LogicalDisk.PNPDeviceID
- CIM_LogicalDisk.PowerManagementCapabilities
- CIM_LogicalDisk.PowerManagementSupported
- CIM_LogicalDisk.Purpose
- CIM_LogicalDisk.Size
- CIM_LogicalDisk.Status
- CIM_LogicalDisk.StatusInfo
- CIM_LogicalDisk.SystemCreationClassName
- CIM_LogicalDisk.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd28ab0b9982606278e65705273a9965cfb9b396
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747960"
---
# <a name="cim_logicaldisk-class-cimwin32-wmi-providers"></a><span data-ttu-id="40d6d-103">CIM_LogicalDisk-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="40d6d-103">CIM_LogicalDisk class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="40d6d-104">Die **CIM \_ LogicalDisk** -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das **DeviceID** (Key)-Feld des Datenträgers identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-104">The **CIM\_LogicalDisk** class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="40d6d-105">Beispielsweise enthält das Feld " **DeviceID** " in einer Windows-Umgebung einen Laufwerk Buchstaben. in einer UNIX-Umgebung enthält Sie den Zugriffs Pfad. und in einer NetWare-Umgebung enthält Sie den Volumenamen.</span><span class="sxs-lookup"><span data-stu-id="40d6d-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40d6d-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="40d6d-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="40d6d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="40d6d-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="40d6d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="40d6d-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="40d6d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d6d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="40d6d-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C539-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="40d6d-111">Member</span><span class="sxs-lookup"><span data-stu-id="40d6d-111">Members</span></span>

<span data-ttu-id="40d6d-112">Die **CIM \_ LogicalDisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="40d6d-112">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="40d6d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="40d6d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="40d6d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40d6d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="40d6d-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="40d6d-115">Methods</span></span>

<span data-ttu-id="40d6d-116">Die **CIM \_ LogicalDisk** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-116">The **CIM\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="40d6d-117">Methode</span><span class="sxs-lookup"><span data-stu-id="40d6d-117">Method</span></span>                                                                 | <span data-ttu-id="40d6d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40d6d-118">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40d6d-119">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="40d6d-119">**Reset**</span></span>](reset-method-in-class-cim-logicaldisk.md)                 | <span data-ttu-id="40d6d-120">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="40d6d-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="40d6d-121">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="40d6d-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="40d6d-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldisk.md) | <span data-ttu-id="40d6d-123">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40d6d-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="40d6d-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="40d6d-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40d6d-125">Properties</span></span>

<span data-ttu-id="40d6d-126">Die **CIM \_ LogicalDisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="40d6d-126">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40d6d-127">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="40d6d-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40d6d-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-130">Beschreibt, ob die Medien lesbar, beschreibbar oder beides sind, z. b..</span><span class="sxs-lookup"><span data-stu-id="40d6d-130">Describes whether the media is readable, writable, or both, for example.</span></span> <span data-ttu-id="40d6d-131">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40d6d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="40d6d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-133">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="40d6d-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="40d6d-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="40d6d-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-135">Lesbare.</span><span class="sxs-lookup"><span data-stu-id="40d6d-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="40d6d-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="40d6d-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-137">Beschreibbaren.</span><span class="sxs-lookup"><span data-stu-id="40d6d-137">Writable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="40d6d-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="40d6d-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-139">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="40d6d-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="40d6d-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="40d6d-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-141">Einmal schreiben.</span><span class="sxs-lookup"><span data-stu-id="40d6d-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40d6d-142">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="40d6d-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40d6d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-145">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="40d6d-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-146">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-146">Availability and status of the device.</span></span>

<span data-ttu-id="40d6d-147">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="40d6d-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="40d6d-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40d6d-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="40d6d-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="40d6d-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="40d6d-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="40d6d-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="40d6d-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="40d6d-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="40d6d-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="40d6d-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="40d6d-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="40d6d-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="40d6d-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="40d6d-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="40d6d-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="40d6d-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="40d6d-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="40d6d-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="40d6d-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="40d6d-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="40d6d-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="40d6d-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="40d6d-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="40d6d-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="40d6d-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-161">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="40d6d-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="40d6d-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-163">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="40d6d-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="40d6d-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="40d6d-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-165">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="40d6d-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="40d6d-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="40d6d-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="40d6d-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-168">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="40d6d-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="40d6d-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="40d6d-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-170">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="40d6d-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="40d6d-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="40d6d-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-172">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="40d6d-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="40d6d-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="40d6d-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-174">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="40d6d-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="40d6d-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-176">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="40d6d-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40d6d-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="40d6d-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-178">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40d6d-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-180">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="40d6d-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-181">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="40d6d-182">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-182">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="40d6d-183">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 ein.</span><span class="sxs-lookup"><span data-stu-id="40d6d-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="40d6d-184">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="40d6d-185">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="40d6d-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-186">**Caption**</span><span class="sxs-lookup"><span data-stu-id="40d6d-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-189">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="40d6d-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-190">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-190">Short textual description of the object.</span></span>

<span data-ttu-id="40d6d-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-192">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="40d6d-192">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-193">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40d6d-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-195">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="40d6d-195">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-196">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="40d6d-196">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="40d6d-197">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-197">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="40d6d-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="40d6d-199"> (0)</span><span class="sxs-lookup"><span data-stu-id="40d6d-199">(0)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-200">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="40d6d-200">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="40d6d-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="40d6d-202">(1)</span><span class="sxs-lookup"><span data-stu-id="40d6d-202">(1)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-203">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-203">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="40d6d-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="40d6d-205">(2)</span><span class="sxs-lookup"><span data-stu-id="40d6d-205">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="40d6d-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="40d6d-207">(3)</span><span class="sxs-lookup"><span data-stu-id="40d6d-207">(3)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-208">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="40d6d-208">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="40d6d-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="40d6d-210">(4)</span><span class="sxs-lookup"><span data-stu-id="40d6d-210">(4)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-211">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="40d6d-211">Device is not working properly.</span></span> <span data-ttu-id="40d6d-212">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-212">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="40d6d-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="40d6d-214">(5)</span><span class="sxs-lookup"><span data-stu-id="40d6d-214">(5)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-215">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="40d6d-215">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="40d6d-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="40d6d-217"> (6)</span><span class="sxs-lookup"><span data-stu-id="40d6d-217">(6)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-218">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="40d6d-218">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="40d6d-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="40d6d-220">(7)</span><span class="sxs-lookup"><span data-stu-id="40d6d-220">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="40d6d-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="40d6d-222">(8)</span><span class="sxs-lookup"><span data-stu-id="40d6d-222">(8)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-223">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-223">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="40d6d-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="40d6d-225">(9)</span><span class="sxs-lookup"><span data-stu-id="40d6d-225">(9)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-226">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="40d6d-226">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="40d6d-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="40d6d-228">(10)</span><span class="sxs-lookup"><span data-stu-id="40d6d-228">(10)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-229">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-229">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="40d6d-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="40d6d-231">(11)</span><span class="sxs-lookup"><span data-stu-id="40d6d-231">(11)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-232">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="40d6d-232">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="40d6d-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="40d6d-234">(12)</span><span class="sxs-lookup"><span data-stu-id="40d6d-234">(12)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-235">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-235">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="40d6d-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="40d6d-237">(13)</span><span class="sxs-lookup"><span data-stu-id="40d6d-237">(13)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-238">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-238">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="40d6d-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="40d6d-240">(14)</span><span class="sxs-lookup"><span data-stu-id="40d6d-240">(14)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-241">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="40d6d-241">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="40d6d-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="40d6d-243">(15)</span><span class="sxs-lookup"><span data-stu-id="40d6d-243">(15)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-244">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="40d6d-244">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="40d6d-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="40d6d-246">(16)</span><span class="sxs-lookup"><span data-stu-id="40d6d-246">(16)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-247">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-247">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="40d6d-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="40d6d-249">(17)</span><span class="sxs-lookup"><span data-stu-id="40d6d-249">(17)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-250">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="40d6d-250">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="40d6d-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="40d6d-252">(18)</span><span class="sxs-lookup"><span data-stu-id="40d6d-252">(18)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-253">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-253">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="40d6d-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="40d6d-255">(19)</span><span class="sxs-lookup"><span data-stu-id="40d6d-255">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="40d6d-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="40d6d-257">(20)</span><span class="sxs-lookup"><span data-stu-id="40d6d-257">(20)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-258">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-258">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="40d6d-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="40d6d-260">(21)</span><span class="sxs-lookup"><span data-stu-id="40d6d-260">(21)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-261">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="40d6d-261">System failure.</span></span> <span data-ttu-id="40d6d-262">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="40d6d-262">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="40d6d-263">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-263">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="40d6d-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="40d6d-265">(22)</span><span class="sxs-lookup"><span data-stu-id="40d6d-265">(22)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-266">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-266">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="40d6d-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="40d6d-268">(23)</span><span class="sxs-lookup"><span data-stu-id="40d6d-268">(23)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-269">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="40d6d-269">System failure.</span></span> <span data-ttu-id="40d6d-270">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="40d6d-270">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="40d6d-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="40d6d-272">(24)</span><span class="sxs-lookup"><span data-stu-id="40d6d-272">(24)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-273">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-273">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="40d6d-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="40d6d-275">(25)</span><span class="sxs-lookup"><span data-stu-id="40d6d-275">(25)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-276">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="40d6d-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="40d6d-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="40d6d-278">(26)</span><span class="sxs-lookup"><span data-stu-id="40d6d-278">(26)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-279">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="40d6d-279">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="40d6d-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="40d6d-281">(27)</span><span class="sxs-lookup"><span data-stu-id="40d6d-281">(27)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-282">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="40d6d-282">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="40d6d-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="40d6d-284">(28)</span><span class="sxs-lookup"><span data-stu-id="40d6d-284">(28)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-285">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-285">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="40d6d-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="40d6d-287">(29)</span><span class="sxs-lookup"><span data-stu-id="40d6d-287">(29)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-288">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-288">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="40d6d-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="40d6d-290">(30)</span><span class="sxs-lookup"><span data-stu-id="40d6d-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-291">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40d6d-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="40d6d-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="40d6d-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="40d6d-293">31,5</span><span class="sxs-lookup"><span data-stu-id="40d6d-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-294">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-294">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40d6d-295">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="40d6d-295">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-296">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40d6d-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-298">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="40d6d-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-299">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="40d6d-299">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="40d6d-300">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-301">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="40d6d-301">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-304">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40d6d-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-305">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40d6d-305">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="40d6d-306">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-306">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="40d6d-307">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-308">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40d6d-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-311">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="40d6d-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-312">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-312">Textual description of the object.</span></span>

<span data-ttu-id="40d6d-313">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="40d6d-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-317">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40d6d-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-318">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="40d6d-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="40d6d-319">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-320">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="40d6d-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-321">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40d6d-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-323">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="40d6d-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="40d6d-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="40d6d-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-328">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="40d6d-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="40d6d-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-330">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="40d6d-330">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-333">Eine frei Form Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, der vom Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="40d6d-333">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="40d6d-334">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-334">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-335">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="40d6d-335">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-336">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40d6d-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-338">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="40d6d-338">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-339">Der verfügbare freie Speicherplatz (in Bytes) auf dem logischen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="40d6d-339">Available free space, in bytes, on the logical disk.</span></span>

<span data-ttu-id="40d6d-340">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="40d6d-340">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-341">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="40d6d-341">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-342">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="40d6d-342">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-344">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="40d6d-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-345">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-345">Date and time the object was installed.</span></span> <span data-ttu-id="40d6d-346">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="40d6d-346">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="40d6d-347">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-348">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="40d6d-348">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-349">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40d6d-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-351">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="40d6d-351">Last error code reported by the logical device.</span></span>

<span data-ttu-id="40d6d-352">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-353">**Name**</span><span class="sxs-lookup"><span data-stu-id="40d6d-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-354">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-356">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="40d6d-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-357">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="40d6d-357">Label by which the object is known.</span></span> <span data-ttu-id="40d6d-358">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="40d6d-359">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-360">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="40d6d-360">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-361">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40d6d-361">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-363">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="40d6d-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-364">Gesamtanzahl der aufeinanderfolgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-364">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form the storage extent.</span></span> <span data-ttu-id="40d6d-365">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="40d6d-365">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="40d6d-366">Wenn der Wert der **BLOCKSIZE** -Eigenschaft 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherbereichs.</span><span class="sxs-lookup"><span data-stu-id="40d6d-366">If the value of the **BlockSize** property is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="40d6d-367">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-367">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="40d6d-368">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="40d6d-368">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-369">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="40d6d-369">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-370">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-372">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="40d6d-372">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-373">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-373">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="40d6d-374">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="40d6d-375">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="40d6d-375">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-376">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="40d6d-376">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-377">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="40d6d-377">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-379">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-379">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="40d6d-380">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-380">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40d6d-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="40d6d-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="40d6d-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="40d6d-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="40d6d-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="40d6d-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="40d6d-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="40d6d-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-385">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40d6d-385">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="40d6d-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="40d6d-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-387">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="40d6d-387">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="40d6d-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="40d6d-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-389">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-389">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="40d6d-390">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-390">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="40d6d-391">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="40d6d-391">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="40d6d-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="40d6d-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-393">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40d6d-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="40d6d-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="40d6d-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="40d6d-395">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40d6d-395">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40d6d-396">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="40d6d-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-397">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="40d6d-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-399">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="40d6d-399">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="40d6d-400">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="40d6d-400">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="40d6d-401">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-401">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="40d6d-402">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="40d6d-402">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="40d6d-403">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-404">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="40d6d-404">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-405">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-407">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-407">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="40d6d-408">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-408">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-409">**Größe**</span><span class="sxs-lookup"><span data-stu-id="40d6d-409">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-410">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40d6d-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-412">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="40d6d-412">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-413">Größe des logischen Datenträgers (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="40d6d-413">Size of the logical disk, in bytes.</span></span>

<span data-ttu-id="40d6d-414">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="40d6d-414">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-415">**Status**</span><span class="sxs-lookup"><span data-stu-id="40d6d-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-416">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-418">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="40d6d-418">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-419">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-419">Current status of the object.</span></span>

<span data-ttu-id="40d6d-420">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-420">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="40d6d-421">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="40d6d-421">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="40d6d-422">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="40d6d-422">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="40d6d-423">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="40d6d-423">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="40d6d-424">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="40d6d-424">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40d6d-425">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="40d6d-425">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="40d6d-426">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="40d6d-426">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="40d6d-427">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="40d6d-427">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="40d6d-428">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="40d6d-428">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="40d6d-429">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="40d6d-429">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="40d6d-430">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="40d6d-430">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="40d6d-431">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="40d6d-431">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="40d6d-432">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="40d6d-432">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="40d6d-433">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="40d6d-433">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40d6d-434">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="40d6d-434">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-435">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40d6d-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-437">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="40d6d-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-438">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="40d6d-438">State of the logical device.</span></span> <span data-ttu-id="40d6d-439">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40d6d-439">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="40d6d-440">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="40d6d-441">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="40d6d-441">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40d6d-442">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="40d6d-442">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="40d6d-443">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="40d6d-443">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="40d6d-444">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="40d6d-444">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="40d6d-445">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="40d6d-445">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40d6d-446">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="40d6d-446">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-447">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-449">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40d6d-449">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-450">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="40d6d-450">Scoping system's creation class name.</span></span>

<span data-ttu-id="40d6d-451">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d6d-452">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="40d6d-452">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d6d-453">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="40d6d-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-454">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="40d6d-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d6d-455">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40d6d-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40d6d-456">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="40d6d-456">Scoping system's name.</span></span>

<span data-ttu-id="40d6d-457">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="40d6d-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40d6d-458">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40d6d-458">Remarks</span></span>

<span data-ttu-id="40d6d-459">Die **CIM \_ LogicalDisk** -Klasse wird von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="40d6d-459">The **CIM\_LogicalDisk** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="40d6d-460">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="40d6d-460">WMI does not implement this class.</span></span> <span data-ttu-id="40d6d-461">Informationen zu Klassen, die von **CIM \_ LogicalDisk** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="40d6d-461">For classes derived from **CIM\_LogicalDisk**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="40d6d-462">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="40d6d-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="40d6d-463">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="40d6d-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d6d-464">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40d6d-464">Requirements</span></span>



| <span data-ttu-id="40d6d-465">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40d6d-465">Requirement</span></span> | <span data-ttu-id="40d6d-466">Wert</span><span class="sxs-lookup"><span data-stu-id="40d6d-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40d6d-467">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40d6d-467">Minimum supported client</span></span><br/> | <span data-ttu-id="40d6d-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40d6d-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40d6d-469">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40d6d-469">Minimum supported server</span></span><br/> | <span data-ttu-id="40d6d-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40d6d-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40d6d-471">Namespace</span><span class="sxs-lookup"><span data-stu-id="40d6d-471">Namespace</span></span><br/>                | <span data-ttu-id="40d6d-472">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40d6d-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40d6d-473">MOF</span><span class="sxs-lookup"><span data-stu-id="40d6d-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40d6d-474"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="40d6d-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40d6d-475">DLL</span><span class="sxs-lookup"><span data-stu-id="40d6d-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d6d-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d6d-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40d6d-477">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40d6d-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d6d-478">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="40d6d-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

