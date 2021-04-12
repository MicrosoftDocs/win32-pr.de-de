---
description: Die CIM \_ -Klasse "magnetyopticaldrive" stellt die Funktionen und die Verwaltung eines "Magneto-Optical"-Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.
ms.assetid: 82a4604d-3bef-4378-812b-550849e30b8c
ms.tgt_platform: multiple
title: CIM_MagnetoOpticalDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MagnetoOpticalDrive
- CIM_MagnetoOpticalDrive.Availability
- CIM_MagnetoOpticalDrive.Capabilities
- CIM_MagnetoOpticalDrive.CapabilityDescriptions
- CIM_MagnetoOpticalDrive.Caption
- CIM_MagnetoOpticalDrive.CompressionMethod
- CIM_MagnetoOpticalDrive.ConfigManagerErrorCode
- CIM_MagnetoOpticalDrive.ConfigManagerUserConfig
- CIM_MagnetoOpticalDrive.CreationClassName
- CIM_MagnetoOpticalDrive.DefaultBlockSize
- CIM_MagnetoOpticalDrive.Description
- CIM_MagnetoOpticalDrive.DeviceID
- CIM_MagnetoOpticalDrive.ErrorCleared
- CIM_MagnetoOpticalDrive.ErrorDescription
- CIM_MagnetoOpticalDrive.ErrorMethodology
- CIM_MagnetoOpticalDrive.InstallDate
- CIM_MagnetoOpticalDrive.LastErrorCode
- CIM_MagnetoOpticalDrive.MaxBlockSize
- CIM_MagnetoOpticalDrive.MaxMediaSize
- CIM_MagnetoOpticalDrive.MinBlockSize
- CIM_MagnetoOpticalDrive.Name
- CIM_MagnetoOpticalDrive.NeedsCleaning
- CIM_MagnetoOpticalDrive.NumberOfMediaSupported
- CIM_MagnetoOpticalDrive.PNPDeviceID
- CIM_MagnetoOpticalDrive.PowerManagementCapabilities
- CIM_MagnetoOpticalDrive.PowerManagementSupported
- CIM_MagnetoOpticalDrive.Status
- CIM_MagnetoOpticalDrive.StatusInfo
- CIM_MagnetoOpticalDrive.SystemCreationClassName
- CIM_MagnetoOpticalDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: abc5acdf25a2920fa53c6315109264180b6e7c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483366"
---
# <a name="cim_magnetoopticaldrive-class"></a><span data-ttu-id="122cf-103">CIM- \_ Klasse "magnedeopticaldrive"</span><span class="sxs-lookup"><span data-stu-id="122cf-103">CIM\_MagnetoOpticalDrive class</span></span>

<span data-ttu-id="122cf-104">Die CIM-Klasse " **\_ magnetyopticaldrive** " stellt die Funktionen und die Verwaltung eines "Magneto-Optical"-Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="122cf-104">The **CIM\_MagnetoOpticalDrive** class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="122cf-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="122cf-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="122cf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="122cf-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="122cf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="122cf-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="122cf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="122cf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="122cf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{F62037D8-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_MagnetoOpticalDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="122cf-110">Member</span><span class="sxs-lookup"><span data-stu-id="122cf-110">Members</span></span>

<span data-ttu-id="122cf-111">Die CIM-Klasse " **\_ magnetoopticaldrive** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="122cf-111">The **CIM\_MagnetoOpticalDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="122cf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="122cf-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="122cf-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="122cf-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="122cf-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="122cf-114">Methods</span></span>

<span data-ttu-id="122cf-115">Die CIM-Klasse " **\_ magneyopticaldrive** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="122cf-115">The **CIM\_MagnetoOpticalDrive** class has these methods.</span></span>



| <span data-ttu-id="122cf-116">Methode</span><span class="sxs-lookup"><span data-stu-id="122cf-116">Method</span></span>                                                                         | <span data-ttu-id="122cf-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="122cf-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="122cf-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="122cf-118">**Reset**</span></span>](reset-method-in-class-cim-magnetoopticaldrive.md)                 | <span data-ttu-id="122cf-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="122cf-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="122cf-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="122cf-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="122cf-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="122cf-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-magnetoopticaldrive.md) | <span data-ttu-id="122cf-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="122cf-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="122cf-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="122cf-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="122cf-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="122cf-124">Properties</span></span>

