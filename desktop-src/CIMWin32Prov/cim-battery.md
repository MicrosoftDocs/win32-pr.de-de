---
description: Die CIM \_ -Akku Klasse stellt die Funktionen und die Verwaltung des logischen Akku Geräts dar. Diese Klasse gilt für Akkus in Laptop Systemen und anderen internen und externen Akkus.
ms.assetid: af127b7a-021b-4cd8-af1b-176aff760858
ms.tgt_platform: multiple
title: CIM_Battery-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery
- CIM_Battery.Caption
- CIM_Battery.Description
- CIM_Battery.InstallDate
- CIM_Battery.Name
- CIM_Battery.Status
- CIM_Battery.Availability
- CIM_Battery.ConfigManagerErrorCode
- CIM_Battery.ConfigManagerUserConfig
- CIM_Battery.CreationClassName
- CIM_Battery.DeviceID
- CIM_Battery.PowerManagementCapabilities
- CIM_Battery.ErrorCleared
- CIM_Battery.ErrorDescription
- CIM_Battery.LastErrorCode
- CIM_Battery.PNPDeviceID
- CIM_Battery.PowerManagementSupported
- CIM_Battery.StatusInfo
- CIM_Battery.SystemCreationClassName
- CIM_Battery.SystemName
- CIM_Battery.BatteryStatus
- CIM_Battery.Chemistry
- CIM_Battery.DesignCapacity
- CIM_Battery.DesignVoltage
- CIM_Battery.EstimatedChargeRemaining
- CIM_Battery.EstimatedRunTime
- CIM_Battery.ExpectedLife
- CIM_Battery.FullChargeCapacity
- CIM_Battery.MaxRechargeTime
- CIM_Battery.SmartBatteryVersion
- CIM_Battery.TimeOnBattery
- CIM_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3719b2700c69cfa58921bed1242aa8a6de158466
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346856"
---
# <a name="cim_battery-class"></a><span data-ttu-id="6c05e-104">CIM- \_ Akku Klasse</span><span class="sxs-lookup"><span data-stu-id="6c05e-104">CIM\_Battery class</span></span>

<span data-ttu-id="6c05e-105">Die **CIM- \_ Akku** Klasse stellt die Funktionen und die Verwaltung des logischen Akku Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="6c05e-105">The **CIM\_Battery** class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="6c05e-106">Diese Klasse gilt für Akkus in Laptop Systemen und anderen internen und externen Akkus.</span><span class="sxs-lookup"><span data-stu-id="6c05e-106">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c05e-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6c05e-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6c05e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6c05e-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6c05e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6c05e-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6c05e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c05e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c05e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C548-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Battery : CIM_LogicalDevice
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
  uint16   BatteryStatus;
  uint16   Chemistry;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  uint32   MaxRechargeTime;
  string   SmartBatteryVersion;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="6c05e-112">Member</span><span class="sxs-lookup"><span data-stu-id="6c05e-112">Members</span></span>

<span data-ttu-id="6c05e-113">Die **CIM- \_ Akku** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c05e-113">The **CIM\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="6c05e-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c05e-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6c05e-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c05e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6c05e-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c05e-116">Methods</span></span>

<span data-ttu-id="6c05e-117">Die **CIM- \_ Akku** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-117">The **CIM\_Battery** class has these methods.</span></span>



| <span data-ttu-id="6c05e-118">Methode</span><span class="sxs-lookup"><span data-stu-id="6c05e-118">Method</span></span>                                                             | <span data-ttu-id="6c05e-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c05e-119">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c05e-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="6c05e-120">**Reset**</span></span>](reset-method-in-class-cim-battery.md)                 | <span data-ttu-id="6c05e-121">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="6c05e-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="6c05e-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6c05e-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="6c05e-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6c05e-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-battery.md) | <span data-ttu-id="6c05e-124">Definiert den gewünschten Energiezustand für ein logisches Gerät und den Zeitpunkt, zu dem das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c05e-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="6c05e-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6c05e-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6c05e-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c05e-126">Properties</span></span>

<span data-ttu-id="6c05e-127">Die **CIM- \_ Akku** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c05e-127">The **CIM\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c05e-128">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="6c05e-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05e-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-132">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6c05e-132">Availability and status of the device.</span></span>

