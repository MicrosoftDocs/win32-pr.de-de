---
description: Die CIM \_ -cdromdrive-Klasse stellt ein CD-ROM-Laufwerk auf dem Computer dar.
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: CIM_CDROMDrive-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499607e050124533465a40da9e73d433142e6515
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861352"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="0f658-103">CIM_CDROMDrive-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="0f658-103">CIM_CDROMDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0f658-104">Die **CIM- \_ cdromdrive** -Klasse stellt ein CD-ROM-Laufwerk auf dem Computer dar.</span><span class="sxs-lookup"><span data-stu-id="0f658-104">The **CIM\_CDROMDrive** class represents a CD-ROM drive on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="0f658-105">Der Name des Laufwerks entspricht nicht dem Buchstaben des logischen Laufwerks, das dem Gerät zugewiesen ist. Dies ist der Name des logischen Speichergeräts, das vom Laufwerk abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="0f658-105">The name of the drive does not correspond to the logical drive letter assigned to the device, which is the name of the logical storage device that is dependent on the drive.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="0f658-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0f658-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0f658-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0f658-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0f658-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0f658-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0f658-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f658-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f658-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a><span data-ttu-id="0f658-111">Member</span><span class="sxs-lookup"><span data-stu-id="0f658-111">Members</span></span>

<span data-ttu-id="0f658-112">Die **CIM- \_ cdromdrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0f658-112">The **CIM\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="0f658-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="0f658-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f658-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f658-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0f658-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="0f658-115">Methods</span></span>

<span data-ttu-id="0f658-116">Die **CIM- \_ cdromdrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0f658-116">The **CIM\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="0f658-117">Methode</span><span class="sxs-lookup"><span data-stu-id="0f658-117">Method</span></span>                                                                | <span data-ttu-id="0f658-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f658-118">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f658-119">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="0f658-119">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="0f658-120">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="0f658-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="0f658-121">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="0f658-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0f658-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0f658-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="0f658-123">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f658-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0f658-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="0f658-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0f658-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f658-125">Properties</span></span>

<span data-ttu-id="0f658-126">Die **CIM- \_ cdromdrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0f658-126">The **CIM\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f658-127">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="0f658-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f658-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-130">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="0f658-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-131">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="0f658-131">Availability and status of the device.</span></span>

<span data-ttu-id="0f658-132">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-132">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0f658-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0f658-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f658-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0f658-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0f658-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="0f658-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0f658-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="0f658-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0f658-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="0f658-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0f658-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="0f658-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0f658-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="0f658-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0f658-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="0f658-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0f658-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="0f658-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0f658-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="0f658-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0f658-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="0f658-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0f658-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="0f658-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0f658-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="0f658-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-146">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="0f658-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0f658-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="0f658-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-148">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0f658-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0f658-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="0f658-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-150">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-150">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0f658-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="0f658-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0f658-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="0f658-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-153">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="0f658-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0f658-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="0f658-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-155">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="0f658-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0f658-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="0f658-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-157">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="0f658-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0f658-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="0f658-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-159">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="0f658-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0f658-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="0f658-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-161">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="0f658-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f658-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="0f658-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-163">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0f658-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0f658-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-165">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="0f658-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-166">Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="0f658-166">Capabilities of the media access device.</span></span>

<span data-ttu-id="0f658-167">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f658-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0f658-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-169">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="0f658-169">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0f658-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0f658-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-171">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0f658-171">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="0f658-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="0f658-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-173">Sequenzieller Zugriff.</span><span class="sxs-lookup"><span data-stu-id="0f658-173">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="0f658-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="0f658-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-175">Random-Access.</span><span class="sxs-lookup"><span data-stu-id="0f658-175">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="0f658-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="0f658-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-177">Schreiben.</span><span class="sxs-lookup"><span data-stu-id="0f658-177">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="0f658-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="0f658-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-179">Verschlüsselung:</span><span class="sxs-lookup"><span data-stu-id="0f658-179">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="0f658-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="0f658-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-181">Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="0f658-181">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="0f658-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="0f658-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-183">Wechselmedien.</span><span class="sxs-lookup"><span data-stu-id="0f658-183">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="0f658-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="0f658-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-185">Manuelle Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="0f658-185">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="0f658-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="0f658-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-187">Automatische Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="0f658-187">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="0f658-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="0f658-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-189">Intelligente Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0f658-189">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="0f658-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="0f658-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-191">Unterscheidet ein Gerät, das auf beide Seiten eines zweiseitigen Mediums zugreifen kann, von einem Gerät, das nur eine einzelne Seite liest und erfordert, dass die Medien eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-191">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="0f658-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="0f658-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-193">Gibt an, dass das Medium nicht explizit vom Gerät ausworfen werden muss, bevor von einem Auswahl Element darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="0f658-193">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f658-194">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="0f658-194">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-195">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0f658-195">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f658-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-197">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="0f658-197">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-198">Array von Freiform-Zeichen folgen, das ausführliche Erläuterungen **für den Zugriff** auf Gerätefunktionen bereitstellt, die im Funktions Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0f658-198">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="0f658-199">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="0f658-199">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="0f658-200">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-200">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-201">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0f658-201">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-204">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0f658-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-205">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0f658-205">A short textual description of the object.</span></span>

