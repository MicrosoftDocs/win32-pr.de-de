---
description: Die CIM \_ -Klasse "Wormdrive" stellt die Funktionen und die Verwaltung eines Wurm Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.
ms.assetid: df77084a-01f2-4cca-b395-d74ee64ef526
ms.tgt_platform: multiple
title: CIM_WORMDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WORMDrive
- CIM_WORMDrive.Availability
- CIM_WORMDrive.Capabilities
- CIM_WORMDrive.CapabilityDescriptions
- CIM_WORMDrive.Caption
- CIM_WORMDrive.CompressionMethod
- CIM_WORMDrive.ConfigManagerErrorCode
- CIM_WORMDrive.ConfigManagerUserConfig
- CIM_WORMDrive.CreationClassName
- CIM_WORMDrive.DefaultBlockSize
- CIM_WORMDrive.Description
- CIM_WORMDrive.DeviceID
- CIM_WORMDrive.ErrorCleared
- CIM_WORMDrive.ErrorDescription
- CIM_WORMDrive.ErrorMethodology
- CIM_WORMDrive.InstallDate
- CIM_WORMDrive.LastErrorCode
- CIM_WORMDrive.MaxBlockSize
- CIM_WORMDrive.MaxMediaSize
- CIM_WORMDrive.MinBlockSize
- CIM_WORMDrive.Name
- CIM_WORMDrive.NeedsCleaning
- CIM_WORMDrive.NumberOfMediaSupported
- CIM_WORMDrive.PNPDeviceID
- CIM_WORMDrive.PowerManagementCapabilities
- CIM_WORMDrive.PowerManagementSupported
- CIM_WORMDrive.Status
- CIM_WORMDrive.StatusInfo
- CIM_WORMDrive.SystemCreationClassName
- CIM_WORMDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 08133d1abdcb6fc401ee4ad730d82ef97fb30200
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126122"
---
# <a name="cim_wormdrive-class"></a><span data-ttu-id="b8141-103">CIM- \_ Klasse "Wormdrive"</span><span class="sxs-lookup"><span data-stu-id="b8141-103">CIM\_WORMDrive class</span></span>

<span data-ttu-id="b8141-104">Die CIM-Klasse " **\_ Wormdrive** " stellt die Funktionen und die Verwaltung eines Wurm Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="b8141-104">The **CIM\_WORMDrive** class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8141-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8141-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8141-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8141-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b8141-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b8141-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b8141-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8141-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8141-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FFB58B9A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_WORMDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="b8141-110">Member</span><span class="sxs-lookup"><span data-stu-id="b8141-110">Members</span></span>

<span data-ttu-id="b8141-111">Die CIM-Klasse " **\_ Wormdrive** " hat folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b8141-111">The **CIM\_WORMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b8141-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="b8141-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8141-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8141-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8141-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="b8141-114">Methods</span></span>

<span data-ttu-id="b8141-115">Die CIM-Klasse " **\_ Wormdrive** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b8141-115">The **CIM\_WORMDrive** class has these methods.</span></span>



| <span data-ttu-id="b8141-116">Methode</span><span class="sxs-lookup"><span data-stu-id="b8141-116">Method</span></span>                                                               | <span data-ttu-id="b8141-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8141-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8141-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="b8141-118">**Reset**</span></span>](reset-method-in-class-cim-wormdrive.md)                 | <span data-ttu-id="b8141-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="b8141-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b8141-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="b8141-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b8141-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b8141-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-wormdrive.md) | <span data-ttu-id="b8141-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8141-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b8141-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="b8141-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8141-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8141-124">Properties</span></span>

<span data-ttu-id="b8141-125">Die CIM-Klasse " **\_ Wormdrive** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b8141-125">The **CIM\_WORMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8141-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="b8141-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8141-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="b8141-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="b8141-130">Availability and status of the device.</span></span>

