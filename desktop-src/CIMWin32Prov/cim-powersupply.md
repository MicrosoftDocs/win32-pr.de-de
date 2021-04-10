---
description: Die CIM \_ -PowerSupply-Klasse stellt die Funktionen und die Verwaltung des logischen netzwerknetzwerkgeräts dar.
ms.assetid: a9b79564-01d9-42a4-8586-782f179c179f
ms.tgt_platform: multiple
title: CIM_PowerSupply-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply
- CIM_PowerSupply.ActiveInputVoltage
- CIM_PowerSupply.Availability
- CIM_PowerSupply.Caption
- CIM_PowerSupply.ConfigManagerErrorCode
- CIM_PowerSupply.ConfigManagerUserConfig
- CIM_PowerSupply.CreationClassName
- CIM_PowerSupply.Description
- CIM_PowerSupply.DeviceID
- CIM_PowerSupply.ErrorCleared
- CIM_PowerSupply.ErrorDescription
- CIM_PowerSupply.InstallDate
- CIM_PowerSupply.IsSwitchingSupply
- CIM_PowerSupply.LastErrorCode
- CIM_PowerSupply.Name
- CIM_PowerSupply.PNPDeviceID
- CIM_PowerSupply.PowerManagementCapabilities
- CIM_PowerSupply.PowerManagementSupported
- CIM_PowerSupply.Range1InputFrequencyHigh
- CIM_PowerSupply.Range1InputFrequencyLow
- CIM_PowerSupply.Range1InputVoltageHigh
- CIM_PowerSupply.Range1InputVoltageLow
- CIM_PowerSupply.Range2InputFrequencyHigh
- CIM_PowerSupply.Range2InputFrequencyLow
- CIM_PowerSupply.Range2InputVoltageHigh
- CIM_PowerSupply.Range2InputVoltageLow
- CIM_PowerSupply.Status
- CIM_PowerSupply.StatusInfo
- CIM_PowerSupply.SystemCreationClassName
- CIM_PowerSupply.SystemName
- CIM_PowerSupply.TotalOutputPower
- CIM_PowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35a1eb73c258b800bb8b33ad7aa75ea86cd0ef4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214125"
---
# <a name="cim_powersupply-class"></a><span data-ttu-id="27399-103">CIM- \_ PowerSupply-Klasse</span><span class="sxs-lookup"><span data-stu-id="27399-103">CIM\_PowerSupply class</span></span>

<span data-ttu-id="27399-104">Die **CIM- \_ PowerSupply** -Klasse stellt die Funktionen und die Verwaltung des logischen netzwerknetzwerkgeräts dar.</span><span class="sxs-lookup"><span data-stu-id="27399-104">The **CIM\_PowerSupply** class represents the capabilities and management of the power supply logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27399-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="27399-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="27399-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="27399-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="27399-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27399-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="27399-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="27399-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="27399-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="27399-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C547-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PowerSupply : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="27399-110">Member</span><span class="sxs-lookup"><span data-stu-id="27399-110">Members</span></span>

<span data-ttu-id="27399-111">Die **CIM- \_ PowerSupply** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="27399-111">The **CIM\_PowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="27399-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="27399-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="27399-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27399-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="27399-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="27399-114">Methods</span></span>

<span data-ttu-id="27399-115">Die **CIM- \_ PowerSupply** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="27399-115">The **CIM\_PowerSupply** class has these methods.</span></span>



| <span data-ttu-id="27399-116">Methode</span><span class="sxs-lookup"><span data-stu-id="27399-116">Method</span></span>                                                                 | <span data-ttu-id="27399-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27399-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27399-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="27399-118">**Reset**</span></span>](reset-method-in-class-cim-powersupply.md)                 | <span data-ttu-id="27399-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="27399-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="27399-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="27399-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="27399-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="27399-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-powersupply.md) | <span data-ttu-id="27399-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27399-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="27399-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="27399-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="27399-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27399-124">Properties</span></span>