<span data-ttu-id="6c05e-133">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c05e-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05e-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c05e-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05e-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6c05e-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05e-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6c05e-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="6c05e-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6c05e-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="6c05e-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6c05e-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="6c05e-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6c05e-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="6c05e-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6c05e-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="6c05e-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6c05e-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="6c05e-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6c05e-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="6c05e-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6c05e-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="6c05e-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6c05e-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="6c05e-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6c05e-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="6c05e-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-147">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6c05e-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="6c05e-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-149">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6c05e-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6c05e-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="6c05e-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-151">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6c05e-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="6c05e-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6c05e-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="6c05e-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-154">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="6c05e-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6c05e-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="6c05e-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-156">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="6c05e-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6c05e-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="6c05e-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-158">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="6c05e-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6c05e-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="6c05e-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-160">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6c05e-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6c05e-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="6c05e-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-162">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="6c05e-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05e-163">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="6c05e-163">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-164">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05e-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-166">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-167">Die Beschreibung des Ladestatus der Batterie.</span><span class="sxs-lookup"><span data-stu-id="6c05e-167">Description of the battery's charge status.</span></span> <span data-ttu-id="6c05e-168">Der Wert 10 ist im CIM-Schema ungültig, was bedeutet, dass kein Akku in der Desktop Verwaltungsschnittstelle (Desktop Management Interface, DMI) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-168">The value 10 is not valid in the CIM schema, which represents no battery being installed in Desktop Management Interface (DMI).</span></span> <span data-ttu-id="6c05e-169">In diesem Fall sollte das Objekt nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-169">In this case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c05e-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05e-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-171">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="6c05e-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c05e-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05e-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-173">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="6c05e-173">Unknown.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="6c05e-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Vollständig abgerechnet** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05e-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-175">Vollständig abgerechnet.</span><span class="sxs-lookup"><span data-stu-id="6c05e-175">Fully charged.</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="6c05e-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (4)</span><span class="sxs-lookup"><span data-stu-id="6c05e-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-177">Niedrig.</span><span class="sxs-lookup"><span data-stu-id="6c05e-177">Low.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="6c05e-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (5)</span><span class="sxs-lookup"><span data-stu-id="6c05e-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-179">Kritisch.</span><span class="sxs-lookup"><span data-stu-id="6c05e-179">Critical.</span></span>

</dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="6c05e-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>Wird **berechnet** (6)</span><span class="sxs-lookup"><span data-stu-id="6c05e-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-181">Verlangen.</span><span class="sxs-lookup"><span data-stu-id="6c05e-181">Charging.</span></span>

</dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="6c05e-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Abrechnung und hoch** (7)</span><span class="sxs-lookup"><span data-stu-id="6c05e-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-183">Abrechnung und hoch.</span><span class="sxs-lookup"><span data-stu-id="6c05e-183">Charging and high.</span></span>

</dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="6c05e-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Abrechnung und niedrig** (8)</span><span class="sxs-lookup"><span data-stu-id="6c05e-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-185">Abrechnung und niedrig.</span><span class="sxs-lookup"><span data-stu-id="6c05e-185">Charging and low.</span></span>

</dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="6c05e-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Abrechnung und kritisch** (9)</span><span class="sxs-lookup"><span data-stu-id="6c05e-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-187">Abrechnung und kritisch.</span><span class="sxs-lookup"><span data-stu-id="6c05e-187">Charging and critical.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6c05e-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (10)</span><span class="sxs-lookup"><span data-stu-id="6c05e-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-189">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6c05e-189">Undefined.</span></span>

</dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="6c05e-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Teilweise abgerechnet** (11)</span><span class="sxs-lookup"><span data-stu-id="6c05e-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-191">Teilweise in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-191">Partially charged.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05e-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6c05e-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-195">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6c05e-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-196">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6c05e-196">A short textual description of the object.</span></span>

<span data-ttu-id="6c05e-197">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-198">**Chemi**</span><span class="sxs-lookup"><span data-stu-id="6c05e-198">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-199">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05e-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-201">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-202">Enumeration, die die Chemie des Akkus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-202">Enumeration that describes the battery's chemistry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c05e-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05e-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-204">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="6c05e-204">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c05e-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05e-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-206">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="6c05e-206">Unknown.</span></span>

</dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="6c05e-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Führende Acid** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05e-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Lead Acid** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-208">Führende Acid.</span><span class="sxs-lookup"><span data-stu-id="6c05e-208">Lead acid.</span></span>

</dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="6c05e-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel-Cadmium** (4)</span><span class="sxs-lookup"><span data-stu-id="6c05e-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel Cadmium** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-210">Nickel-Kadmium.</span><span class="sxs-lookup"><span data-stu-id="6c05e-210">Nickel cadmium.</span></span>

</dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="6c05e-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel-Metal-Hydride** (5)</span><span class="sxs-lookup"><span data-stu-id="6c05e-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel Metal Hydride** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-212">Nickel-Metal-Hydride.</span><span class="sxs-lookup"><span data-stu-id="6c05e-212">Nickel metal hydride.</span></span>

</dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="6c05e-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-Ion** (6)</span><span class="sxs-lookup"><span data-stu-id="6c05e-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-214">Lithium-Ionen.</span><span class="sxs-lookup"><span data-stu-id="6c05e-214">Lithium ion.</span></span>

</dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="6c05e-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zink Luft** (7)</span><span class="sxs-lookup"><span data-stu-id="6c05e-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-216">Zink Luft.</span><span class="sxs-lookup"><span data-stu-id="6c05e-216">Zinc air.</span></span>

</dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="6c05e-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium-Polymer** (8)</span><span class="sxs-lookup"><span data-stu-id="6c05e-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium Polymer** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-218">Lithium-Polymer.</span><span class="sxs-lookup"><span data-stu-id="6c05e-218">Lithium polymer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05e-219">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="6c05e-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-220">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-222">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6c05e-222">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-223">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6c05e-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6c05e-224">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6c05e-225">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-225">**This device is working properly.**</span></span> <span data-ttu-id="6c05e-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="6c05e-226">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6c05e-227">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-227">**This device is not configured correctly.**</span></span> <span data-ttu-id="6c05e-228">(1)</span><span class="sxs-lookup"><span data-stu-id="6c05e-228">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6c05e-229">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-229">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6c05e-230">(2)</span><span class="sxs-lookup"><span data-stu-id="6c05e-230">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6c05e-231">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-231">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6c05e-232">(3)</span><span class="sxs-lookup"><span data-stu-id="6c05e-232">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6c05e-233">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-233">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6c05e-234">(4)</span><span class="sxs-lookup"><span data-stu-id="6c05e-234">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6c05e-235">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-235">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6c05e-236">(5)</span><span class="sxs-lookup"><span data-stu-id="6c05e-236">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6c05e-237">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-237">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6c05e-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="6c05e-238">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6c05e-239">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-239">**Cannot filter.**</span></span> <span data-ttu-id="6c05e-240">(7)</span><span class="sxs-lookup"><span data-stu-id="6c05e-240">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6c05e-241">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-241">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6c05e-242">(8)</span><span class="sxs-lookup"><span data-stu-id="6c05e-242">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6c05e-243">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-243">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6c05e-244">(9)</span><span class="sxs-lookup"><span data-stu-id="6c05e-244">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6c05e-245">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-245">**This device cannot start.**</span></span> <span data-ttu-id="6c05e-246">(10)</span><span class="sxs-lookup"><span data-stu-id="6c05e-246">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6c05e-247">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-247">**This device failed.**</span></span> <span data-ttu-id="6c05e-248">(11)</span><span class="sxs-lookup"><span data-stu-id="6c05e-248">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6c05e-249">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-249">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6c05e-250">(12)</span><span class="sxs-lookup"><span data-stu-id="6c05e-250">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6c05e-251">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-251">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6c05e-252">(13)</span><span class="sxs-lookup"><span data-stu-id="6c05e-252">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6c05e-253">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-253">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6c05e-254">(14)</span><span class="sxs-lookup"><span data-stu-id="6c05e-254">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6c05e-255">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-255">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6c05e-256">(15)</span><span class="sxs-lookup"><span data-stu-id="6c05e-256">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6c05e-257">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-257">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6c05e-258">(16)</span><span class="sxs-lookup"><span data-stu-id="6c05e-258">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6c05e-259">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-259">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6c05e-260">(17)</span><span class="sxs-lookup"><span data-stu-id="6c05e-260">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6c05e-261">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-261">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6c05e-262">(18)</span><span class="sxs-lookup"><span data-stu-id="6c05e-262">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6c05e-263">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-263">**Failure using the VxD loader.**</span></span> <span data-ttu-id="6c05e-264">(19)</span><span class="sxs-lookup"><span data-stu-id="6c05e-264">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6c05e-265">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-265">**Your registry might be corrupted.**</span></span> <span data-ttu-id="6c05e-266">(20)</span><span class="sxs-lookup"><span data-stu-id="6c05e-266">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6c05e-267">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-267">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6c05e-268">(21)</span><span class="sxs-lookup"><span data-stu-id="6c05e-268">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6c05e-269">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-269">**This device is disabled.**</span></span> <span data-ttu-id="6c05e-270">(22)</span><span class="sxs-lookup"><span data-stu-id="6c05e-270">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6c05e-271">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-271">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6c05e-272">(23)</span><span class="sxs-lookup"><span data-stu-id="6c05e-272">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6c05e-273">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-273">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6c05e-274">(24)</span><span class="sxs-lookup"><span data-stu-id="6c05e-274">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6c05e-275">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-275">**Windows is still setting up this device.**</span></span> <span data-ttu-id="6c05e-276">(25)</span><span class="sxs-lookup"><span data-stu-id="6c05e-276">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6c05e-277">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="6c05e-278">(26)</span><span class="sxs-lookup"><span data-stu-id="6c05e-278">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6c05e-279">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-279">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6c05e-280">(27)</span><span class="sxs-lookup"><span data-stu-id="6c05e-280">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6c05e-281">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-281">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6c05e-282">(28)</span><span class="sxs-lookup"><span data-stu-id="6c05e-282">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6c05e-283">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-283">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6c05e-284">(29)</span><span class="sxs-lookup"><span data-stu-id="6c05e-284">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6c05e-285">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-285">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6c05e-286">(30)</span><span class="sxs-lookup"><span data-stu-id="6c05e-286">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6c05e-287">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="6c05e-287">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6c05e-288">31,5</span><span class="sxs-lookup"><span data-stu-id="6c05e-288">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05e-289">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="6c05e-289">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-290">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6c05e-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-292">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6c05e-292">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-293">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c05e-293">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6c05e-294">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-295">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="6c05e-295">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-298">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c05e-298">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-299">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c05e-299">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6c05e-300">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-300">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6c05e-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-302">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c05e-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-305">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6c05e-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-306">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6c05e-306">A textual description of the object.</span></span>