<span data-ttu-id="b8141-131">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8141-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b8141-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8141-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b8141-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b8141-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="b8141-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-135">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="b8141-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b8141-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="b8141-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b8141-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="b8141-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b8141-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="b8141-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b8141-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="b8141-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b8141-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="b8141-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b8141-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b8141-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8141-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="b8141-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b8141-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="b8141-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b8141-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="b8141-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b8141-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="b8141-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-146">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="b8141-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b8141-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="b8141-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-148">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b8141-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b8141-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b8141-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-150">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b8141-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="b8141-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b8141-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="b8141-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-153">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="b8141-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b8141-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="b8141-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-155">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="b8141-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b8141-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="b8141-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-157">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="b8141-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b8141-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="b8141-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-159">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b8141-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b8141-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="b8141-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-161">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="b8141-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8141-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="b8141-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-163">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b8141-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8141-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-165">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="b8141-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-166">Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="b8141-166">Capabilities of the media access device.</span></span> <span data-ttu-id="b8141-167">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8141-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b8141-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8141-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b8141-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="b8141-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="b8141-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="b8141-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="b8141-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="b8141-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="b8141-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="b8141-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="b8141-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="b8141-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="b8141-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="b8141-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="b8141-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-176">Wechselmedien.</span><span class="sxs-lookup"><span data-stu-id="b8141-176">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="b8141-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="b8141-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="b8141-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="b8141-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="b8141-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="b8141-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="b8141-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="b8141-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-181">Unterscheidet ein Gerät, das auf beide Seiten eines zweiseitigen Mediums zugreifen kann, von einem Gerät, das nur eine einzelne Seite liest und erfordert, dass die Medien eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-181">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="b8141-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="b8141-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-183">Gibt an, dass das Medium nicht explizit vom Gerät ausworfen werden muss, bevor von einem Auswahl Element darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="b8141-183">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8141-184">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="b8141-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-185">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b8141-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8141-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-187">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="b8141-187">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-188">Freiform-Zeichen folgen, die ausführliche Beschreibungen der Features des Zugriffs Geräts bereitstellen, die im **Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="b8141-188">Free-form strings that provide detailed descriptions for the access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="b8141-189">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="b8141-189">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="b8141-190">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-190">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-191">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b8141-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-194">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b8141-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-195">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b8141-195">Short textual description of the object.</span></span>