<span data-ttu-id="27399-125">Die **CIM- \_ PowerSupply** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27399-125">The **CIM\_PowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27399-126">**Activinput Spannung**</span><span class="sxs-lookup"><span data-stu-id="27399-126">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27399-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27399-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="27399-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="27399-130">Der Spannungsbereich, der zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27399-130">Voltage range that is currently in use.</span></span> <span data-ttu-id="27399-131">Wenn die Bereitstellung derzeit keine Zeichenkraft ist, kann der Wert 6 ("keine") angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="27399-131">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="27399-132">Diese Informationen sind erforderlich, wenn eine unterbrechungsfreie Stromversorgung (USV), eine Unterklasse des **CIM- \_ Netzteils**, erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="27399-132">This information is necessary in the case of an uninterruptible power supply (UPS), a subclass of **CIM\_PowerSupply**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27399-133">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="27399-133">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27399-134">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="27399-134">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="27399-135">**Bereich 1** (3)</span><span class="sxs-lookup"><span data-stu-id="27399-135">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="27399-136">**Bereich 2** (4)</span><span class="sxs-lookup"><span data-stu-id="27399-136">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="27399-137">**Beides** (5)</span><span class="sxs-lookup"><span data-stu-id="27399-137">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="27399-138">**Keines der beiden** (6)</span><span class="sxs-lookup"><span data-stu-id="27399-138">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27399-139">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="27399-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27399-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27399-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-142">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="27399-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="27399-143">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="27399-143">Availability and status of the device.</span></span>

<span data-ttu-id="27399-144">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27399-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="27399-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27399-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="27399-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="27399-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="27399-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="27399-148">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="27399-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="27399-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="27399-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="27399-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="27399-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="27399-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="27399-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="27399-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="27399-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="27399-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="27399-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="27399-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="27399-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="27399-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="27399-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="27399-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="27399-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="27399-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="27399-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="27399-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="27399-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="27399-159">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="27399-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="27399-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="27399-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="27399-161">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="27399-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="27399-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="27399-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="27399-163">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="27399-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="27399-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="27399-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="27399-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="27399-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="27399-166">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="27399-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="27399-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="27399-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="27399-168">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="27399-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="27399-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="27399-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="27399-170">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="27399-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="27399-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="27399-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="27399-172">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="27399-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="27399-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="27399-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="27399-174">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="27399-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27399-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="27399-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-178">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="27399-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="27399-179">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="27399-179">Short textual description of the object.</span></span>

