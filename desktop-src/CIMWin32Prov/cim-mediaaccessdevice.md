---
description: Die CIM \_ mediaaccessdevice-Klasse stellt die Möglichkeit dar, auf ein oder mehrere Medien zuzugreifen und dann die Medien zum Speichern und Abrufen von Daten zu verwenden.
ms.assetid: 224a7b08-1566-4b0b-90d8-9991fa188d93
ms.tgt_platform: multiple
title: CIM_MediaAccessDevice-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Caption
- CIM_MediaAccessDevice.Description
- CIM_MediaAccessDevice.InstallDate
- CIM_MediaAccessDevice.Name
- CIM_MediaAccessDevice.Status
- CIM_MediaAccessDevice.Availability
- CIM_MediaAccessDevice.ConfigManagerErrorCode
- CIM_MediaAccessDevice.ConfigManagerUserConfig
- CIM_MediaAccessDevice.CreationClassName
- CIM_MediaAccessDevice.DeviceID
- CIM_MediaAccessDevice.PowerManagementCapabilities
- CIM_MediaAccessDevice.ErrorCleared
- CIM_MediaAccessDevice.ErrorDescription
- CIM_MediaAccessDevice.LastErrorCode
- CIM_MediaAccessDevice.PNPDeviceID
- CIM_MediaAccessDevice.PowerManagementSupported
- CIM_MediaAccessDevice.StatusInfo
- CIM_MediaAccessDevice.SystemCreationClassName
- CIM_MediaAccessDevice.SystemName
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de0b993b4cc1da46b19b1c296fae44e855c5816
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869588"
---
# <a name="cim_mediaaccessdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="c8d12-103">CIM_MediaAccessDevice-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="c8d12-103">CIM_MediaAccessDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c8d12-104">Die **CIM \_ mediaaccessdevice** -Klasse stellt die Möglichkeit dar, auf ein oder mehrere Medien zuzugreifen und dann die Medien zum Speichern und Abrufen von Daten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-104">The **CIM\_MediaAccessDevice** class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8d12-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c8d12-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c8d12-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c8d12-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c8d12-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c8d12-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c8d12-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d12-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8d12-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
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

## <a name="members"></a><span data-ttu-id="c8d12-110">Member</span><span class="sxs-lookup"><span data-stu-id="c8d12-110">Members</span></span>

<span data-ttu-id="c8d12-111">Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c8d12-111">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c8d12-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c8d12-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8d12-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8d12-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8d12-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="c8d12-114">Methods</span></span>

<span data-ttu-id="c8d12-115">Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-115">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="c8d12-116">Methode</span><span class="sxs-lookup"><span data-stu-id="c8d12-116">Method</span></span>                                                                       | <span data-ttu-id="c8d12-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8d12-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8d12-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="c8d12-118">**Reset**</span></span>](reset-method-in-class-cim-mediaaccessdevice.md)                 | <span data-ttu-id="c8d12-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c8d12-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="c8d12-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8d12-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c8d12-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c8d12-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-mediaaccessdevice.md) | <span data-ttu-id="c8d12-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8d12-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c8d12-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8d12-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c8d12-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8d12-124">Properties</span></span>

<span data-ttu-id="c8d12-125">Die **CIM \_ mediaaccessdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8d12-125">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8d12-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c8d12-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8d12-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="c8d12-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c8d12-130">Availability and status of the device.</span></span>

<span data-ttu-id="c8d12-131">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c8d12-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c8d12-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8d12-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c8d12-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c8d12-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="c8d12-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c8d12-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="c8d12-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c8d12-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="c8d12-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c8d12-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="c8d12-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c8d12-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="c8d12-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c8d12-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="c8d12-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c8d12-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="c8d12-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c8d12-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="c8d12-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c8d12-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="c8d12-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c8d12-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="c8d12-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c8d12-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="c8d12-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c8d12-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="c8d12-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c8d12-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c8d12-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="c8d12-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c8d12-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="c8d12-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c8d12-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="c8d12-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="c8d12-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c8d12-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="c8d12-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-154">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="c8d12-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c8d12-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="c8d12-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-156">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="c8d12-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c8d12-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="c8d12-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-158">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c8d12-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c8d12-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="c8d12-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-160">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="c8d12-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8d12-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c8d12-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-162">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c8d12-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-164">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="c8d12-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-165">Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="c8d12-165">Capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8d12-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c8d12-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-167">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c8d12-167">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c8d12-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c8d12-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-169">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="c8d12-169">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="c8d12-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="c8d12-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-171">Sequenzieller Zugriff.</span><span class="sxs-lookup"><span data-stu-id="c8d12-171">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="c8d12-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="c8d12-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-173">Random-Access.</span><span class="sxs-lookup"><span data-stu-id="c8d12-173">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="c8d12-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="c8d12-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-175">Schreiben.</span><span class="sxs-lookup"><span data-stu-id="c8d12-175">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="c8d12-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="c8d12-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-177">Verschlüsselung:</span><span class="sxs-lookup"><span data-stu-id="c8d12-177">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="c8d12-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="c8d12-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-179">Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="c8d12-179">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="c8d12-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="c8d12-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-181">Wechselmedien.</span><span class="sxs-lookup"><span data-stu-id="c8d12-181">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="c8d12-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="c8d12-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-183">Manuelle Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="c8d12-183">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="c8d12-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="c8d12-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-185">Automatische Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="c8d12-185">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="c8d12-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="c8d12-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-187">Intelligente Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c8d12-187">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="c8d12-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="c8d12-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-189">Dual-seitiges Medium.</span><span class="sxs-lookup"><span data-stu-id="c8d12-189">Dual-sided media.</span></span>

