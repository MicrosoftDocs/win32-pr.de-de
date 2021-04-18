---
description: Die CIM- \_ Klasse uninterruptiblepowersupply stellt die Funktionen und die Verwaltung einer unterbrechungsfreien Stromversorgung (UPS) dar.
ms.assetid: 27ddc955-906b-40b9-981b-96872356477c
ms.tgt_platform: multiple
title: CIM_UninterruptiblePowerSupply-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply
- CIM_UninterruptiblePowerSupply.ActiveInputVoltage
- CIM_UninterruptiblePowerSupply.Availability
- CIM_UninterruptiblePowerSupply.Caption
- CIM_UninterruptiblePowerSupply.ConfigManagerErrorCode
- CIM_UninterruptiblePowerSupply.ConfigManagerUserConfig
- CIM_UninterruptiblePowerSupply.CreationClassName
- CIM_UninterruptiblePowerSupply.Description
- CIM_UninterruptiblePowerSupply.DeviceID
- CIM_UninterruptiblePowerSupply.ErrorCleared
- CIM_UninterruptiblePowerSupply.ErrorDescription
- CIM_UninterruptiblePowerSupply.EstimatedChargeRemaining
- CIM_UninterruptiblePowerSupply.EstimatedRunTime
- CIM_UninterruptiblePowerSupply.InstallDate
- CIM_UninterruptiblePowerSupply.IsSwitchingSupply
- CIM_UninterruptiblePowerSupply.LastErrorCode
- CIM_UninterruptiblePowerSupply.Name
- CIM_UninterruptiblePowerSupply.PNPDeviceID
- CIM_UninterruptiblePowerSupply.PowerManagementCapabilities
- CIM_UninterruptiblePowerSupply.PowerManagementSupported
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range1InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range1InputVoltageLow
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range2InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range2InputVoltageLow
- CIM_UninterruptiblePowerSupply.RemainingCapacityStatus
- CIM_UninterruptiblePowerSupply.Status
- CIM_UninterruptiblePowerSupply.StatusInfo
- CIM_UninterruptiblePowerSupply.SystemCreationClassName
- CIM_UninterruptiblePowerSupply.SystemName
- CIM_UninterruptiblePowerSupply.TimeOnBackup
- CIM_UninterruptiblePowerSupply.TotalOutputPower
- CIM_UninterruptiblePowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 214517fd6518cf2ca406523c61f522ae9c1adc46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344811"
---
# <a name="cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="63ded-103">CIM- \_ Klasse uninterruptiblepowersupply</span><span class="sxs-lookup"><span data-stu-id="63ded-103">CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="63ded-104">Die **CIM-Klasse \_ uninterruptiblepowersupply** stellt die Funktionen und die Verwaltung einer unterbrechungsfreien Stromversorgung (UPS) dar.</span><span class="sxs-lookup"><span data-stu-id="63ded-104">The **CIM\_UninterruptiblePowerSupply** class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span> <span data-ttu-id="63ded-105">Die Eigenschaften des UPS-Geräts geben an, wenn die eingehende Stromversorgung gekürzt oder erhöht wird, sowie die aggregierten Informationen der Akkus, Generatoren usw., die das Gerät bilden.</span><span class="sxs-lookup"><span data-stu-id="63ded-105">The properties of the UPS device indicate when incoming power is trimmed or boosted, and the aggregated information of the batteries, generators, and so on, that make up the device.</span></span> <span data-ttu-id="63ded-106">Die einzelnen Komponenten (z. b. mehrere Akkus) können auch unabhängig modelliert und mit den UPS verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-106">The individual components (for example, multiple batteries) can also be independently modeled and associated with the UPS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63ded-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="63ded-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="63ded-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="63ded-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="63ded-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="63ded-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="63ded-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ded-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="63ded-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UninterruptiblePowerSupply : CIM_PowerSupply
{
  uint16   ActiveInputVoltage;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  datetime InstallDate;
  boolean  IsSwitchingSupply;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Range1InputFrequencyHigh;
  uint32   Range1InputFrequencyLow;
  uint32   Range1InputVoltageHigh;
  uint32   Range1InputVoltageLow;
  uint32   Range2InputFrequencyHigh;
  uint32   Range2InputFrequencyLow;
  uint32   Range2InputVoltageHigh;
  uint32   Range2InputVoltageLow;
  uint16   RemainingCapacityStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBackup;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="63ded-112">Member</span><span class="sxs-lookup"><span data-stu-id="63ded-112">Members</span></span>

<span data-ttu-id="63ded-113">Die **CIM-Klasse \_ uninterruptiblepowersupply** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="63ded-113">The **CIM\_UninterruptiblePowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="63ded-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="63ded-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="63ded-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="63ded-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63ded-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="63ded-116">Methods</span></span>

<span data-ttu-id="63ded-117">Die **CIM-Klasse \_ uninterruptiblepowersupply** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="63ded-117">The **CIM\_UninterruptiblePowerSupply** class has these methods.</span></span>



| <span data-ttu-id="63ded-118">Methode</span><span class="sxs-lookup"><span data-stu-id="63ded-118">Method</span></span>                                                                                | <span data-ttu-id="63ded-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63ded-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63ded-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="63ded-120">**Reset**</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)                 | <span data-ttu-id="63ded-121">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="63ded-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="63ded-122">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="63ded-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="63ded-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-uninterruptiblepowersupply.md) | <span data-ttu-id="63ded-124">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63ded-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="63ded-125">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="63ded-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="63ded-126">Properties</span></span>