<span data-ttu-id="0f658-206">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="0f658-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-210">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f658-210">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="0f658-211">Wenn es nicht möglich ist, das Komprimierungs Schema zu beschreiben (weil es unbekannt ist), verwenden Sie Folgendes: Wenn, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="0f658-211">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="0f658-212">Wenn, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="0f658-212">If , use "Compressed".</span></span> <span data-ttu-id="0f658-213">, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="0f658-213">, use "Not Compressed".</span></span>

<span data-ttu-id="0f658-214">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="0f658-215">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0f658-215">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="0f658-216">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0f658-216">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="0f658-217">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="0f658-217">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="0f658-218">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0f658-218">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="0f658-219">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="0f658-219">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="0f658-220">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="0f658-220">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f658-221">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="0f658-221">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-222">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f658-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-224">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0f658-224">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-225">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0f658-225">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0f658-226">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-226">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0f658-227">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="0f658-227">**This device is working properly.**</span></span> <span data-ttu-id="0f658-228"> (0)</span><span class="sxs-lookup"><span data-stu-id="0f658-228">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0f658-229">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="0f658-229">**This device is not configured correctly.**</span></span> <span data-ttu-id="0f658-230">(1)</span><span class="sxs-lookup"><span data-stu-id="0f658-230">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0f658-231">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="0f658-231">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0f658-232">(2)</span><span class="sxs-lookup"><span data-stu-id="0f658-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0f658-233">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="0f658-233">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0f658-234">(3)</span><span class="sxs-lookup"><span data-stu-id="0f658-234">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0f658-235">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="0f658-235">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0f658-236">(4)</span><span class="sxs-lookup"><span data-stu-id="0f658-236">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0f658-237">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="0f658-237">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0f658-238">(5)</span><span class="sxs-lookup"><span data-stu-id="0f658-238">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0f658-239">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="0f658-239">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0f658-240"> (6)</span><span class="sxs-lookup"><span data-stu-id="0f658-240">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0f658-241">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="0f658-241">**Cannot filter.**</span></span> <span data-ttu-id="0f658-242">(7)</span><span class="sxs-lookup"><span data-stu-id="0f658-242">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0f658-243">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="0f658-243">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0f658-244">(8)</span><span class="sxs-lookup"><span data-stu-id="0f658-244">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0f658-245">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="0f658-245">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0f658-246">(9)</span><span class="sxs-lookup"><span data-stu-id="0f658-246">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0f658-247">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="0f658-247">**This device cannot start.**</span></span> <span data-ttu-id="0f658-248">(10)</span><span class="sxs-lookup"><span data-stu-id="0f658-248">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0f658-249">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="0f658-249">**This device failed.**</span></span> <span data-ttu-id="0f658-250">(11)</span><span class="sxs-lookup"><span data-stu-id="0f658-250">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0f658-251">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="0f658-251">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0f658-252">(12)</span><span class="sxs-lookup"><span data-stu-id="0f658-252">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0f658-253">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="0f658-253">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0f658-254">(13)</span><span class="sxs-lookup"><span data-stu-id="0f658-254">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0f658-255">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="0f658-255">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0f658-256">(14)</span><span class="sxs-lookup"><span data-stu-id="0f658-256">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0f658-257">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="0f658-257">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0f658-258">(15)</span><span class="sxs-lookup"><span data-stu-id="0f658-258">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0f658-259">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="0f658-259">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0f658-260">(16)</span><span class="sxs-lookup"><span data-stu-id="0f658-260">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0f658-261">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="0f658-261">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0f658-262">(17)</span><span class="sxs-lookup"><span data-stu-id="0f658-262">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0f658-263">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="0f658-263">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0f658-264">(18)</span><span class="sxs-lookup"><span data-stu-id="0f658-264">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0f658-265">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="0f658-265">**Failure using the VxD loader.**</span></span> <span data-ttu-id="0f658-266">(19)</span><span class="sxs-lookup"><span data-stu-id="0f658-266">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0f658-267">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="0f658-267">**Your registry might be corrupted.**</span></span> <span data-ttu-id="0f658-268">(20)</span><span class="sxs-lookup"><span data-stu-id="0f658-268">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0f658-269">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="0f658-269">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0f658-270">(21)</span><span class="sxs-lookup"><span data-stu-id="0f658-270">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0f658-271">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="0f658-271">**This device is disabled.**</span></span> <span data-ttu-id="0f658-272">(22)</span><span class="sxs-lookup"><span data-stu-id="0f658-272">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0f658-273">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="0f658-273">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0f658-274">(23)</span><span class="sxs-lookup"><span data-stu-id="0f658-274">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0f658-275">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="0f658-275">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0f658-276">(24)</span><span class="sxs-lookup"><span data-stu-id="0f658-276">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0f658-277">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="0f658-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0f658-278">(25)</span><span class="sxs-lookup"><span data-stu-id="0f658-278">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0f658-279">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="0f658-279">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0f658-280">(26)</span><span class="sxs-lookup"><span data-stu-id="0f658-280">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0f658-281">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="0f658-281">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0f658-282">(27)</span><span class="sxs-lookup"><span data-stu-id="0f658-282">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0f658-283">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="0f658-283">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0f658-284">(28)</span><span class="sxs-lookup"><span data-stu-id="0f658-284">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0f658-285">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="0f658-285">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0f658-286">(29)</span><span class="sxs-lookup"><span data-stu-id="0f658-286">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0f658-287">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="0f658-287">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0f658-288">(30)</span><span class="sxs-lookup"><span data-stu-id="0f658-288">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0f658-289">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="0f658-289">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0f658-290">31,5</span><span class="sxs-lookup"><span data-stu-id="0f658-290">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f658-291">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="0f658-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-292">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0f658-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-294">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0f658-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-295">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f658-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0f658-296">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-297">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0f658-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-300">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f658-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f658-301">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0f658-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0f658-302">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0f658-303">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-304">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="0f658-304">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-305">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0f658-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-307">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="0f658-307">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-308">Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="0f658-308">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="0f658-309">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0f658-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0f658-310">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-310">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-311">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f658-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-314">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0f658-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-315">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0f658-315">A textual description of the object.</span></span>

