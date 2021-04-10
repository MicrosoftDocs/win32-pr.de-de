---
description: Die CIM \_ diskdrive-Klasse stellt ein physisches Laufwerk dar, das vom Betriebssystem erkannt wird.
ms.assetid: 3a63506e-455e-4108-b0c7-03b2af249d61
ms.tgt_platform: multiple
title: CIM_DiskDrive-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive
- CIM_DiskDrive.Availability
- CIM_DiskDrive.Capabilities
- CIM_DiskDrive.CapabilityDescriptions
- CIM_DiskDrive.Caption
- CIM_DiskDrive.CompressionMethod
- CIM_DiskDrive.ConfigManagerErrorCode
- CIM_DiskDrive.ConfigManagerUserConfig
- CIM_DiskDrive.CreationClassName
- CIM_DiskDrive.DefaultBlockSize
- CIM_DiskDrive.Description
- CIM_DiskDrive.DeviceID
- CIM_DiskDrive.ErrorCleared
- CIM_DiskDrive.ErrorDescription
- CIM_DiskDrive.ErrorMethodology
- CIM_DiskDrive.InstallDate
- CIM_DiskDrive.LastErrorCode
- CIM_DiskDrive.MaxBlockSize
- CIM_DiskDrive.MaxMediaSize
- CIM_DiskDrive.MinBlockSize
- CIM_DiskDrive.Name
- CIM_DiskDrive.NeedsCleaning
- CIM_DiskDrive.NumberOfMediaSupported
- CIM_DiskDrive.PNPDeviceID
- CIM_DiskDrive.PowerManagementCapabilities
- CIM_DiskDrive.PowerManagementSupported
- CIM_DiskDrive.Status
- CIM_DiskDrive.StatusInfo
- CIM_DiskDrive.SystemCreationClassName
- CIM_DiskDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c68e8fc53898220737f473cc0c13f43d7ad471b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214228"
---
# <a name="cim_diskdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="52fe5-103">CIM_DiskDrive-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="52fe5-103">CIM_DiskDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="52fe5-104">Die **CIM \_ diskdrive** -Klasse stellt ein physisches Laufwerk dar, das vom Betriebssystem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="52fe5-104">The **CIM\_DiskDrive** class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="52fe5-105">Die Festplattenlaufwerke entsprechen den logischen und Verwaltungs Merkmalen des Laufwerks, und in manchen Fällen werden die physischen Merkmale des Geräts möglicherweise nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-105">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="52fe5-106">Eine Schnittstelle zu einem physischen Laufwerk ist ein Member dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="52fe5-106">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="52fe5-107">Ein Objekt, das auf einem anderen logischen Gerät basiert, ist jedoch kein Member dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="52fe5-107">However, an object based on another logical device is not a member of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52fe5-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="52fe5-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="52fe5-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="52fe5-110">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="52fe5-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="52fe5-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="52fe5-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="52fe5-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="52fe5-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="52fe5-113">Member</span><span class="sxs-lookup"><span data-stu-id="52fe5-113">Members</span></span>

<span data-ttu-id="52fe5-114">Die **CIM \_ diskdrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52fe5-114">The **CIM\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="52fe5-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="52fe5-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="52fe5-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52fe5-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="52fe5-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="52fe5-117">Methods</span></span>

<span data-ttu-id="52fe5-118">Die **CIM \_ diskdrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-118">The **CIM\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="52fe5-119">Methode</span><span class="sxs-lookup"><span data-stu-id="52fe5-119">Method</span></span>                                                                | <span data-ttu-id="52fe5-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52fe5-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52fe5-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="52fe5-121">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="52fe5-122">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="52fe5-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="52fe5-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="52fe5-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="52fe5-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="52fe5-125">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52fe5-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="52fe5-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="52fe5-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52fe5-127">Properties</span></span>

<span data-ttu-id="52fe5-128">Die **CIM \_ diskdrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52fe5-128">The **CIM\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52fe5-129">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="52fe5-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52fe5-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-132">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="52fe5-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-133">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-133">Availability and status of the device.</span></span>