<span data-ttu-id="122cf-125">Die CIM-Klasse " **\_ magnedeopticaldrive** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="122cf-125">The **CIM\_MagnetoOpticalDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="122cf-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="122cf-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="122cf-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="122cf-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="122cf-130">Availability and status of the device.</span></span>

<span data-ttu-id="122cf-131">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="122cf-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="122cf-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="122cf-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="122cf-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="122cf-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="122cf-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="122cf-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="122cf-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="122cf-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="122cf-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="122cf-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="122cf-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="122cf-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="122cf-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="122cf-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="122cf-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="122cf-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="122cf-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="122cf-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="122cf-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="122cf-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="122cf-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="122cf-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="122cf-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="122cf-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="122cf-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="122cf-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="122cf-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="122cf-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="122cf-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="122cf-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="122cf-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="122cf-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="122cf-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="122cf-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="122cf-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="122cf-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="122cf-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="122cf-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-154">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="122cf-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="122cf-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="122cf-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-156">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="122cf-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="122cf-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="122cf-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-158">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="122cf-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="122cf-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="122cf-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-160">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="122cf-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="122cf-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="122cf-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-162">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="122cf-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="122cf-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-164">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="122cf-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-165">Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="122cf-165">Capabilities of the media access device.</span></span>

<span data-ttu-id="122cf-166">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-166">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="122cf-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="122cf-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-168">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="122cf-168">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="122cf-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="122cf-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-170">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="122cf-170">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="122cf-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="122cf-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-172">Sequenzieller Zugriff.</span><span class="sxs-lookup"><span data-stu-id="122cf-172">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="122cf-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="122cf-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-174">Random-Access.</span><span class="sxs-lookup"><span data-stu-id="122cf-174">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="122cf-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="122cf-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-176">Schreiben.</span><span class="sxs-lookup"><span data-stu-id="122cf-176">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="122cf-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="122cf-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-178">Verschlüsselung:</span><span class="sxs-lookup"><span data-stu-id="122cf-178">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="122cf-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="122cf-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-180">Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="122cf-180">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="122cf-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="122cf-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-182">Wechselmedien.</span><span class="sxs-lookup"><span data-stu-id="122cf-182">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="122cf-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="122cf-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-184">Manuelle Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="122cf-184">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="122cf-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="122cf-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-186">Automatische Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="122cf-186">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="122cf-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="122cf-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-188">Intelligente Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="122cf-188">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="122cf-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="122cf-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-190">Unterscheidet ein Gerät, das auf beide Seiten eines zweiseitigen Mediums zugreifen kann, von einem Gerät, das nur eine einzelne Seite liest und erfordert, dass die Medien eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="122cf-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="122cf-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-192">Gibt an, dass das Medium nicht explizit vom Gerät ausworfen werden muss, bevor von einem Auswahl Element darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="122cf-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="122cf-193">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="122cf-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-194">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="122cf-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="122cf-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-196">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="122cf-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-197">Array von Freiform-Zeichen folgen, das ausführliche Erläuterungen **für den Zugriff** auf Gerätefunktionen bereitstellt, die im Funktions Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="122cf-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="122cf-198">Jeder Array Eintrag bezieht sich auf den Eintrag im Funktions **Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="122cf-198">Each array entry is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="122cf-199">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-199">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-200">**Caption**</span><span class="sxs-lookup"><span data-stu-id="122cf-200">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-203">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="122cf-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-204">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="122cf-204">Short textual description of the object.</span></span>