<span data-ttu-id="6c05e-307">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-308">**Design Capacity**</span><span class="sxs-lookup"><span data-stu-id="6c05e-308">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-309">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-311">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt Stunden ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-312">Die Kapazität der Akkukapazität in Milliwatt Stunden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-312">Designed capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6c05e-313">Wenn diese Eigenschaft nicht unterstützt wird, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="6c05e-313">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-314">**Design Spannung**</span><span class="sxs-lookup"><span data-stu-id="6c05e-314">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-315">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c05e-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-317">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,9 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-318">Entwickelte Spannung des Akkus in Millivolt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-318">Designed voltage of the battery in millivolts.</span></span> <span data-ttu-id="6c05e-319">Wenn dieses Attribut nicht unterstützt wird, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="6c05e-319">If this attribute is not supported, enter 0.</span></span>

<span data-ttu-id="6c05e-320">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6c05e-320">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-321">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6c05e-321">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-324">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c05e-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-325">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="6c05e-325">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6c05e-326">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-327">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="6c05e-327">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-328">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6c05e-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-330">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6c05e-330">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6c05e-331">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-332">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6c05e-332">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-335">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="6c05e-335">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6c05e-336">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-337">**Estimatedchargeremainung**</span><span class="sxs-lookup"><span data-stu-id="6c05e-337">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-338">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05e-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-340">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="6c05e-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-341">Geschätzter Prozentsatz der verbleibenden vollen Abrechnung.</span><span class="sxs-lookup"><span data-stu-id="6c05e-341">Estimated percentage of the remaining full charge.</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-342">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="6c05e-342">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-343">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-345">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Minuten ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-346">Geschätzte Zeit (in Minuten), bis die Akku Belastung unter den aktuellen Ladebedingungen erschöpft ist, wenn die Stromversorgung ausfällt, verloren geht und ausfällt, oder wenn ein Laptop von einer Stromquelle getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-346">Estimated time, in minutes, until the battery charge is depleted under the present load conditions if the utility power is off, is lost and remains off, or if a laptop is disconnected from a power source.</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-347">**Expectedlife**</span><span class="sxs-lookup"><span data-stu-id="6c05e-347">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-348">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-350">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="6c05e-350">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-351">Erwartete Lebensdauer des Akkus (in Minuten), vorausgesetzt, dass der Akku vollständig abgerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6c05e-351">Battery's expected lifetime, in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="6c05e-352">Diese Eigenschaft stellt die erwartete Gesamtlebensdauer des Akkus dar, nicht die aktuelle verbleibende Lebensdauer, die durch die **EstimatedRunTime** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6c05e-352">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-353">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="6c05e-353">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-354">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-356">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt Stunden ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-357">Die gesamte Ladekapazität des Akkus in Milliwatt Stunden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-357">The full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6c05e-358">Vergleichen Sie diesen Wert mit der **DesignCapacity** -Eigenschaft, um zu bestimmen, wann der Akku ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="6c05e-358">Compare this value to the **DesignCapacity** property to determine when the battery requires replacement.</span></span> <span data-ttu-id="6c05e-359">Die Lebensdauer eines Akkus ist in der Regel der Fall, wenn die **FullChargeCapacity** -Eigenschaft unter 80 Prozent der **DesignCapacity** -Eigenschaft liegt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-359">A battery's end-life is typically when the **FullChargeCapacity** property falls below 80 percent of the **DesignCapacity** property.</span></span> <span data-ttu-id="6c05e-360">Wenn diese Eigenschaft nicht unterstützt wird, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="6c05e-360">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-361">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6c05e-361">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-362">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6c05e-362">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-364">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-365">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c05e-365">Indicates when the object was installed.</span></span> <span data-ttu-id="6c05e-366">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-366">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6c05e-367">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-368">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6c05e-368">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-369">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-371">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6c05e-371">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6c05e-372">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-373">**Maxakku Zeit**</span><span class="sxs-lookup"><span data-stu-id="6c05e-373">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-374">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-376">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="6c05e-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-377">Maximale Zeit in Minuten, um den Akku vollständig zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6c05e-377">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="6c05e-378">Diese Eigenschaft stellt die Zeit dar, die eine vollständig abgelegte Akkukapazität wieder auflädt, nicht die derzeit verbleibende Ladezeit, die in der **Timeto fullgebühr** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-378">This property represents the time to recharge a fully depleted battery, not the current remaining charging time, which is indicated in the **TimeToFullCharge** property.</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-379">**Name**</span><span class="sxs-lookup"><span data-stu-id="6c05e-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-380">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-382">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6c05e-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-383">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-383">Label by which the object is known.</span></span> <span data-ttu-id="6c05e-384">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6c05e-385">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6c05e-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-389">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6c05e-389">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-390">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="6c05e-390">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6c05e-391">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6c05e-391">Example: "\*PNP030b"</span></span>