<span data-ttu-id="0f658-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0f658-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-320">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f658-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f658-321">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="0f658-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0f658-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-323">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="0f658-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-324">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0f658-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-326">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0f658-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0f658-327">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0f658-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-331">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="0f658-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0f658-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-333">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="0f658-333">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-336">Eine frei Form Zeichenfolge, die die vom Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0f658-336">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="0f658-337">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0f658-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-339">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f658-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-341">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="0f658-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-342">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0f658-342">Indicates when the object was installed.</span></span> <span data-ttu-id="0f658-343">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f658-343">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0f658-344">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0f658-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-346">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f658-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-348">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0f658-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0f658-349">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-350">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="0f658-350">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-351">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0f658-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-353">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="0f658-353">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-354">Maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="0f658-354">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="0f658-355">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0f658-355">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0f658-356">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-356">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-357">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="0f658-357">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-358">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0f658-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-360">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="0f658-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-361">Maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="0f658-361">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="0f658-362">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="0f658-362">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="0f658-363">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0f658-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0f658-364">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-364">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-365">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="0f658-365">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-366">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0f658-366">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-368">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="0f658-368">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-369">Minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="0f658-369">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="0f658-370">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0f658-370">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0f658-371">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-371">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-372">**Name**</span><span class="sxs-lookup"><span data-stu-id="0f658-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-375">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0f658-375">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-376">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0f658-376">Label by which the object is known.</span></span> <span data-ttu-id="0f658-377">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-377">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0f658-378">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-379">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="0f658-379">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-380">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0f658-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-382">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0f658-382">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="0f658-383">Ob eine manuelle oder automatische Bereinigung möglich ist, wird in der **Funktionen** -Array-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="0f658-383">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="0f658-384">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-385">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="0f658-385">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-386">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f658-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-388">Maximale Anzahl von mehreren einzelnen Medien, die unterstützt oder eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="0f658-388">Maximum number of multiple individual media that can be supported or inserted.</span></span>