<span data-ttu-id="c8d12-190">Unterscheidet ein Gerät, das auf beide Seiten eines zweiseitigen Mediums zugreifen kann, von einem Gerät, das nur eine einzelne Seite liest und erfordert, dass die Medien eingeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="c8d12-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="c8d12-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-192">Gibt an, dass das Medium nicht explizit vom Gerät ausworfen werden muss, bevor von einem Auswahl Element darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="c8d12-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8d12-193">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="c8d12-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-194">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c8d12-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-196">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ mediaaccessdevice**.**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="c8d12-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-197">Array von Freiform-Zeichen folgen, das ausführliche Erläuterungen **für den Zugriff** auf Gerätefunktionen bereitstellt, die im Funktions Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c8d12-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="c8d12-198">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="c8d12-198">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="c8d12-199">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c8d12-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-202">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c8d12-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-203">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8d12-203">A short textual description of the object.</span></span>

<span data-ttu-id="c8d12-204">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-205">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="c8d12-205">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-208">Eine frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8d12-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="c8d12-209">Wenn es nicht möglich ist, das Komprimierungs Schema zu beschreiben (weil es unbekannt ist), verwenden Sie Folgendes: Wenn, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="c8d12-209">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="c8d12-210">Wenn, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="c8d12-210">If , use "Compressed".</span></span> <span data-ttu-id="c8d12-211">, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="c8d12-211">, use "Not Compressed".</span></span>

<dt>