<span data-ttu-id="6c05e-392">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-393">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="6c05e-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-394">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6c05e-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-396">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="6c05e-396">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="6c05e-397">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c05e-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6c05e-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-399">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-399">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6c05e-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05e-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-401">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-401">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6c05e-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05e-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-403">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c05e-403">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6c05e-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05e-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-405">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c05e-405">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6c05e-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="6c05e-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-407">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="6c05e-407">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6c05e-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="6c05e-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-409">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-409">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="6c05e-410">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-410">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="6c05e-411">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6c05e-411">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6c05e-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="6c05e-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-413">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="6c05e-413">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6c05e-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="6c05e-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6c05e-415">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-415">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05e-416">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="6c05e-416">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-417">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6c05e-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-419">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="6c05e-419">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6c05e-420">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="6c05e-420">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6c05e-421">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-421">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6c05e-422">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="6c05e-422">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6c05e-423">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-423">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-424">**Smartbatteryversion**</span><span class="sxs-lookup"><span data-stu-id="6c05e-424">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-425">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-426">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-427">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-427">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-428">Die Versionsnummer der Smart Akku-Daten Spezifikation, die von diesem Akku unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6c05e-428">Smart battery data-specification version number that is supported by this battery.</span></span> <span data-ttu-id="6c05e-429">Wenn der Akku diese Funktion nicht unterstützt, sollte der Wert leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-429">If the battery does not support this function, the value should be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-430">**Status**</span><span class="sxs-lookup"><span data-stu-id="6c05e-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-431">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-433">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6c05e-433">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-434">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-434">String that indicates the current status of the object.</span></span> <span data-ttu-id="6c05e-435">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-435">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6c05e-436">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c05e-436">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6c05e-437">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="6c05e-437">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6c05e-438">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c05e-438">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6c05e-439">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="6c05e-439">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6c05e-440">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="6c05e-440">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6c05e-441">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6c05e-442">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="6c05e-442">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6c05e-443">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6c05e-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6c05e-444">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="6c05e-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6c05e-445">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="6c05e-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c05e-446">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="6c05e-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6c05e-447">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6c05e-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6c05e-448">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="6c05e-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6c05e-449">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6c05e-450">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="6c05e-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6c05e-451">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="6c05e-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6c05e-452">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="6c05e-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6c05e-453">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="6c05e-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6c05e-454">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="6c05e-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05e-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6c05e-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-456">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c05e-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-458">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-459">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6c05e-459">State of the logical device.</span></span> <span data-ttu-id="6c05e-460">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-460">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="6c05e-461">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c05e-462">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6c05e-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c05e-463">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6c05e-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6c05e-464">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6c05e-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6c05e-465">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="6c05e-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6c05e-466">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="6c05e-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c05e-467">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="6c05e-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-468">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-470">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c05e-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-471">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="6c05e-471">The scoping system's creation class name.</span></span>