<span data-ttu-id="52fe5-134">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="52fe5-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="52fe5-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-136">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="52fe5-136">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52fe5-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="52fe5-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-138">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="52fe5-138">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="52fe5-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="52fe5-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-140">Ausführung/volle Leistung.</span><span class="sxs-lookup"><span data-stu-id="52fe5-140">Running/full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="52fe5-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="52fe5-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-142">Warnung.</span><span class="sxs-lookup"><span data-stu-id="52fe5-142">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="52fe5-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="52fe5-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-144">Tests.</span><span class="sxs-lookup"><span data-stu-id="52fe5-144">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="52fe5-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="52fe5-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="52fe5-146">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="52fe5-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="52fe5-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-148">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="52fe5-148">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="52fe5-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="52fe5-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="52fe5-150">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="52fe5-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="52fe5-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-152">Off-Duty.</span><span class="sxs-lookup"><span data-stu-id="52fe5-152">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="52fe5-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="52fe5-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-154">Heruntergestuft.</span><span class="sxs-lookup"><span data-stu-id="52fe5-154">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="52fe5-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="52fe5-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-156">Nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-156">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="52fe5-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="52fe5-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-158">Installationsfehler.</span><span class="sxs-lookup"><span data-stu-id="52fe5-158">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="52fe5-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="52fe5-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-160">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status in diesem Modus ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-160">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="52fe5-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="52fe5-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-162">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="52fe5-162">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="52fe5-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="52fe5-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-164">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-164">Device is not functioning but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="52fe5-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="52fe5-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-166">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="52fe5-166">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="52fe5-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="52fe5-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-168">Das Gerät befindet sich in einem Warn Status und auch in einem Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="52fe5-168">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="52fe5-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="52fe5-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-170">Angehalten.</span><span class="sxs-lookup"><span data-stu-id="52fe5-170">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="52fe5-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="52fe5-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-172">Nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="52fe5-172">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="52fe5-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="52fe5-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-174">Nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="52fe5-174">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="52fe5-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="52fe5-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-176">Das Laufwerk ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52fe5-176">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52fe5-177">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="52fe5-177">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-178">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="52fe5-178">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-180">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="52fe5-180">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-181">Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-181">Capabilities of the media access device.</span></span> <span data-ttu-id="52fe5-182">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-182">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52fe5-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="52fe5-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-184">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="52fe5-184">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="52fe5-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="52fe5-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-186">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="52fe5-186">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="52fe5-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="52fe5-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-188">Sequenzieller Zugriff.</span><span class="sxs-lookup"><span data-stu-id="52fe5-188">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="52fe5-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="52fe5-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-190">Random-Access.</span><span class="sxs-lookup"><span data-stu-id="52fe5-190">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="52fe5-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="52fe5-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-192">Schreiben.</span><span class="sxs-lookup"><span data-stu-id="52fe5-192">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="52fe5-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="52fe5-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-194">Verschlüsselung:</span><span class="sxs-lookup"><span data-stu-id="52fe5-194">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="52fe5-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="52fe5-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-196">Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="52fe5-196">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="52fe5-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="52fe5-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-198">Wechselmedien.</span><span class="sxs-lookup"><span data-stu-id="52fe5-198">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="52fe5-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="52fe5-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-200">Manuelle Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="52fe5-200">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="52fe5-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="52fe5-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-202">Automatische Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="52fe5-202">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="52fe5-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="52fe5-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-204">Intelligente Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="52fe5-204">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="52fe5-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="52fe5-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-206">Unterscheidet ein Gerät, das auf beide Seiten eines zweiseitigen Mediums zugreifen kann, von einem Gerät, das nur eine einzelne Seite liest und erfordert, dass die Medien eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-206">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="52fe5-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="52fe5-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-208">Gibt an, dass das Medium nicht explizit vom Gerät ausworfen werden muss, bevor von einem Auswahl Element darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="52fe5-208">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52fe5-209">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="52fe5-209">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-210">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="52fe5-210">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-212">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="52fe5-212">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-213">Array von Freiform-Zeichen folgen, die ausführliche Erläuterungen **für den Zugriff** auf Gerätefunktionen bereitstellen, die im Funktions Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="52fe5-213">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="52fe5-214">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

> [!Note]  
> <span data-ttu-id="52fe5-215">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="52fe5-215">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="52fe5-216">**Caption**</span><span class="sxs-lookup"><span data-stu-id="52fe5-216">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-219">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="52fe5-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-220">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-220">Short textual description of the object.</span></span>