<span data-ttu-id="63ded-127">Die **CIM-Klasse \_ uninterruptiblepowersupply** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="63ded-127">The **CIM\_UninterruptiblePowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63ded-128">**Activinput Spannung**</span><span class="sxs-lookup"><span data-stu-id="63ded-128">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63ded-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="63ded-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-132">Der Eingabe Spannungsbereich wird derzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="63ded-132">Input voltage range is currently in use.</span></span> <span data-ttu-id="63ded-133">Wenn die Bereitstellung derzeit keine Zeichenkraft ist, kann der Wert 6 ("keine") angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-133">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="63ded-134">Diese Informationen sind erforderlich, wenn es sich um eine Unterklasse des CIM- [**\_ Netzteils**](cim-powersupply.md)handelt.</span><span class="sxs-lookup"><span data-stu-id="63ded-134">This information is necessary in the case of a UPS, a subclass of [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="63ded-135">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-135">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63ded-136">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="63ded-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63ded-137">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="63ded-137">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="63ded-138">**Bereich 1** (3)</span><span class="sxs-lookup"><span data-stu-id="63ded-138">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="63ded-139">**Bereich 2** (4)</span><span class="sxs-lookup"><span data-stu-id="63ded-139">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="63ded-140">**Beides** (5)</span><span class="sxs-lookup"><span data-stu-id="63ded-140">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="63ded-141">**Keines der beiden** (6)</span><span class="sxs-lookup"><span data-stu-id="63ded-141">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63ded-142">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="63ded-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63ded-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-145">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="63ded-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-146">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="63ded-146">Availability and status of the device.</span></span>

<span data-ttu-id="63ded-147">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63ded-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="63ded-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63ded-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="63ded-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="63ded-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="63ded-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-151">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="63ded-151">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="63ded-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="63ded-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="63ded-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="63ded-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="63ded-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="63ded-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="63ded-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="63ded-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="63ded-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="63ded-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="63ded-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="63ded-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="63ded-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="63ded-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="63ded-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="63ded-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="63ded-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="63ded-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="63ded-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="63ded-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-162">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="63ded-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="63ded-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="63ded-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-164">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63ded-164">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="63ded-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="63ded-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-166">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="63ded-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="63ded-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="63ded-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="63ded-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-169">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="63ded-169">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="63ded-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="63ded-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-171">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="63ded-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="63ded-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="63ded-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-173">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="63ded-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="63ded-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="63ded-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-175">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="63ded-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="63ded-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="63ded-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-177">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="63ded-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63ded-178">**Caption**</span><span class="sxs-lookup"><span data-stu-id="63ded-178">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-181">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="63ded-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-182">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="63ded-182">Short textual description of the object.</span></span>

<span data-ttu-id="63ded-183">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-184">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="63ded-184">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-185">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-185">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-187">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="63ded-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-188">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="63ded-188">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="63ded-189">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-189">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="63ded-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="63ded-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="63ded-191"> (0)</span><span class="sxs-lookup"><span data-stu-id="63ded-191">(0)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-192">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="63ded-192">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="63ded-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="63ded-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="63ded-194">(1)</span><span class="sxs-lookup"><span data-stu-id="63ded-194">(1)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-195">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="63ded-195">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="63ded-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="63ded-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="63ded-197">(2)</span><span class="sxs-lookup"><span data-stu-id="63ded-197">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="63ded-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="63ded-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="63ded-199">(3)</span><span class="sxs-lookup"><span data-stu-id="63ded-199">(3)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-200">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="63ded-200">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="63ded-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="63ded-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="63ded-202">(4)</span><span class="sxs-lookup"><span data-stu-id="63ded-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-203">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="63ded-203">Device is not working properly.</span></span> <span data-ttu-id="63ded-204">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="63ded-204">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="63ded-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="63ded-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="63ded-206">(5)</span><span class="sxs-lookup"><span data-stu-id="63ded-206">(5)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-207">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="63ded-207">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="63ded-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="63ded-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="63ded-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="63ded-209">(6)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-210">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="63ded-210">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="63ded-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="63ded-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="63ded-212">(7)</span><span class="sxs-lookup"><span data-stu-id="63ded-212">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="63ded-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="63ded-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="63ded-214">(8)</span><span class="sxs-lookup"><span data-stu-id="63ded-214">(8)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-215">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="63ded-215">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="63ded-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="63ded-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="63ded-217">(9)</span><span class="sxs-lookup"><span data-stu-id="63ded-217">(9)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-218">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="63ded-218">Device is not working properly.</span></span> <span data-ttu-id="63ded-219">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="63ded-219">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="63ded-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="63ded-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="63ded-221">(10)</span><span class="sxs-lookup"><span data-stu-id="63ded-221">(10)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-222">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-222">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="63ded-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="63ded-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="63ded-224">(11)</span><span class="sxs-lookup"><span data-stu-id="63ded-224">(11)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-225">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="63ded-225">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="63ded-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="63ded-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="63ded-227">(12)</span><span class="sxs-lookup"><span data-stu-id="63ded-227">(12)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-228">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="63ded-228">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="63ded-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="63ded-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="63ded-230">(13)</span><span class="sxs-lookup"><span data-stu-id="63ded-230">(13)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-231">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-231">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="63ded-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="63ded-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="63ded-233">(14)</span><span class="sxs-lookup"><span data-stu-id="63ded-233">(14)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-234">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="63ded-234">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="63ded-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="63ded-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="63ded-236">(15)</span><span class="sxs-lookup"><span data-stu-id="63ded-236">(15)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-237">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="63ded-237">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="63ded-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="63ded-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="63ded-239">(16)</span><span class="sxs-lookup"><span data-stu-id="63ded-239">(16)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-240">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-240">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="63ded-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="63ded-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="63ded-242">(17)</span><span class="sxs-lookup"><span data-stu-id="63ded-242">(17)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-243">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="63ded-243">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="63ded-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="63ded-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="63ded-245">(18)</span><span class="sxs-lookup"><span data-stu-id="63ded-245">(18)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-246">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-246">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="63ded-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="63ded-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="63ded-248">(19)</span><span class="sxs-lookup"><span data-stu-id="63ded-248">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="63ded-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="63ded-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="63ded-250">(20)</span><span class="sxs-lookup"><span data-stu-id="63ded-250">(20)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-251">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="63ded-251">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="63ded-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="63ded-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="63ded-253">(21)</span><span class="sxs-lookup"><span data-stu-id="63ded-253">(21)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-254">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="63ded-254">System failure.</span></span> <span data-ttu-id="63ded-255">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="63ded-255">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="63ded-256">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="63ded-256">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="63ded-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="63ded-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="63ded-258">(22)</span><span class="sxs-lookup"><span data-stu-id="63ded-258">(22)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-259">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="63ded-259">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="63ded-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="63ded-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="63ded-261">(23)</span><span class="sxs-lookup"><span data-stu-id="63ded-261">(23)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-262">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="63ded-262">System failure.</span></span> <span data-ttu-id="63ded-263">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="63ded-263">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="63ded-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="63ded-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="63ded-265">(24)</span><span class="sxs-lookup"><span data-stu-id="63ded-265">(24)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-266">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-266">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="63ded-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="63ded-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="63ded-268">(25)</span><span class="sxs-lookup"><span data-stu-id="63ded-268">(25)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-269">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="63ded-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="63ded-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="63ded-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="63ded-271">(26)</span><span class="sxs-lookup"><span data-stu-id="63ded-271">(26)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-272">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="63ded-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="63ded-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="63ded-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="63ded-274">(27)</span><span class="sxs-lookup"><span data-stu-id="63ded-274">(27)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-275">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="63ded-275">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="63ded-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="63ded-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="63ded-277">(28)</span><span class="sxs-lookup"><span data-stu-id="63ded-277">(28)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-278">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-278">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="63ded-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="63ded-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="63ded-280">(29)</span><span class="sxs-lookup"><span data-stu-id="63ded-280">(29)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-281">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="63ded-281">Device is disabled.</span></span> <span data-ttu-id="63ded-282">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="63ded-282">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="63ded-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="63ded-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="63ded-284">(30)</span><span class="sxs-lookup"><span data-stu-id="63ded-284">(30)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-285">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63ded-285">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="63ded-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="63ded-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="63ded-287">31,5</span><span class="sxs-lookup"><span data-stu-id="63ded-287">(31)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-288">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="63ded-288">Device is not working properly.</span></span> <span data-ttu-id="63ded-289">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-289">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63ded-290">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="63ded-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-291">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="63ded-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-293">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="63ded-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-294">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="63ded-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="63ded-295">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-296">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="63ded-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-299">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63ded-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63ded-300">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63ded-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="63ded-301">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="63ded-302">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-303">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63ded-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-306">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="63ded-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-307">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="63ded-307">Textual description of the object.</span></span>

<span data-ttu-id="63ded-308">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="63ded-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-312">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63ded-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63ded-313">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="63ded-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="63ded-314">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-315">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="63ded-315">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-316">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="63ded-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63ded-318">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="63ded-318">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="63ded-319">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-320">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="63ded-320">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63ded-323">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="63ded-323">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="63ded-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-325">**Estimatedchargeremainung**</span><span class="sxs-lookup"><span data-stu-id="63ded-325">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-326">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63ded-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-328">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UPS Akku \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Prozent ")</span><span class="sxs-lookup"><span data-stu-id="63ded-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-329">Prozentuale Schätzung der verbleibenden vollständigen Kosten für einen UPS, der Akku Technologie verwendet.</span><span class="sxs-lookup"><span data-stu-id="63ded-329">Percentage estimate of the remaining full charge for a UPS that uses battery technology.</span></span>

</dd> <dt>

<span data-ttu-id="63ded-330">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="63ded-330">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-331">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-333">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UPS Akku \| 001,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Minuten ")</span><span class="sxs-lookup"><span data-stu-id="63ded-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-334">Geschätzte Zeit (in Minuten), bis der Akku, Generator oder die andere Stromquelle unter den aktuellen Ladebedingungen erschöpft ist, wenn die Stromversorgung ausgeschaltet ist oder verloren geht und ausfällt.</span><span class="sxs-lookup"><span data-stu-id="63ded-334">Estimated time, in minutes, until the battery, generator, or other power source is depleted under the present load conditions if the utility power is off, or is lost and remains off.</span></span>

</dd> <dt>

<span data-ttu-id="63ded-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="63ded-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-336">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="63ded-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-338">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="63ded-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-339">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="63ded-339">Date and time the object was installed.</span></span> <span data-ttu-id="63ded-340">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="63ded-341">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-342">**Isswitchingsupply**</span><span class="sxs-lookup"><span data-stu-id="63ded-342">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-343">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="63ded-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63ded-345">Wenn der Wert **true** ist, ist das Netzteil ein Wechsel (anstatt linear).</span><span class="sxs-lookup"><span data-stu-id="63ded-345">If **TRUE**, the power supply is a switching (rather than linear) supply.</span></span>

<span data-ttu-id="63ded-346">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-346">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="63ded-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-348">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63ded-350">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="63ded-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="63ded-351">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-352">**Name**</span><span class="sxs-lookup"><span data-stu-id="63ded-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-355">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="63ded-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-356">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-356">Label by which the object is known.</span></span> <span data-ttu-id="63ded-357">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="63ded-358">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-359">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="63ded-359">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-362">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="63ded-362">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-363">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="63ded-363">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="63ded-364">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="63ded-365">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="63ded-365">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="63ded-366">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="63ded-366">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-367">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="63ded-367">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="63ded-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63ded-369">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="63ded-369">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="63ded-370">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-370">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63ded-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="63ded-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="63ded-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="63ded-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="63ded-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="63ded-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="63ded-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="63ded-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-375">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="63ded-375">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="63ded-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="63ded-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-377">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="63ded-377">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="63ded-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="63ded-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-379">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63ded-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="63ded-380">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-380">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="63ded-381">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="63ded-381">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="63ded-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="63ded-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-383">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-383">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="63ded-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="63ded-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-385">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-385">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63ded-386">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="63ded-386">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-387">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="63ded-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63ded-389">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="63ded-389">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="63ded-390">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="63ded-390">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="63ded-391">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-391">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="63ded-392">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="63ded-392">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="63ded-393">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-394">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="63ded-394">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-395">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-395">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-397">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="63ded-397">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-398">Häufigkeit in Hertz am höchst Ende des Eingabe Häufigkeits Bereichs 1 der Stromversorgung.</span><span class="sxs-lookup"><span data-stu-id="63ded-398">Frequency, in hertz, at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="63ded-399">Der Wert 0 (null) impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="63ded-399">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="63ded-400">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-400">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-401">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="63ded-401">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-402">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-404">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,17 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="63ded-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-405">Häufigkeit in Hertz am unteren Ende des Eingabe Häufigkeits Bereichs 1 der Stromversorgung.</span><span class="sxs-lookup"><span data-stu-id="63ded-405">Frequency, in hertz, at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="63ded-406">Der Wert 0 (null) impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="63ded-406">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="63ded-407">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-407">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-408">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="63ded-408">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-409">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-411">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Range1InputVoltageHigh"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millivolt")</span><span class="sxs-lookup"><span data-stu-id="63ded-411">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-412">Wenn die Spannung in Millivolt den von der **Range1InputVoltageHigh** -Eigenschaft angegebenen Wert übersteigt, wird die Spannung durch kürzen der Spannung kompensiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-412">If the voltage, in millivolts, rises above the value specified by the **Range1InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="63ded-413">Der Wert 0 (null) gibt an, dass die Spannung, bei der der Trimmen auftritt, unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-413">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="63ded-414">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-414">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-415">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="63ded-415">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-416">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-418">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Range1InputVoltageLow"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millivolt")</span><span class="sxs-lookup"><span data-stu-id="63ded-418">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-419">Wenn die Spannung in Millivolt unter den von der **Range1InputVoltageLow** -Eigenschaft angegebenen Wert fällt, werden die-UPS durch die Verstärkung der Spannung mithilfe der entsprechenden Stromquellen kompensiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-419">If the voltage, in millivolts, drops below the value specified by the **Range1InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="63ded-420">Der Wert 0 gibt an, dass die Spannung, bei der die Verstärkung auftritt, unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-420">A value of 0 indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="63ded-421">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-421">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-422">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="63ded-422">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-423">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-423">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-425">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,20 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="63ded-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-426">Häufigkeit in Hertz am höchst Ende des Eingabe Häufigkeits Bereichs der Stromversorgung 2.</span><span class="sxs-lookup"><span data-stu-id="63ded-426">Frequency, in hertz, at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="63ded-427">Der Wert 0 (null) impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="63ded-427">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="63ded-428">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-428">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-429">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="63ded-429">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-430">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-432">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,19 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="63ded-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-433">Häufigkeit in Hertz am unteren Ende des Eingabe Frequenzbereichs der Stromversorgung 2.</span><span class="sxs-lookup"><span data-stu-id="63ded-433">Frequency, in hertz, at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="63ded-434">Der Wert 0 impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="63ded-434">A value of 0 implies DC.</span></span>