<span data-ttu-id="b8141-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-197">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="b8141-197">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-200">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8141-200">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="b8141-201">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="b8141-201">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="b8141-202">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="b8141-202">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="b8141-203">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="b8141-203">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="b8141-204">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-204">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="b8141-205">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b8141-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="b8141-206">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b8141-206">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="b8141-207">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="b8141-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b8141-208">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b8141-208">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="b8141-209">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="b8141-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b8141-210">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="b8141-210">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8141-211">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="b8141-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-212">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8141-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-214">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b8141-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-215">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b8141-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b8141-216">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b8141-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="b8141-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b8141-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="b8141-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-219">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b8141-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b8141-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="b8141-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b8141-221">(1)</span><span class="sxs-lookup"><span data-stu-id="b8141-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-222">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b8141-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b8141-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="b8141-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b8141-224">(2)</span><span class="sxs-lookup"><span data-stu-id="b8141-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b8141-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="b8141-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b8141-226">(3)</span><span class="sxs-lookup"><span data-stu-id="b8141-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-227">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b8141-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b8141-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="b8141-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b8141-229">(4)</span><span class="sxs-lookup"><span data-stu-id="b8141-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-230">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b8141-230">Device is not working properly.</span></span> <span data-ttu-id="b8141-231">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b8141-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b8141-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="b8141-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b8141-233">(5)</span><span class="sxs-lookup"><span data-stu-id="b8141-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-234">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8141-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b8141-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="b8141-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b8141-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="b8141-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-237">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="b8141-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b8141-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="b8141-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b8141-239">(7)</span><span class="sxs-lookup"><span data-stu-id="b8141-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b8141-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="b8141-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b8141-241">(8)</span><span class="sxs-lookup"><span data-stu-id="b8141-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-242">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="b8141-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b8141-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="b8141-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b8141-244">(9)</span><span class="sxs-lookup"><span data-stu-id="b8141-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-245">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b8141-245">Device is not working properly.</span></span> <span data-ttu-id="b8141-246">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="b8141-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b8141-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="b8141-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b8141-248">(10)</span><span class="sxs-lookup"><span data-stu-id="b8141-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-249">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b8141-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="b8141-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b8141-251">(11)</span><span class="sxs-lookup"><span data-stu-id="b8141-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-252">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="b8141-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b8141-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="b8141-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b8141-254">(12)</span><span class="sxs-lookup"><span data-stu-id="b8141-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-255">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="b8141-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b8141-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="b8141-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b8141-257">(13)</span><span class="sxs-lookup"><span data-stu-id="b8141-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-258">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b8141-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="b8141-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b8141-260">(14)</span><span class="sxs-lookup"><span data-stu-id="b8141-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-261">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b8141-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b8141-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="b8141-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b8141-263">(15)</span><span class="sxs-lookup"><span data-stu-id="b8141-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-264">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b8141-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b8141-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="b8141-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b8141-266">(16)</span><span class="sxs-lookup"><span data-stu-id="b8141-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-267">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b8141-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="b8141-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b8141-269">(17)</span><span class="sxs-lookup"><span data-stu-id="b8141-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-270">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="b8141-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b8141-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="b8141-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b8141-272">(18)</span><span class="sxs-lookup"><span data-stu-id="b8141-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-273">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b8141-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="b8141-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b8141-275">(19)</span><span class="sxs-lookup"><span data-stu-id="b8141-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b8141-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="b8141-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b8141-277">(20)</span><span class="sxs-lookup"><span data-stu-id="b8141-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-278">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b8141-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b8141-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="b8141-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b8141-280">(21)</span><span class="sxs-lookup"><span data-stu-id="b8141-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-281">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="b8141-281">System failure.</span></span> <span data-ttu-id="b8141-282">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b8141-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b8141-283">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="b8141-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b8141-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="b8141-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b8141-285">(22)</span><span class="sxs-lookup"><span data-stu-id="b8141-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-286">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8141-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b8141-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="b8141-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b8141-288">(23)</span><span class="sxs-lookup"><span data-stu-id="b8141-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-289">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="b8141-289">System failure.</span></span> <span data-ttu-id="b8141-290">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b8141-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b8141-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="b8141-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b8141-292">(24)</span><span class="sxs-lookup"><span data-stu-id="b8141-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-293">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="b8141-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b8141-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="b8141-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b8141-295">(25)</span><span class="sxs-lookup"><span data-stu-id="b8141-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-296">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b8141-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b8141-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="b8141-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b8141-298">(26)</span><span class="sxs-lookup"><span data-stu-id="b8141-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-299">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b8141-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b8141-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="b8141-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b8141-301">(27)</span><span class="sxs-lookup"><span data-stu-id="b8141-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-302">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8141-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b8141-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="b8141-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b8141-304">(28)</span><span class="sxs-lookup"><span data-stu-id="b8141-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-305">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="b8141-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b8141-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="b8141-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b8141-307">(29)</span><span class="sxs-lookup"><span data-stu-id="b8141-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-308">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8141-308">Device is disabled.</span></span> <span data-ttu-id="b8141-309">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b8141-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b8141-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="b8141-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b8141-311">(30)</span><span class="sxs-lookup"><span data-stu-id="b8141-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-312">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8141-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b8141-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="b8141-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b8141-314">31,5</span><span class="sxs-lookup"><span data-stu-id="b8141-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-315">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b8141-315">Device is not working properly.</span></span> <span data-ttu-id="b8141-316">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8141-317">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="b8141-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-318">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8141-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-320">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b8141-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-321">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8141-321">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b8141-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-323">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="b8141-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-326">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8141-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8141-327">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8141-327">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b8141-328">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-328">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b8141-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-330">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="b8141-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-331">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8141-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-333">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="b8141-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-334">Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="b8141-334">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="b8141-335">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b8141-336">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8141-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-337">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8141-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-340">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b8141-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-341">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b8141-341">Textual description of the object.</span></span>