<span data-ttu-id="6c05e-472">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-473">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="6c05e-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c05e-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-476">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c05e-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-477">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="6c05e-477">The scoping system's name.</span></span>

<span data-ttu-id="6c05e-478">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6c05e-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-479">**Timeonakku**</span><span class="sxs-lookup"><span data-stu-id="6c05e-479">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-480">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-482">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="6c05e-482">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-483">Verstrichene Zeit (in Sekunden) seit dem letzten Neustart des Computer Systems auf die Akkuleistung oder die Zeitspanne seit dem letzten Neustart des Systems oder der UPS, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-483">Elapsed time, in seconds, since the computer system's UPS last switched to battery power, or the amount of time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="6c05e-484">Der Wert 0 wird zurückgegeben, wenn der Akku "Online" ist.</span><span class="sxs-lookup"><span data-stu-id="6c05e-484">A value of 0 is returned if the battery is "online."</span></span>

</dd> <dt>

<span data-ttu-id="6c05e-485">**Timeto fullladung**</span><span class="sxs-lookup"><span data-stu-id="6c05e-485">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c05e-486">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c05e-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c05e-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c05e-488">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,16 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Minuten ")</span><span class="sxs-lookup"><span data-stu-id="6c05e-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6c05e-489">Verbleibende Zeit in Minuten, um den Akku vollständig zum aktuellen Abrechnungs Preis zu berechnen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c05e-489">Remaining time, in minutes, to charge the battery fully at the current charging rate and use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c05e-490">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c05e-490">Remarks</span></span>

<span data-ttu-id="6c05e-491">Die **CIM- \_ Akku** Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6c05e-491">The **CIM\_Battery** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6c05e-492">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6c05e-492">WMI does not implement this class.</span></span> <span data-ttu-id="6c05e-493">Weitere Informationen zu Klassen, die von **CIM- \_ Akku** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6c05e-493">For more information about classes derived from **CIM\_Battery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6c05e-494">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6c05e-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6c05e-495">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6c05e-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c05e-496">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c05e-496">Requirements</span></span>



| <span data-ttu-id="6c05e-497">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c05e-497">Requirement</span></span> | <span data-ttu-id="6c05e-498">Wert</span><span class="sxs-lookup"><span data-stu-id="6c05e-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c05e-499">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c05e-499">Minimum supported client</span></span><br/> | <span data-ttu-id="6c05e-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c05e-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c05e-501">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c05e-501">Minimum supported server</span></span><br/> | <span data-ttu-id="6c05e-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c05e-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c05e-503">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c05e-503">Namespace</span></span><br/>                | <span data-ttu-id="6c05e-504">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6c05e-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c05e-505">MOF</span><span class="sxs-lookup"><span data-stu-id="6c05e-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c05e-506"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6c05e-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c05e-507">DLL</span><span class="sxs-lookup"><span data-stu-id="6c05e-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c05e-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c05e-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c05e-509">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c05e-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c05e-510">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="6c05e-510">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