<span data-ttu-id="122cf-205">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-206">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="122cf-206">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-209">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="122cf-209">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="122cf-210">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="122cf-210">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="122cf-211">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="122cf-211">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="122cf-212">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="122cf-212">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="122cf-213">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-213">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="122cf-214">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="122cf-214">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="122cf-215">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="122cf-215">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="122cf-216">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="122cf-216">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="122cf-217">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="122cf-217">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="122cf-218">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="122cf-218">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="122cf-219">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="122cf-219">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="122cf-220">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="122cf-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-221">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="122cf-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-223">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="122cf-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-224">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="122cf-224">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="122cf-225">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="122cf-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="122cf-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="122cf-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="122cf-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-228">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="122cf-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="122cf-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="122cf-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="122cf-230">(1)</span><span class="sxs-lookup"><span data-stu-id="122cf-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-231">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="122cf-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="122cf-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="122cf-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="122cf-233">(2)</span><span class="sxs-lookup"><span data-stu-id="122cf-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="122cf-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="122cf-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="122cf-235">(3)</span><span class="sxs-lookup"><span data-stu-id="122cf-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-236">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="122cf-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="122cf-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="122cf-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="122cf-238">(4)</span><span class="sxs-lookup"><span data-stu-id="122cf-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-239">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="122cf-239">Device is not working properly.</span></span> <span data-ttu-id="122cf-240">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="122cf-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="122cf-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="122cf-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="122cf-242">(5)</span><span class="sxs-lookup"><span data-stu-id="122cf-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-243">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="122cf-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="122cf-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="122cf-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="122cf-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="122cf-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-246">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="122cf-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="122cf-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="122cf-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="122cf-248">(7)</span><span class="sxs-lookup"><span data-stu-id="122cf-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="122cf-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="122cf-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="122cf-250">(8)</span><span class="sxs-lookup"><span data-stu-id="122cf-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-251">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="122cf-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="122cf-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="122cf-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="122cf-253">(9)</span><span class="sxs-lookup"><span data-stu-id="122cf-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-254">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="122cf-254">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="122cf-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="122cf-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="122cf-256">(10)</span><span class="sxs-lookup"><span data-stu-id="122cf-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-257">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="122cf-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="122cf-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="122cf-259">(11)</span><span class="sxs-lookup"><span data-stu-id="122cf-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-260">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="122cf-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="122cf-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="122cf-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="122cf-262">(12)</span><span class="sxs-lookup"><span data-stu-id="122cf-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-263">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="122cf-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="122cf-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="122cf-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="122cf-265">(13)</span><span class="sxs-lookup"><span data-stu-id="122cf-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-266">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="122cf-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="122cf-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="122cf-268">(14)</span><span class="sxs-lookup"><span data-stu-id="122cf-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-269">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="122cf-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="122cf-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="122cf-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="122cf-271">(15)</span><span class="sxs-lookup"><span data-stu-id="122cf-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-272">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="122cf-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="122cf-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="122cf-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="122cf-274">(16)</span><span class="sxs-lookup"><span data-stu-id="122cf-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-275">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="122cf-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="122cf-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="122cf-277">(17)</span><span class="sxs-lookup"><span data-stu-id="122cf-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-278">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="122cf-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="122cf-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="122cf-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="122cf-280">(18)</span><span class="sxs-lookup"><span data-stu-id="122cf-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-281">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="122cf-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="122cf-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="122cf-283">(19)</span><span class="sxs-lookup"><span data-stu-id="122cf-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="122cf-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="122cf-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="122cf-285">(20)</span><span class="sxs-lookup"><span data-stu-id="122cf-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-286">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="122cf-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="122cf-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="122cf-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="122cf-288">(21)</span><span class="sxs-lookup"><span data-stu-id="122cf-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-289">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="122cf-289">System failure.</span></span> <span data-ttu-id="122cf-290">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="122cf-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="122cf-291">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="122cf-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="122cf-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="122cf-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="122cf-293">(22)</span><span class="sxs-lookup"><span data-stu-id="122cf-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-294">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="122cf-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="122cf-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="122cf-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="122cf-296">(23)</span><span class="sxs-lookup"><span data-stu-id="122cf-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-297">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="122cf-297">System failure.</span></span> <span data-ttu-id="122cf-298">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="122cf-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="122cf-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="122cf-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="122cf-300">(24)</span><span class="sxs-lookup"><span data-stu-id="122cf-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-301">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="122cf-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="122cf-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="122cf-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="122cf-303">(25)</span><span class="sxs-lookup"><span data-stu-id="122cf-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-304">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="122cf-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="122cf-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="122cf-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="122cf-306">(26)</span><span class="sxs-lookup"><span data-stu-id="122cf-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-307">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="122cf-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="122cf-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="122cf-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="122cf-309">(27)</span><span class="sxs-lookup"><span data-stu-id="122cf-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-310">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="122cf-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="122cf-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="122cf-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="122cf-312">(28)</span><span class="sxs-lookup"><span data-stu-id="122cf-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-313">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="122cf-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="122cf-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="122cf-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="122cf-315">(29)</span><span class="sxs-lookup"><span data-stu-id="122cf-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-316">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="122cf-316">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="122cf-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="122cf-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="122cf-318">(30)</span><span class="sxs-lookup"><span data-stu-id="122cf-318">(30)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-319">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="122cf-319">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="122cf-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="122cf-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="122cf-321">31,5</span><span class="sxs-lookup"><span data-stu-id="122cf-321">(31)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-322">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-322">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="122cf-323">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="122cf-323">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-324">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="122cf-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-326">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="122cf-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-327">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="122cf-327">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="122cf-328">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-329">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="122cf-329">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-332">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="122cf-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="122cf-333">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="122cf-333">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="122cf-334">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-334">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="122cf-335">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-336">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="122cf-336">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-337">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="122cf-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-339">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="122cf-339">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-340">Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="122cf-340">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="122cf-341">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-341">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="122cf-342">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="122cf-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-343">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="122cf-343">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-346">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="122cf-346">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-347">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="122cf-347">Textual description of the object.</span></span>