<span data-ttu-id="b8141-342">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b8141-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-346">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8141-346">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8141-347">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="b8141-347">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b8141-348">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-349">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="b8141-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-350">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8141-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-352">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b8141-352">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b8141-353">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b8141-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-357">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="b8141-357">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b8141-358">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-359">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="b8141-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-362">Eine frei Form Zeichenfolge, die die vom Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b8141-362">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="b8141-363">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-364">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8141-364">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-365">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8141-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-367">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="b8141-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-368">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b8141-368">Date and time the object was installed.</span></span> <span data-ttu-id="b8141-369">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b8141-369">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b8141-370">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-371">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b8141-371">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-372">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8141-372">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-374">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b8141-374">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b8141-375">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-376">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="b8141-376">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-377">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8141-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-379">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="b8141-379">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-380">Maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="b8141-380">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b8141-381">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-381">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b8141-382">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8141-382">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-383">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="b8141-383">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-384">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8141-384">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-386">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="b8141-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-387">Maximale Größe des vom Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="b8141-387">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="b8141-388">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="b8141-388">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="b8141-389">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b8141-390">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8141-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-391">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="b8141-391">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-392">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8141-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-394">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="b8141-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-395">Minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="b8141-395">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b8141-396">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b8141-397">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8141-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-398">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8141-398">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-399">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-401">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b8141-401">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-402">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b8141-402">Label by which the object is known.</span></span> <span data-ttu-id="b8141-403">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-403">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b8141-404">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-405">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="b8141-405">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-406">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8141-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-408">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="b8141-408">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="b8141-409">Ob eine manuelle oder automatische Bereinigung möglich ist, wird in der **Funktionen** -Array-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8141-409">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="b8141-410">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-410">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-411">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="b8141-411">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-412">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8141-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-414">Wenn das Medien Zugriffsgerät mehrere einzelne Medien unterstützt, definiert diese Eigenschaft die maximale Anzahl, die unterstützt oder eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8141-414">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="b8141-415">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-415">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-416">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b8141-416">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-417">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-419">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b8141-419">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-420">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b8141-420">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b8141-421">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b8141-422">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b8141-422">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b8141-423">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="b8141-423">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-424">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b8141-424">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8141-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-426">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b8141-426">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b8141-427">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-427">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8141-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b8141-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b8141-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b8141-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-430">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8141-430">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b8141-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="b8141-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b8141-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b8141-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-433">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8141-433">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b8141-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="b8141-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-435">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="b8141-435">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b8141-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="b8141-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-437">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8141-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b8141-438">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-438">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b8141-439">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b8141-439">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b8141-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="b8141-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-441">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b8141-441">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b8141-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="b8141-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b8141-443">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b8141-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8141-444">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="b8141-444">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-445">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8141-445">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8141-447">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b8141-447">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b8141-448">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="b8141-448">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b8141-449">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-449">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b8141-450">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="b8141-450">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b8141-451">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-452">**Status**</span><span class="sxs-lookup"><span data-stu-id="b8141-452">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-453">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-454">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-455">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b8141-455">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-456">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b8141-456">Current status of the object.</span></span> <span data-ttu-id="b8141-457">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8141-458">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="b8141-458">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b8141-459">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b8141-459">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b8141-460">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="b8141-460">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8141-461">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="b8141-461">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8141-462">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b8141-462">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b8141-463">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b8141-463">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b8141-464">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="b8141-464">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b8141-465">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="b8141-465">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b8141-466">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="b8141-466">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b8141-467">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="b8141-467">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b8141-468">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="b8141-468">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b8141-469">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="b8141-469">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b8141-470">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="b8141-470">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8141-471">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b8141-471">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-472">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8141-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-473">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-474">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b8141-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b8141-475">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b8141-475">State of the logical device.</span></span> <span data-ttu-id="b8141-476">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8141-476">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b8141-477">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8141-478">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b8141-478">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8141-479">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b8141-479">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b8141-480">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b8141-480">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b8141-481">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="b8141-481">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b8141-482">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="b8141-482">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8141-483">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="b8141-483">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-484">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-485">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-486">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8141-486">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8141-487">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="b8141-487">Scoping system's creation class name.</span></span>

<span data-ttu-id="b8141-488">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-488">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8141-489">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="b8141-489">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8141-490">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8141-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8141-491">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8141-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8141-492">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8141-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8141-493">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="b8141-493">Scoping system's name.</span></span>

<span data-ttu-id="b8141-494">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8141-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8141-495">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8141-495">Remarks</span></span>

<span data-ttu-id="b8141-496">Die CIM-Klasse " **\_ Wormdrive** " ist von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b8141-496">The **CIM\_WORMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b8141-497">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b8141-497">WMI does not implement this class.</span></span>

<span data-ttu-id="b8141-498">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b8141-498">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8141-499">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b8141-499">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8141-500">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8141-500">Requirements</span></span>



| <span data-ttu-id="b8141-501">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8141-501">Requirement</span></span> | <span data-ttu-id="b8141-502">Wert</span><span class="sxs-lookup"><span data-stu-id="b8141-502">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8141-503">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8141-503">Minimum supported client</span></span><br/> | <span data-ttu-id="b8141-504">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8141-504">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8141-505">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8141-505">Minimum supported server</span></span><br/> | <span data-ttu-id="b8141-506">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8141-506">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8141-507">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8141-507">Namespace</span></span><br/>                | <span data-ttu-id="b8141-508">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b8141-508">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8141-509">MOF</span><span class="sxs-lookup"><span data-stu-id="b8141-509">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8141-510"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b8141-510"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8141-511">DLL</span><span class="sxs-lookup"><span data-stu-id="b8141-511">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8141-512"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8141-512"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8141-513">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8141-513">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8141-514">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="b8141-514">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