<span data-ttu-id="c8d12-212">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="c8d12-212">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="c8d12-213">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8d12-213">The compression scheme is unknown or not described.</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-214">Komprimierte</span><span class="sxs-lookup"><span data-stu-id="c8d12-214">"Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="c8d12-215">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8d12-215">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-216">"Nicht komprimiert"</span><span class="sxs-lookup"><span data-stu-id="c8d12-216">"Not Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="c8d12-217">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="c8d12-217">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8d12-218">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="c8d12-218">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-219">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8d12-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-221">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c8d12-221">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-222">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c8d12-222">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c8d12-223">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-223">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c8d12-224">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-224">**This device is working properly.**</span></span> <span data-ttu-id="c8d12-225"> (0)</span><span class="sxs-lookup"><span data-stu-id="c8d12-225">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c8d12-226">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-226">**This device is not configured correctly.**</span></span> <span data-ttu-id="c8d12-227">(1)</span><span class="sxs-lookup"><span data-stu-id="c8d12-227">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c8d12-228">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-228">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c8d12-229">(2)</span><span class="sxs-lookup"><span data-stu-id="c8d12-229">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c8d12-230">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-230">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c8d12-231">(3)</span><span class="sxs-lookup"><span data-stu-id="c8d12-231">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c8d12-232">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-232">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c8d12-233">(4)</span><span class="sxs-lookup"><span data-stu-id="c8d12-233">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c8d12-234">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-234">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c8d12-235">(5)</span><span class="sxs-lookup"><span data-stu-id="c8d12-235">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c8d12-236">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-236">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c8d12-237"> (6)</span><span class="sxs-lookup"><span data-stu-id="c8d12-237">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c8d12-238">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-238">**Cannot filter.**</span></span> <span data-ttu-id="c8d12-239">(7)</span><span class="sxs-lookup"><span data-stu-id="c8d12-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c8d12-240">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-240">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c8d12-241">(8)</span><span class="sxs-lookup"><span data-stu-id="c8d12-241">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c8d12-242">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-242">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c8d12-243">(9)</span><span class="sxs-lookup"><span data-stu-id="c8d12-243">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c8d12-244">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-244">**This device cannot start.**</span></span> <span data-ttu-id="c8d12-245">(10)</span><span class="sxs-lookup"><span data-stu-id="c8d12-245">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c8d12-246">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-246">**This device failed.**</span></span> <span data-ttu-id="c8d12-247">(11)</span><span class="sxs-lookup"><span data-stu-id="c8d12-247">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c8d12-248">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-248">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c8d12-249">(12)</span><span class="sxs-lookup"><span data-stu-id="c8d12-249">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c8d12-250">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-250">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c8d12-251">(13)</span><span class="sxs-lookup"><span data-stu-id="c8d12-251">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c8d12-252">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-252">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c8d12-253">(14)</span><span class="sxs-lookup"><span data-stu-id="c8d12-253">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c8d12-254">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-254">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c8d12-255">(15)</span><span class="sxs-lookup"><span data-stu-id="c8d12-255">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c8d12-256">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-256">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c8d12-257">(16)</span><span class="sxs-lookup"><span data-stu-id="c8d12-257">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c8d12-258">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-258">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c8d12-259">(17)</span><span class="sxs-lookup"><span data-stu-id="c8d12-259">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c8d12-260">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-260">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c8d12-261">(18)</span><span class="sxs-lookup"><span data-stu-id="c8d12-261">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c8d12-262">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-262">**Failure using the VxD loader.**</span></span> <span data-ttu-id="c8d12-263">(19)</span><span class="sxs-lookup"><span data-stu-id="c8d12-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c8d12-264">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-264">**Your registry might be corrupted.**</span></span> <span data-ttu-id="c8d12-265">(20)</span><span class="sxs-lookup"><span data-stu-id="c8d12-265">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c8d12-266">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-266">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c8d12-267">(21)</span><span class="sxs-lookup"><span data-stu-id="c8d12-267">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c8d12-268">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-268">**This device is disabled.**</span></span> <span data-ttu-id="c8d12-269">(22)</span><span class="sxs-lookup"><span data-stu-id="c8d12-269">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c8d12-270">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-270">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c8d12-271">(23)</span><span class="sxs-lookup"><span data-stu-id="c8d12-271">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c8d12-272">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-272">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c8d12-273">(24)</span><span class="sxs-lookup"><span data-stu-id="c8d12-273">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c8d12-274">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-274">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c8d12-275">(25)</span><span class="sxs-lookup"><span data-stu-id="c8d12-275">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c8d12-276">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-276">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c8d12-277">(26)</span><span class="sxs-lookup"><span data-stu-id="c8d12-277">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c8d12-278">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-278">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c8d12-279">(27)</span><span class="sxs-lookup"><span data-stu-id="c8d12-279">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c8d12-280">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-280">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c8d12-281">(28)</span><span class="sxs-lookup"><span data-stu-id="c8d12-281">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c8d12-282">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-282">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c8d12-283">(29)</span><span class="sxs-lookup"><span data-stu-id="c8d12-283">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c8d12-284">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-284">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c8d12-285">(30)</span><span class="sxs-lookup"><span data-stu-id="c8d12-285">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c8d12-286">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="c8d12-286">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c8d12-287">31,5</span><span class="sxs-lookup"><span data-stu-id="c8d12-287">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8d12-288">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="c8d12-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-289">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c8d12-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-291">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c8d12-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-292">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8d12-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c8d12-293">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-294">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c8d12-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-297">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8d12-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-298">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8d12-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c8d12-299">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c8d12-300">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-301">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="c8d12-301">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-302">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c8d12-302">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-304">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c8d12-304">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-305">Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="c8d12-305">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="c8d12-306">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c8d12-306">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-307">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8d12-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-310">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c8d12-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-311">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c8d12-311">A textual description of the object.</span></span>