<span data-ttu-id="122cf-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="122cf-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-352">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="122cf-352">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="122cf-353">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="122cf-353">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="122cf-354">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-355">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="122cf-355">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-356">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="122cf-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-358">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="122cf-358">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="122cf-359">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-360">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="122cf-360">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-363">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="122cf-363">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="122cf-364">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-365">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="122cf-365">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-366">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-368">Eine frei Form Zeichenfolge, die die vom Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="122cf-368">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="122cf-369">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-369">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="122cf-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-371">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="122cf-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-373">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="122cf-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-374">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="122cf-374">Date and time the object was installed.</span></span> <span data-ttu-id="122cf-375">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="122cf-375">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="122cf-376">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="122cf-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-378">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="122cf-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-380">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="122cf-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="122cf-381">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-382">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="122cf-382">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-383">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="122cf-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-385">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="122cf-385">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-386">Maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="122cf-386">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="122cf-387">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-387">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="122cf-388">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="122cf-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-389">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="122cf-389">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-390">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="122cf-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-392">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="122cf-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-393">Maximale Größe des vom Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="122cf-393">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="122cf-394">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="122cf-394">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="122cf-395">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-395">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="122cf-396">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="122cf-396">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-397">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="122cf-397">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-398">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="122cf-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-400">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="122cf-400">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-401">Minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="122cf-401">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="122cf-402">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-402">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="122cf-403">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="122cf-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-404">**Name**</span><span class="sxs-lookup"><span data-stu-id="122cf-404">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-405">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-407">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="122cf-407">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-408">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="122cf-408">Label by which the object is known.</span></span> <span data-ttu-id="122cf-409">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-409">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="122cf-410">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-410">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-411">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="122cf-411">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-412">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="122cf-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-414">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="122cf-414">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="122cf-415">Ob eine manuelle oder automatische Bereinigung möglich ist, wird in der **Funktionen** -Array-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="122cf-415">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="122cf-416">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-416">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-417">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="122cf-417">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-418">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="122cf-418">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-420">Wenn das Medien Zugriffsgerät mehrere einzelne Medien unterstützt, definiert diese Eigenschaft die maximale Anzahl, die unterstützt oder eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="122cf-420">If the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="122cf-421">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-421">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-422">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="122cf-422">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-423">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-425">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="122cf-425">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-426">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="122cf-426">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="122cf-427">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="122cf-428">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="122cf-428">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="122cf-429">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="122cf-429">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-430">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="122cf-430">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="122cf-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-432">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="122cf-432">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="122cf-433">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-433">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="122cf-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="122cf-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="122cf-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="122cf-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-436">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="122cf-436">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="122cf-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="122cf-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="122cf-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="122cf-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-439">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="122cf-439">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="122cf-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="122cf-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-441">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="122cf-441">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="122cf-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="122cf-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-443">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="122cf-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="122cf-444">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-444">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="122cf-445">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="122cf-445">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="122cf-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="122cf-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-447">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="122cf-447">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="122cf-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="122cf-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="122cf-449">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="122cf-449">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="122cf-450">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="122cf-450">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-451">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="122cf-451">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="122cf-453">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="122cf-453">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="122cf-454">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="122cf-454">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="122cf-455">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-455">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="122cf-456">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="122cf-456">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="122cf-457">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-458">**Status**</span><span class="sxs-lookup"><span data-stu-id="122cf-458">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-459">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-461">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="122cf-461">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-462">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="122cf-462">Current status of the object.</span></span>