<span data-ttu-id="27399-180">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-181">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="27399-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-184">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27399-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27399-185">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="27399-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="27399-186">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="27399-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="27399-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="27399-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="27399-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="27399-189">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="27399-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="27399-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="27399-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="27399-191">(1)</span><span class="sxs-lookup"><span data-stu-id="27399-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="27399-192">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="27399-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27399-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="27399-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="27399-194">(2)</span><span class="sxs-lookup"><span data-stu-id="27399-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="27399-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="27399-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="27399-196">(3)</span><span class="sxs-lookup"><span data-stu-id="27399-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="27399-197">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="27399-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="27399-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="27399-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="27399-199">(4)</span><span class="sxs-lookup"><span data-stu-id="27399-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="27399-200">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="27399-200">Device is not working properly.</span></span> <span data-ttu-id="27399-201">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="27399-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="27399-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="27399-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="27399-203">(5)</span><span class="sxs-lookup"><span data-stu-id="27399-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="27399-204">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="27399-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="27399-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="27399-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="27399-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="27399-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="27399-207">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="27399-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="27399-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="27399-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="27399-209">(7)</span><span class="sxs-lookup"><span data-stu-id="27399-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="27399-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="27399-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="27399-211">(8)</span><span class="sxs-lookup"><span data-stu-id="27399-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="27399-212">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="27399-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="27399-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="27399-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="27399-214">(9)</span><span class="sxs-lookup"><span data-stu-id="27399-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="27399-215">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="27399-215">Device is not working properly.</span></span> <span data-ttu-id="27399-216">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="27399-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="27399-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="27399-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="27399-218">(10)</span><span class="sxs-lookup"><span data-stu-id="27399-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="27399-219">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="27399-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="27399-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="27399-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="27399-221">(11)</span><span class="sxs-lookup"><span data-stu-id="27399-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="27399-222">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="27399-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="27399-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="27399-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="27399-224">(12)</span><span class="sxs-lookup"><span data-stu-id="27399-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="27399-225">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="27399-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="27399-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="27399-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="27399-227">(13)</span><span class="sxs-lookup"><span data-stu-id="27399-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="27399-228">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="27399-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="27399-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="27399-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="27399-230">(14)</span><span class="sxs-lookup"><span data-stu-id="27399-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="27399-231">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="27399-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="27399-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="27399-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="27399-233">(15)</span><span class="sxs-lookup"><span data-stu-id="27399-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="27399-234">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="27399-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="27399-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="27399-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="27399-236">(16)</span><span class="sxs-lookup"><span data-stu-id="27399-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="27399-237">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27399-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="27399-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="27399-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="27399-239">(17)</span><span class="sxs-lookup"><span data-stu-id="27399-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="27399-240">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="27399-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27399-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="27399-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="27399-242">(18)</span><span class="sxs-lookup"><span data-stu-id="27399-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="27399-243">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="27399-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="27399-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="27399-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="27399-245">(19)</span><span class="sxs-lookup"><span data-stu-id="27399-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="27399-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="27399-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="27399-247">(20)</span><span class="sxs-lookup"><span data-stu-id="27399-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="27399-248">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="27399-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="27399-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="27399-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="27399-250">(21)</span><span class="sxs-lookup"><span data-stu-id="27399-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="27399-251">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="27399-251">System failure.</span></span> <span data-ttu-id="27399-252">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="27399-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="27399-253">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="27399-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="27399-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="27399-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="27399-255">(22)</span><span class="sxs-lookup"><span data-stu-id="27399-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="27399-256">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="27399-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="27399-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="27399-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="27399-258">(23)</span><span class="sxs-lookup"><span data-stu-id="27399-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="27399-259">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="27399-259">System failure.</span></span> <span data-ttu-id="27399-260">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="27399-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="27399-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="27399-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="27399-262">(24)</span><span class="sxs-lookup"><span data-stu-id="27399-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="27399-263">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="27399-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="27399-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="27399-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="27399-265">(25)</span><span class="sxs-lookup"><span data-stu-id="27399-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="27399-266">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="27399-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="27399-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="27399-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="27399-268">(26)</span><span class="sxs-lookup"><span data-stu-id="27399-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="27399-269">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="27399-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="27399-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="27399-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="27399-271">(27)</span><span class="sxs-lookup"><span data-stu-id="27399-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="27399-272">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="27399-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="27399-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="27399-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="27399-274">(28)</span><span class="sxs-lookup"><span data-stu-id="27399-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="27399-275">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="27399-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="27399-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="27399-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="27399-277">(29)</span><span class="sxs-lookup"><span data-stu-id="27399-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="27399-278">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="27399-278">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="27399-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="27399-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="27399-280">(30)</span><span class="sxs-lookup"><span data-stu-id="27399-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="27399-281">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27399-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27399-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="27399-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="27399-283">31,5</span><span class="sxs-lookup"><span data-stu-id="27399-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="27399-284">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="27399-284">Device is not working properly.</span></span> <span data-ttu-id="27399-285">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="27399-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27399-286">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="27399-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-287">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27399-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27399-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-289">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27399-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27399-290">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="27399-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="27399-291">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-292">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="27399-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-295">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27399-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27399-296">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27399-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="27399-297">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="27399-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="27399-298">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-299">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27399-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-302">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="27399-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="27399-303">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="27399-303">Textual description of the object.</span></span>

<span data-ttu-id="27399-304">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="27399-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-308">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27399-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27399-309">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="27399-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="27399-310">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-311">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="27399-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-312">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27399-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27399-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27399-314">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="27399-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="27399-315">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="27399-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27399-319">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="27399-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="27399-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="27399-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-322">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="27399-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="27399-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-324">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="27399-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="27399-325">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="27399-325">Date and time the object was installed.</span></span> <span data-ttu-id="27399-326">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="27399-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="27399-327">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-328">**Isswitchingsupply**</span><span class="sxs-lookup"><span data-stu-id="27399-328">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-329">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27399-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27399-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27399-331">**True** gibt an, dass das Netzteil eine Wechsel-(oder lineare) Angabe ist.</span><span class="sxs-lookup"><span data-stu-id="27399-331">If **TRUE**, the power supply is a switching (versus linear) supply.</span></span>

</dd> <dt>

<span data-ttu-id="27399-332">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="27399-332">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-333">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27399-335">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="27399-335">Last error code reported by the logical device.</span></span>