<span data-ttu-id="c8d12-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c8d12-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-316">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8d12-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-317">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="c8d12-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c8d12-318">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-319">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="c8d12-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-320">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c8d12-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-322">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c8d12-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c8d12-323">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c8d12-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-327">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="c8d12-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c8d12-328">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-329">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="c8d12-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-332">Eine frei Form Zeichenfolge, die die vom Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-332">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-333">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c8d12-333">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-334">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8d12-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-336">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c8d12-336">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-337">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c8d12-337">Indicates when the object was installed.</span></span> <span data-ttu-id="c8d12-338">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c8d12-338">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c8d12-339">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c8d12-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-341">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8d12-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-343">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c8d12-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c8d12-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-345">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="c8d12-345">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-346">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c8d12-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-348">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c8d12-348">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-349">Maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="c8d12-349">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="c8d12-350">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c8d12-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-351">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="c8d12-351">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-352">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c8d12-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-354">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="c8d12-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-355">Maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="c8d12-355">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="c8d12-356">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="c8d12-356">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="c8d12-357">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c8d12-357">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-358">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="c8d12-358">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-359">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c8d12-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-361">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c8d12-361">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-362">Minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="c8d12-362">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="c8d12-363">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c8d12-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-364">**Name**</span><span class="sxs-lookup"><span data-stu-id="c8d12-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-365">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-367">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c8d12-367">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-368">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c8d12-368">Label by which the object is known.</span></span> <span data-ttu-id="c8d12-369">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-369">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c8d12-370">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-371">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="c8d12-371">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-372">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c8d12-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-374">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8d12-374">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="c8d12-375">Ob eine manuelle oder automatische Bereinigung möglich ist, wird in der **Funktionen** -Array-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="c8d12-375">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-376">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="c8d12-376">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-377">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8d12-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-379">Maximale Anzahl von mehreren einzelnen Medien, die unterstützt oder eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="c8d12-379">Maximum number of multiple individual media that can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c8d12-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-383">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c8d12-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-384">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c8d12-384">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c8d12-385">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c8d12-385">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c8d12-386">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-387">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c8d12-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-388">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c8d12-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-390">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c8d12-390">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="c8d12-391">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8d12-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c8d12-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-393">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-393">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c8d12-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="c8d12-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-395">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-395">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c8d12-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="c8d12-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-397">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8d12-397">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c8d12-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c8d12-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-399">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8d12-399">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c8d12-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="c8d12-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-401">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="c8d12-401">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c8d12-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="c8d12-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-403">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-403">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="c8d12-404">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-404">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="c8d12-405">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c8d12-405">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c8d12-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="c8d12-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-407">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="c8d12-407">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c8d12-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="c8d12-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c8d12-409">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c8d12-409">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8d12-410">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="c8d12-410">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-411">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c8d12-411">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-413">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c8d12-413">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c8d12-414">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="c8d12-414">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c8d12-415">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-415">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c8d12-416">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="c8d12-416">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c8d12-417">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-418">**Status**</span><span class="sxs-lookup"><span data-stu-id="c8d12-418">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-419">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-421">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c8d12-421">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-422">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-422">String that indicates the current status of the object.</span></span> <span data-ttu-id="c8d12-423">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-423">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c8d12-424">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8d12-424">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c8d12-425">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="c8d12-425">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c8d12-426">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8d12-426">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c8d12-427">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="c8d12-427">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c8d12-428">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c8d12-428">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c8d12-429">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c8d12-430">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c8d12-430">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c8d12-431">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c8d12-431">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c8d12-432">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c8d12-432">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c8d12-433">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c8d12-433">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8d12-434">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c8d12-434">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c8d12-435">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c8d12-435">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c8d12-436">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c8d12-436">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c8d12-437">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c8d12-437">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c8d12-438">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c8d12-438">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c8d12-439">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c8d12-439">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c8d12-440">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c8d12-440">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c8d12-441">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c8d12-441">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c8d12-442">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c8d12-442">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8d12-443">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c8d12-443">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-444">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8d12-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-446">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c8d12-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-447">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c8d12-447">State of the logical device.</span></span> <span data-ttu-id="c8d12-448">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8d12-448">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="c8d12-449">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c8d12-450">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c8d12-450">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8d12-451">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c8d12-451">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c8d12-452">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c8d12-452">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c8d12-453">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="c8d12-453">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c8d12-454">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="c8d12-454">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8d12-455">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c8d12-455">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-456">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-458">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8d12-458">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-459">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c8d12-459">The scoping system's creation class name.</span></span>

<span data-ttu-id="c8d12-460">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8d12-461">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c8d12-461">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8d12-462">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c8d12-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-463">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8d12-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8d12-464">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8d12-464">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8d12-465">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c8d12-465">The scoping system's name.</span></span>

<span data-ttu-id="c8d12-466">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c8d12-466">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8d12-467">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8d12-467">Remarks</span></span>

<span data-ttu-id="c8d12-468">Die **CIM \_ mediaaccessdevice** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c8d12-468">The **CIM\_MediaAccessDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c8d12-469">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c8d12-469">WMI does not implement this class.</span></span> <span data-ttu-id="c8d12-470">Informationen zu Klassen, die von **CIM \_ mediaaccessdevice** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c8d12-470">For classes derived from **CIM\_MediaAccessDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c8d12-471">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c8d12-471">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8d12-472">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c8d12-472">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d12-473">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8d12-473">Requirements</span></span>



| <span data-ttu-id="c8d12-474">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8d12-474">Requirement</span></span> | <span data-ttu-id="c8d12-475">Wert</span><span class="sxs-lookup"><span data-stu-id="c8d12-475">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d12-476">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8d12-476">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d12-477">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8d12-477">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8d12-478">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8d12-478">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d12-479">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8d12-479">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8d12-480">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8d12-480">Namespace</span></span><br/>                | <span data-ttu-id="c8d12-481">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c8d12-481">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8d12-482">MOF</span><span class="sxs-lookup"><span data-stu-id="c8d12-482">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8d12-483"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c8d12-483"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8d12-484">DLL</span><span class="sxs-lookup"><span data-stu-id="c8d12-484">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8d12-485"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8d12-485"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8d12-486">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8d12-486">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d12-487">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c8d12-487">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