<span data-ttu-id="63ded-435">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-435">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-436">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="63ded-436">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-437">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-437">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-438">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-439">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Range2InputVoltageHigh"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millivolt")</span><span class="sxs-lookup"><span data-stu-id="63ded-439">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-440">Wenn die Spannung in Millivolt den von der **Range2InputVoltageHigh** -Eigenschaft angegebenen Wert übersteigt, wird die Spannung durch kürzen der Spannung kompensiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-440">If the voltage, in millivolts, rises above the value specified by the **Range2InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="63ded-441">Der Wert 0 (null) gibt an, dass die Spannung, bei der der Trimmen auftritt, unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-441">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="63ded-442">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-442">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-443">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="63ded-443">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-444">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-444">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-446">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Range2InputVoltageLow"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millivolt")</span><span class="sxs-lookup"><span data-stu-id="63ded-446">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-447">Wenn die Spannung in Millivolt unter den von der **Range2InputVoltageLow** -Eigenschaft angegebenen Wert fällt, werden die-UPS durch die Verstärkung der Spannung mithilfe der entsprechenden Stromquellen kompensiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-447">If the voltage, in millivolts, drops below the value specified by the **Range2InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="63ded-448">Der Wert 0 (null) gibt an, dass die Spannung, bei der die Verstärkung auftritt, unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-448">A value of 0 (zero) indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="63ded-449">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-449">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-450">**Restingcapacitystatus**</span><span class="sxs-lookup"><span data-stu-id="63ded-450">**RemainingCapacityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-451">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63ded-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-453">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UPS Akku \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="63ded-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-454">Angabe der Kapazität, die in den Akkus, dem Generator oder einer anderen Quelle des UPS verbleiben.</span><span class="sxs-lookup"><span data-stu-id="63ded-454">Indication of the capacity remaining in the UPS's batteries, generator, or other source.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63ded-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="63ded-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="63ded-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span><span class="sxs-lookup"><span data-stu-id="63ded-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-457">Die verbleibenden geschätzten Minuten der Laufzeit sind größer als der definierte Zustand des UPS (in der Regel zwei Minuten).</span><span class="sxs-lookup"><span data-stu-id="63ded-457">Remaining estimated minutes of run-time is greater than the UPS's defined low-power state (typically, two minutes).</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="63ded-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (3)</span><span class="sxs-lookup"><span data-stu-id="63ded-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (3)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-459">Die verbleibenden geschätzten Minuten der Laufzeit sind kleiner als oder gleich dem definierten Zustand des UPS mit niedrigem Energiezustand.</span><span class="sxs-lookup"><span data-stu-id="63ded-459">Remaining estimated minutes of run-time is less than or equal to the UPS's defined low-power state.</span></span>