<span data-ttu-id="27399-336">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-337">**Name**</span><span class="sxs-lookup"><span data-stu-id="27399-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-340">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="27399-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="27399-341">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="27399-341">Label by which the object is known.</span></span> <span data-ttu-id="27399-342">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="27399-342">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="27399-343">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="27399-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-347">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27399-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27399-348">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="27399-348">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="27399-349">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="27399-350">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="27399-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="27399-351">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="27399-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-352">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="27399-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27399-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27399-354">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="27399-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="27399-355">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27399-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="27399-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="27399-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="27399-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="27399-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="27399-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="27399-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="27399-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="27399-360">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27399-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="27399-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="27399-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="27399-362">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="27399-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="27399-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="27399-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="27399-364">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27399-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="27399-365">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="27399-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="27399-366">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="27399-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="27399-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="27399-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="27399-368">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27399-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="27399-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="27399-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="27399-370">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27399-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27399-371">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="27399-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-372">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27399-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27399-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27399-374">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="27399-374">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="27399-375">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="27399-375">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="27399-376">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="27399-376">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="27399-377">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="27399-377">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="27399-378">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-379">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="27399-379">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-380">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-382">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="27399-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="27399-383">Häufigkeit (in Hertz) am Ende des Eingabe Frequenzbereichs 1 der Stromversorgung.</span><span class="sxs-lookup"><span data-stu-id="27399-383">Frequency (in hertz) at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="27399-384">Der Wert 0 impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="27399-384">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="27399-385">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="27399-385">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-386">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-388">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,17 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="27399-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="27399-389">Häufigkeit (in Hertz) am unteren Ende des Eingabe Frequenzbereichs 1 der Stromversorgung.</span><span class="sxs-lookup"><span data-stu-id="27399-389">Frequency (in hertz) at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="27399-390">Der Wert 0 impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="27399-390">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="27399-391">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="27399-391">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-392">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-394">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="27399-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27399-395">Hohe Spannung des Eingangs Spannungsbereichs 1 für das Netzteil (in Millivolt).</span><span class="sxs-lookup"><span data-stu-id="27399-395">High voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="27399-396">Der Wert 0 steht für "unbekannt".</span><span class="sxs-lookup"><span data-stu-id="27399-396">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="27399-397">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="27399-397">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-398">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-400">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="27399-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27399-401">Niedrige Spannung des Eingangs Spannungsbereichs 1 für das Netzteil (in Millivolt).</span><span class="sxs-lookup"><span data-stu-id="27399-401">Low voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="27399-402">Der Wert 0 steht für "unbekannt".</span><span class="sxs-lookup"><span data-stu-id="27399-402">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="27399-403">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="27399-403">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-404">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-406">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,20 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="27399-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="27399-407">Häufigkeit (in Hertz) am höchst Ende des Eingabe Häufigkeits Bereichs der Stromversorgung 2.</span><span class="sxs-lookup"><span data-stu-id="27399-407">Frequency (in hertz) at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="27399-408">Der Wert 0 impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="27399-408">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="27399-409">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="27399-409">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-410">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-412">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,19 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="27399-412">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="27399-413">Häufigkeit (in Hertz) am unteren Ende des Eingabe Frequenzbereichs der Stromversorgung 2.</span><span class="sxs-lookup"><span data-stu-id="27399-413">Frequency (in hertz) at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="27399-414">Der Wert 0 impliziert DC.</span><span class="sxs-lookup"><span data-stu-id="27399-414">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="27399-415">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="27399-415">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-416">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-418">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,12 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="27399-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27399-419">Hohe Spannung des Eingangs Spannungsbereichs 2 für das Netzteil (in Millivolt).</span><span class="sxs-lookup"><span data-stu-id="27399-419">High voltage of input voltage range 2 for the power supply, in millivolts.</span></span> <span data-ttu-id="27399-420">Der Wert 0 steht für "unbekannt".</span><span class="sxs-lookup"><span data-stu-id="27399-420">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="27399-421">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="27399-421">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-422">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-422">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-424">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="27399-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27399-425">Niedrige Spannung des Eingangs Spannungsbereichs 2 für dieses Netzteil (in Millivolt).</span><span class="sxs-lookup"><span data-stu-id="27399-425">Low voltage of input voltage range 2 for this power supply, in Millivolts.</span></span> <span data-ttu-id="27399-426">Der Wert 0 steht für "unbekannt".</span><span class="sxs-lookup"><span data-stu-id="27399-426">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="27399-427">**Status**</span><span class="sxs-lookup"><span data-stu-id="27399-427">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-430">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="27399-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="27399-431">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="27399-431">Current status of the object.</span></span>