<span data-ttu-id="0f658-389">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-390">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0f658-390">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-393">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0f658-393">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-394">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="0f658-394">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0f658-395">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0f658-395">Example: "\*PNP030b"</span></span>

<span data-ttu-id="0f658-396">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-397">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="0f658-397">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-398">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0f658-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0f658-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-400">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="0f658-400">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="0f658-401">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f658-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0f658-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-403">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="0f658-403">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0f658-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="0f658-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-405">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f658-405">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0f658-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="0f658-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-407">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f658-407">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0f658-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="0f658-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-409">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0f658-409">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0f658-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="0f658-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-411">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="0f658-411">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0f658-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="0f658-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-413">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0f658-413">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="0f658-414">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-414">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="0f658-415">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0f658-415">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0f658-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="0f658-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-417">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="0f658-417">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0f658-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="0f658-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0f658-419">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0f658-419">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f658-420">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="0f658-420">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-421">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0f658-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f658-423">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="0f658-423">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0f658-424">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="0f658-424">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0f658-425">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-425">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0f658-426">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="0f658-426">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0f658-427">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-428">**Status**</span><span class="sxs-lookup"><span data-stu-id="0f658-428">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-429">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-431">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0f658-431">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-432">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="0f658-432">String that indicates the current status of the object.</span></span> <span data-ttu-id="0f658-433">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-433">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0f658-434">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f658-434">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0f658-435">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="0f658-435">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0f658-436">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f658-436">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0f658-437">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0f658-437">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0f658-438">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="0f658-438">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0f658-439">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0f658-440">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="0f658-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0f658-441">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0f658-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0f658-442">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="0f658-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0f658-443">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="0f658-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f658-444">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0f658-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0f658-445">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0f658-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0f658-446">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="0f658-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0f658-447">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="0f658-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0f658-448">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="0f658-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0f658-449">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="0f658-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0f658-450">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="0f658-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0f658-451">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="0f658-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0f658-452">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="0f658-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f658-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0f658-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-454">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f658-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-456">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0f658-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0f658-457">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="0f658-457">State of the logical device.</span></span> <span data-ttu-id="0f658-458">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f658-458">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="0f658-459">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0f658-460">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0f658-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f658-461">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0f658-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0f658-462">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="0f658-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0f658-463">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="0f658-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0f658-464">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="0f658-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f658-465">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="0f658-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-466">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-467">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-468">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f658-468">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f658-469">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="0f658-469">The scoping system's creation class name.</span></span>

<span data-ttu-id="0f658-470">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f658-471">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="0f658-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f658-472">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f658-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f658-473">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f658-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f658-474">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f658-474">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f658-475">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="0f658-475">The scoping system's name.</span></span>

<span data-ttu-id="0f658-476">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0f658-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f658-477">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f658-477">Remarks</span></span>

<span data-ttu-id="0f658-478">Die **CIM- \_ cdromdrive** -Klasse wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0f658-478">The **CIM\_CDROMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0f658-479">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0f658-479">WMI does not implement this class.</span></span> <span data-ttu-id="0f658-480">Weitere Informationen zu Klassen, die von **CIM \_ cdromdrive** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0f658-480">For more information about classes derived from **CIM\_CDROMDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0f658-481">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0f658-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0f658-482">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0f658-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f658-483">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f658-483">Requirements</span></span>



| <span data-ttu-id="0f658-484">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f658-484">Requirement</span></span> | <span data-ttu-id="0f658-485">Wert</span><span class="sxs-lookup"><span data-stu-id="0f658-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f658-486">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f658-486">Minimum supported client</span></span><br/> | <span data-ttu-id="0f658-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f658-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f658-488">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f658-488">Minimum supported server</span></span><br/> | <span data-ttu-id="0f658-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f658-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f658-490">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f658-490">Namespace</span></span><br/>                | <span data-ttu-id="0f658-491">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0f658-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f658-492">MOF</span><span class="sxs-lookup"><span data-stu-id="0f658-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f658-493"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0f658-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f658-494">DLL</span><span class="sxs-lookup"><span data-stu-id="0f658-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f658-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f658-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f658-496">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f658-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f658-497">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="0f658-497">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