</dd> <dt>

<span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>

<span data-ttu-id="63ded-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Erschöpft** (4)</span><span class="sxs-lookup"><span data-stu-id="63ded-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Depleted** (4)</span></span>


</dt> <dd>

<span data-ttu-id="63ded-461">Die UPS können den aktuellen Ladevorgang nicht aufrechterhalten, wenn die Stromversorgung verloren geht (einschließlich der Möglichkeit, dass die Stromversorgung derzeit nicht vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="63ded-461">The UPS will be unable to sustain the present load when the utility power is lost (including the possibility that the utility power is currently absent).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="63ded-462">**Status**</span><span class="sxs-lookup"><span data-stu-id="63ded-462">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-463">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-464">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-465">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="63ded-465">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-466">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="63ded-466">Current status of the object.</span></span> <span data-ttu-id="63ded-467">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-467">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="63ded-468">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="63ded-468">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="63ded-469">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="63ded-469">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="63ded-470">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="63ded-470">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="63ded-471">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="63ded-471">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63ded-472">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="63ded-472">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="63ded-473">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="63ded-473">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="63ded-474">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="63ded-474">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="63ded-475">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="63ded-475">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="63ded-476">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="63ded-476">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="63ded-477">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="63ded-477">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="63ded-478">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="63ded-478">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="63ded-479">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="63ded-479">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="63ded-480">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="63ded-480">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63ded-481">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="63ded-481">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-482">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63ded-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-483">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-484">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="63ded-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-485">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="63ded-485">State of the logical device.</span></span> <span data-ttu-id="63ded-486">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63ded-486">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="63ded-487">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63ded-488">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="63ded-488">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63ded-489">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="63ded-489">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="63ded-490">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="63ded-490">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="63ded-491">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="63ded-491">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="63ded-492">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="63ded-492">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63ded-493">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="63ded-493">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-494">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-496">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63ded-496">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63ded-497">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="63ded-497">Scoping system's creation class name.</span></span>

<span data-ttu-id="63ded-498">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-498">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-499">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="63ded-499">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-500">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63ded-500">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-501">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-502">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="63ded-502">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="63ded-503">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="63ded-503">Scoping system's name.</span></span>

<span data-ttu-id="63ded-504">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-504">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-505">**TimeOnBackup**</span><span class="sxs-lookup"><span data-stu-id="63ded-505">**TimeOnBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-506">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-508">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UPS Akku \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Sekunden ")</span><span class="sxs-lookup"><span data-stu-id="63ded-508">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-509">Verstrichene Zeit (in Sekunden), seit die UPS zuletzt auf Akku Strom, Generator oder andere Stromquelle umgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="63ded-509">Elapsed time, in seconds, since the UPS last switched to battery power, generator, or other power source.</span></span> <span data-ttu-id="63ded-510">Oder der Zeitpunkt seit dem letzten Neustart des UPS, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="63ded-510">Or, the time since the UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="63ded-511">Wenn die UPS Online ist, wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63ded-511">If the UPS is online, 0 (zero) will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="63ded-512">**Totaloutputpower**</span><span class="sxs-lookup"><span data-stu-id="63ded-512">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-513">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ded-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-515">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,21 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt ")</span><span class="sxs-lookup"><span data-stu-id="63ded-515">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-516">Gesamtausgabe der Stromversorgung (in Milliwatt).</span><span class="sxs-lookup"><span data-stu-id="63ded-516">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="63ded-517">Der Wert 0 (null) gibt unbekannt an.</span><span class="sxs-lookup"><span data-stu-id="63ded-517">A value of 0 (zero) denotes unknown.</span></span>