<span data-ttu-id="27399-432">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="27399-433">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="27399-433">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="27399-434">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="27399-434">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="27399-435">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="27399-435">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="27399-436">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="27399-436">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27399-437">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="27399-437">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="27399-438">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="27399-438">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="27399-439">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="27399-439">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="27399-440">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="27399-440">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="27399-441">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="27399-441">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="27399-442">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="27399-442">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="27399-443">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="27399-443">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="27399-444">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="27399-444">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="27399-445">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="27399-445">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27399-446">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="27399-446">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-447">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27399-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27399-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-449">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="27399-449">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="27399-450">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="27399-450">State of the logical device.</span></span> <span data-ttu-id="27399-451">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27399-451">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="27399-452">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27399-453">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="27399-453">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27399-454">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="27399-454">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="27399-455">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="27399-455">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="27399-456">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="27399-456">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="27399-457">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="27399-457">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27399-458">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="27399-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-459">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-461">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27399-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27399-462">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="27399-462">Scoping system's creation class name.</span></span>

<span data-ttu-id="27399-463">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-464">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="27399-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-465">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27399-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27399-466">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-467">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="27399-467">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="27399-468">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="27399-468">Scoping system's name.</span></span>

<span data-ttu-id="27399-469">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27399-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27399-470">**Totaloutputpower**</span><span class="sxs-lookup"><span data-stu-id="27399-470">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-471">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27399-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27399-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-473">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,21 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt ")</span><span class="sxs-lookup"><span data-stu-id="27399-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="27399-474">Gesamtausgabe der Stromversorgung (in Milliwatt).</span><span class="sxs-lookup"><span data-stu-id="27399-474">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="27399-475">Der Wert 0 steht für "unbekannt".</span><span class="sxs-lookup"><span data-stu-id="27399-475">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="27399-476">**Typeofrangeswitch**</span><span class="sxs-lookup"><span data-stu-id="27399-476">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27399-477">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27399-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27399-478">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27399-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27399-479">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzteil \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="27399-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="27399-480">Typ des Umschaltens für Eingabe Spannungsbereiche, der in der Netzteil implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="27399-480">Type of input voltage range switching implemented in the power supply.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27399-481">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="27399-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27399-482">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="27399-482">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="27399-483">**Manuell** (3)</span><span class="sxs-lookup"><span data-stu-id="27399-483">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="27399-484">**Autoswitch** (4)</span><span class="sxs-lookup"><span data-stu-id="27399-484">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="27399-485">**Breite Bereich** (5)</span><span class="sxs-lookup"><span data-stu-id="27399-485">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="27399-486">**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="27399-486">**Not Applicable** (6)</span></span>


<span data-ttu-id="27399-487"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="27399-487"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="27399-488">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27399-488">Remarks</span></span>

<span data-ttu-id="27399-489">Die **CIM- \_ PowerSupply** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="27399-489">The **CIM\_PowerSupply** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="27399-490">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="27399-490">WMI does not implement this class.</span></span> <span data-ttu-id="27399-491">Informationen zu WMI, die von **CIM- \_ PowerSupply** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="27399-491">For WMI classed derived from **CIM\_PowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="27399-492">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="27399-492">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="27399-493">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="27399-493">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="27399-494">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27399-494">Requirements</span></span>



| <span data-ttu-id="27399-495">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27399-495">Requirement</span></span> | <span data-ttu-id="27399-496">Wert</span><span class="sxs-lookup"><span data-stu-id="27399-496">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27399-497">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27399-497">Minimum supported client</span></span><br/> | <span data-ttu-id="27399-498">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27399-498">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27399-499">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27399-499">Minimum supported server</span></span><br/> | <span data-ttu-id="27399-500">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27399-500">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27399-501">Namespace</span><span class="sxs-lookup"><span data-stu-id="27399-501">Namespace</span></span><br/>                | <span data-ttu-id="27399-502">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="27399-502">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27399-503">MOF</span><span class="sxs-lookup"><span data-stu-id="27399-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27399-504"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="27399-504"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27399-505">DLL</span><span class="sxs-lookup"><span data-stu-id="27399-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27399-506"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27399-506"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27399-507">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27399-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27399-508">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="27399-508">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