<span data-ttu-id="52fe5-221">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-222">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="52fe5-222">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-225">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52fe5-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="52fe5-226">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="52fe5-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="52fe5-227">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="52fe5-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="52fe5-228">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="52fe5-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="52fe5-229">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-229">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="52fe5-230">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="52fe5-230">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-231">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="52fe5-231">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="52fe5-232">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="52fe5-232">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-233">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="52fe5-233">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="52fe5-234">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="52fe5-234">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-235">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="52fe5-235">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52fe5-236">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="52fe5-236">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-237">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52fe5-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-239">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="52fe5-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-240">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="52fe5-240">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="52fe5-241">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-241">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="52fe5-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="52fe5-243"> (0)</span><span class="sxs-lookup"><span data-stu-id="52fe5-243">(0)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-244">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="52fe5-244">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="52fe5-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="52fe5-246">(1)</span><span class="sxs-lookup"><span data-stu-id="52fe5-246">(1)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-247">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-247">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="52fe5-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="52fe5-249">(2)</span><span class="sxs-lookup"><span data-stu-id="52fe5-249">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="52fe5-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="52fe5-251">(3)</span><span class="sxs-lookup"><span data-stu-id="52fe5-251">(3)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-252">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="52fe5-252">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="52fe5-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="52fe5-254">(4)</span><span class="sxs-lookup"><span data-stu-id="52fe5-254">(4)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-255">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="52fe5-255">Device is not working properly.</span></span> <span data-ttu-id="52fe5-256">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-256">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="52fe5-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="52fe5-258">(5)</span><span class="sxs-lookup"><span data-stu-id="52fe5-258">(5)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-259">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="52fe5-259">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="52fe5-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="52fe5-261"> (6)</span><span class="sxs-lookup"><span data-stu-id="52fe5-261">(6)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-262">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="52fe5-262">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="52fe5-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="52fe5-264">(7)</span><span class="sxs-lookup"><span data-stu-id="52fe5-264">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="52fe5-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="52fe5-266">(8)</span><span class="sxs-lookup"><span data-stu-id="52fe5-266">(8)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-267">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-267">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="52fe5-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="52fe5-269">(9)</span><span class="sxs-lookup"><span data-stu-id="52fe5-269">(9)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-270">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="52fe5-270">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="52fe5-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="52fe5-272">(10)</span><span class="sxs-lookup"><span data-stu-id="52fe5-272">(10)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-273">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-273">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="52fe5-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="52fe5-275">(11)</span><span class="sxs-lookup"><span data-stu-id="52fe5-275">(11)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-276">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="52fe5-276">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="52fe5-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="52fe5-278">(12)</span><span class="sxs-lookup"><span data-stu-id="52fe5-278">(12)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-279">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-279">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="52fe5-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="52fe5-281">(13)</span><span class="sxs-lookup"><span data-stu-id="52fe5-281">(13)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-282">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-282">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="52fe5-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="52fe5-284">(14)</span><span class="sxs-lookup"><span data-stu-id="52fe5-284">(14)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-285">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="52fe5-285">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="52fe5-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="52fe5-287">(15)</span><span class="sxs-lookup"><span data-stu-id="52fe5-287">(15)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-288">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="52fe5-288">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="52fe5-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="52fe5-290">(16)</span><span class="sxs-lookup"><span data-stu-id="52fe5-290">(16)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-291">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-291">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="52fe5-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="52fe5-293">(17)</span><span class="sxs-lookup"><span data-stu-id="52fe5-293">(17)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-294">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="52fe5-294">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="52fe5-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="52fe5-296">(18)</span><span class="sxs-lookup"><span data-stu-id="52fe5-296">(18)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-297">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-297">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="52fe5-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="52fe5-299">(19)</span><span class="sxs-lookup"><span data-stu-id="52fe5-299">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="52fe5-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="52fe5-301">(20)</span><span class="sxs-lookup"><span data-stu-id="52fe5-301">(20)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-302">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-302">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="52fe5-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="52fe5-304">(21)</span><span class="sxs-lookup"><span data-stu-id="52fe5-304">(21)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-305">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="52fe5-305">System failure.</span></span> <span data-ttu-id="52fe5-306">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="52fe5-306">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="52fe5-307">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-307">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="52fe5-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="52fe5-309">(22)</span><span class="sxs-lookup"><span data-stu-id="52fe5-309">(22)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-310">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-310">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="52fe5-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="52fe5-312">(23)</span><span class="sxs-lookup"><span data-stu-id="52fe5-312">(23)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-313">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="52fe5-313">System failure.</span></span> <span data-ttu-id="52fe5-314">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="52fe5-314">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="52fe5-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="52fe5-316">(24)</span><span class="sxs-lookup"><span data-stu-id="52fe5-316">(24)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-317">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-317">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="52fe5-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="52fe5-319">(25)</span><span class="sxs-lookup"><span data-stu-id="52fe5-319">(25)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-320">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="52fe5-320">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="52fe5-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="52fe5-322">(26)</span><span class="sxs-lookup"><span data-stu-id="52fe5-322">(26)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-323">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="52fe5-323">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="52fe5-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="52fe5-325">(27)</span><span class="sxs-lookup"><span data-stu-id="52fe5-325">(27)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-326">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="52fe5-326">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="52fe5-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="52fe5-328">(28)</span><span class="sxs-lookup"><span data-stu-id="52fe5-328">(28)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-329">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-329">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="52fe5-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="52fe5-331">(29)</span><span class="sxs-lookup"><span data-stu-id="52fe5-331">(29)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-332">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-332">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="52fe5-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="52fe5-334">(30)</span><span class="sxs-lookup"><span data-stu-id="52fe5-334">(30)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-335">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52fe5-335">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="52fe5-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="52fe5-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="52fe5-337">31,5</span><span class="sxs-lookup"><span data-stu-id="52fe5-337">(31)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-338">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-338">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52fe5-339">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="52fe5-339">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-340">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="52fe5-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-342">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="52fe5-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-343">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="52fe5-343">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="52fe5-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-345">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="52fe5-345">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-348">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="52fe5-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-349">Der Name der Klasse (oder Unterklasse), die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52fe5-349">Name of the class (or subclass) used in the creation of an instance.</span></span> <span data-ttu-id="52fe5-350">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-350">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="52fe5-351">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-352">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="52fe5-352">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-353">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52fe5-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-355">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="52fe5-355">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-356">Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="52fe5-356">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="52fe5-357">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-357">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="52fe5-358">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="52fe5-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-359">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52fe5-359">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-362">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="52fe5-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-363">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-363">Textual description of the object.</span></span>