<span data-ttu-id="63ded-518">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-518">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="63ded-519">**Typeofrangeswitch**</span><span class="sxs-lookup"><span data-stu-id="63ded-519">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ded-520">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="63ded-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="63ded-521">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63ded-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ded-522">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="63ded-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="63ded-523">Typ des im Netzteil implementierten Wechsel Spannungsbereichs Wechsels.</span><span class="sxs-lookup"><span data-stu-id="63ded-523">Type of input-voltage range switching implemented in the power supply.</span></span>

<span data-ttu-id="63ded-524">Diese Eigenschaft wird vom [**CIM- \_ Netzteil**](cim-powersupply.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="63ded-524">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="63ded-525">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="63ded-525">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63ded-526">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="63ded-526">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="63ded-527">**Manuell** (3)</span><span class="sxs-lookup"><span data-stu-id="63ded-527">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="63ded-528">**Autoswitch** (4)</span><span class="sxs-lookup"><span data-stu-id="63ded-528">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="63ded-529">**Breite Bereich** (5)</span><span class="sxs-lookup"><span data-stu-id="63ded-529">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="63ded-530">**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="63ded-530">**Not Applicable** (6)</span></span>


<span data-ttu-id="63ded-531"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="63ded-531"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="63ded-532">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63ded-532">Remarks</span></span>

<span data-ttu-id="63ded-533">Die **CIM-Klasse \_ uninterruptiblepowersupply** wird von [**CIM- \_ Netzteil**](cim-powersupply.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="63ded-533">The **CIM\_UninterruptiblePowerSupply** class is derived from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="63ded-534">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="63ded-534">WMI does not implement this class.</span></span> <span data-ttu-id="63ded-535">Informationen zu WMI-Klassen, die von **CIM \_ uninterruptiblepowersupply** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="63ded-535">For WMI classes derived from **CIM\_UninterruptiblePowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="63ded-536">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="63ded-536">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="63ded-537">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="63ded-537">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="63ded-538">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63ded-538">Requirements</span></span>



| <span data-ttu-id="63ded-539">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63ded-539">Requirement</span></span> | <span data-ttu-id="63ded-540">Wert</span><span class="sxs-lookup"><span data-stu-id="63ded-540">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63ded-541">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63ded-541">Minimum supported client</span></span><br/> | <span data-ttu-id="63ded-542">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63ded-542">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63ded-543">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63ded-543">Minimum supported server</span></span><br/> | <span data-ttu-id="63ded-544">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63ded-544">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63ded-545">Namespace</span><span class="sxs-lookup"><span data-stu-id="63ded-545">Namespace</span></span><br/>                | <span data-ttu-id="63ded-546">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="63ded-546">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63ded-547">MOF</span><span class="sxs-lookup"><span data-stu-id="63ded-547">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63ded-548"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="63ded-548"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63ded-549">DLL</span><span class="sxs-lookup"><span data-stu-id="63ded-549">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63ded-550"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63ded-550"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ded-551">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63ded-551">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ded-552">**CIM- \_ Netzteil**</span><span class="sxs-lookup"><span data-stu-id="63ded-552">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