<span data-ttu-id="122cf-463">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-463">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="122cf-464">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="122cf-464">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="122cf-465">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="122cf-465">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="122cf-466">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="122cf-466">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="122cf-467">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="122cf-467">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="122cf-468">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="122cf-468">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="122cf-469">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="122cf-469">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="122cf-470">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="122cf-470">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="122cf-471">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="122cf-471">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="122cf-472">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="122cf-472">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="122cf-473">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="122cf-473">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="122cf-474">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="122cf-474">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="122cf-475">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="122cf-475">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="122cf-476">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="122cf-476">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="122cf-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="122cf-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-478">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="122cf-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-479">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-480">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="122cf-480">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="122cf-481">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="122cf-481">State of the logical device.</span></span> <span data-ttu-id="122cf-482">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="122cf-482">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="122cf-483">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="122cf-484">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="122cf-484">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="122cf-485">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="122cf-485">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="122cf-486">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="122cf-486">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="122cf-487">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="122cf-487">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="122cf-488">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="122cf-488">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="122cf-489">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="122cf-489">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-490">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-491">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-492">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="122cf-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="122cf-493">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="122cf-493">Scoping system's creation class name.</span></span>

<span data-ttu-id="122cf-494">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="122cf-495">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="122cf-495">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="122cf-496">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="122cf-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="122cf-497">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="122cf-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="122cf-498">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="122cf-498">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="122cf-499">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="122cf-499">Scoping system's name.</span></span>

<span data-ttu-id="122cf-500">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="122cf-500">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="122cf-501">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="122cf-501">Remarks</span></span>

<span data-ttu-id="122cf-502">Die CIM-Klasse " **\_ magneyopticaldrive** " ist von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="122cf-502">The **CIM\_MagnetoOpticalDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="122cf-503">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="122cf-503">WMI does not implement this class.</span></span>

<span data-ttu-id="122cf-504">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="122cf-504">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="122cf-505">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="122cf-505">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="122cf-506">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="122cf-506">Requirements</span></span>



| <span data-ttu-id="122cf-507">Anforderung</span><span class="sxs-lookup"><span data-stu-id="122cf-507">Requirement</span></span> | <span data-ttu-id="122cf-508">Wert</span><span class="sxs-lookup"><span data-stu-id="122cf-508">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="122cf-509">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="122cf-509">Minimum supported client</span></span><br/> | <span data-ttu-id="122cf-510">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="122cf-510">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="122cf-511">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="122cf-511">Minimum supported server</span></span><br/> | <span data-ttu-id="122cf-512">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="122cf-512">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="122cf-513">Namespace</span><span class="sxs-lookup"><span data-stu-id="122cf-513">Namespace</span></span><br/>                | <span data-ttu-id="122cf-514">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="122cf-514">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="122cf-515">MOF</span><span class="sxs-lookup"><span data-stu-id="122cf-515">MOF</span></span><br/>                      | <dl> <span data-ttu-id="122cf-516"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="122cf-516"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="122cf-517">DLL</span><span class="sxs-lookup"><span data-stu-id="122cf-517">DLL</span></span><br/>                      | <dl> <span data-ttu-id="122cf-518"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="122cf-518"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="122cf-519">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="122cf-519">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122cf-520">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="122cf-520">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