<span data-ttu-id="52fe5-364">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-365">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="52fe5-365">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-366">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-368">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="52fe5-368">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-369">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="52fe5-369">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="52fe5-370">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-371">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="52fe5-371">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-372">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="52fe5-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-374">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler gelöscht.</span><span class="sxs-lookup"><span data-stu-id="52fe5-374">If **TRUE**, the error reported in the **LastErrorCode** property is cleared.</span></span>

<span data-ttu-id="52fe5-375">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-376">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="52fe5-376">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-377">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-379">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="52fe5-379">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="52fe5-380">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-380">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-381">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="52fe5-381">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-384">Eine frei Form Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, die vom Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-384">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="52fe5-385">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-385">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-386">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="52fe5-386">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-387">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="52fe5-387">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-389">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="52fe5-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-390">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-390">Date and time when the object was installed.</span></span> <span data-ttu-id="52fe5-391">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="52fe5-391">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="52fe5-392">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="52fe5-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-394">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52fe5-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-396">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="52fe5-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="52fe5-397">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-398">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="52fe5-398">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-399">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52fe5-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-401">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="52fe5-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-402">Maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="52fe5-402">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="52fe5-403">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="52fe5-404">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="52fe5-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-405">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="52fe5-405">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-406">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52fe5-406">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-408">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="52fe5-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-409">Maximale Größe des vom Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="52fe5-409">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="52fe5-410">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="52fe5-410">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="52fe5-411">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="52fe5-412">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="52fe5-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-413">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="52fe5-413">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-414">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52fe5-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-416">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="52fe5-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-417">Minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="52fe5-417">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="52fe5-418">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="52fe5-419">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="52fe5-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-420">**Name**</span><span class="sxs-lookup"><span data-stu-id="52fe5-420">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-423">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="52fe5-423">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-424">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="52fe5-424">Label by which the object is known.</span></span> <span data-ttu-id="52fe5-425">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-425">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="52fe5-426">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-427">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="52fe5-427">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-428">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="52fe5-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-430">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="52fe5-430">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="52fe5-431">Ob eine manuelle oder automatische Bereinigung möglich ist, wird in der **Funktionen** -Array-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="52fe5-431">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="52fe5-432">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-432">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-433">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="52fe5-433">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-434">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52fe5-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-436">Wenn das Medien Zugriffsgerät mehrere einzelne Medien unterstützt, definiert diese Eigenschaft die maximale Anzahl, die unterstützt oder eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="52fe5-436">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="52fe5-437">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-437">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-438">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="52fe5-438">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-441">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="52fe5-441">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-442">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-442">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="52fe5-443">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="52fe5-444">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="52fe5-444">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-445">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="52fe5-445">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-446">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="52fe5-446">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-448">Bestimmte energiebezogene Funktionen des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-448">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="52fe5-449">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52fe5-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="52fe5-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-451">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="52fe5-451">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="52fe5-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="52fe5-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-453">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-453">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="52fe5-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="52fe5-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-455">Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-455">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="52fe5-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="52fe5-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-457">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52fe5-457">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="52fe5-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="52fe5-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-459">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="52fe5-459">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="52fe5-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="52fe5-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-461">Die [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="52fe5-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="52fe5-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-463">Die [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="52fe5-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="52fe5-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="52fe5-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="52fe5-465">Die [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="52fe5-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52fe5-466">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="52fe5-466">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-467">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="52fe5-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-469">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="52fe5-469">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="52fe5-470">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="52fe5-470">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="52fe5-471">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-471">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="52fe5-472">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="52fe5-472">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="52fe5-473">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-474">**Status**</span><span class="sxs-lookup"><span data-stu-id="52fe5-474">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-475">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-476">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-477">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="52fe5-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-478">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-478">Current status of the object.</span></span>

<span data-ttu-id="52fe5-479">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-479">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="52fe5-480">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="52fe5-480">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="52fe5-481">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="52fe5-481">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="52fe5-482">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="52fe5-482">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="52fe5-483">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="52fe5-483">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52fe5-484">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="52fe5-484">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="52fe5-485">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="52fe5-485">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="52fe5-486">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="52fe5-486">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="52fe5-487">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="52fe5-487">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="52fe5-488">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="52fe5-488">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="52fe5-489">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="52fe5-489">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="52fe5-490">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="52fe5-490">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="52fe5-491">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="52fe5-491">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="52fe5-492">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="52fe5-492">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52fe5-493">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="52fe5-493">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-494">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52fe5-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-496">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="52fe5-496">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-497">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="52fe5-497">State of the logical device.</span></span> <span data-ttu-id="52fe5-498">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-498">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="52fe5-499">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-499">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="52fe5-500">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="52fe5-500">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52fe5-501">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="52fe5-501">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="52fe5-502">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="52fe5-502">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="52fe5-503">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="52fe5-503">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="52fe5-504">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="52fe5-504">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52fe5-505">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="52fe5-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-506">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-508">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="52fe5-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-509">Die Eigenschaft " **kreationclassname** " des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="52fe5-509">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="52fe5-510">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="52fe5-511">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="52fe5-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52fe5-512">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="52fe5-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52fe5-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52fe5-514">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="52fe5-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="52fe5-515">Die **Name** -Eigenschaft des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="52fe5-515">Scoping system's **Name** property.</span></span>

<span data-ttu-id="52fe5-516">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="52fe5-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52fe5-517">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52fe5-517">Remarks</span></span>

<span data-ttu-id="52fe5-518">Die **CIM \_ diskdrive** -Klasse wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="52fe5-518">The **CIM\_DiskDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="52fe5-519">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="52fe5-519">WMI does not implement this class.</span></span> <span data-ttu-id="52fe5-520">Siehe [Win32-Klassen](win32-provider.md) für Klassen, die von **CIM \_ diskdrive** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="52fe5-520">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_DiskDrive**.</span></span>

<span data-ttu-id="52fe5-521">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="52fe5-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="52fe5-522">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="52fe5-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="52fe5-523">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52fe5-523">Requirements</span></span>



| <span data-ttu-id="52fe5-524">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52fe5-524">Requirement</span></span> | <span data-ttu-id="52fe5-525">Wert</span><span class="sxs-lookup"><span data-stu-id="52fe5-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52fe5-526">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52fe5-526">Minimum supported client</span></span><br/> | <span data-ttu-id="52fe5-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52fe5-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52fe5-528">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52fe5-528">Minimum supported server</span></span><br/> | <span data-ttu-id="52fe5-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52fe5-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52fe5-530">Namespace</span><span class="sxs-lookup"><span data-stu-id="52fe5-530">Namespace</span></span><br/>                | <span data-ttu-id="52fe5-531">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="52fe5-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="52fe5-532">MOF</span><span class="sxs-lookup"><span data-stu-id="52fe5-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52fe5-533"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="52fe5-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="52fe5-534">DLL</span><span class="sxs-lookup"><span data-stu-id="52fe5-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52fe5-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52fe5-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52fe5-536">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52fe5-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fe5-537">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="52fe5-537">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

