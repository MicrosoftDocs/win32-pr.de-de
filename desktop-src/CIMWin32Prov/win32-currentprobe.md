---
description: Die Win32 \_ currentprobe-WMI-Klasse stellt die Eigenschaften eines aktuellen Überwachungs Sensors (Ammeter) dar.
ms.assetid: 2e1da856-b787-404b-ac4b-080c4950bad8
ms.tgt_platform: multiple
title: Win32_CurrentProbe-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CurrentProbe
- Win32_CurrentProbe.Reset
- Win32_CurrentProbe.SetPowerState
- Win32_CurrentProbe.Accuracy
- Win32_CurrentProbe.Availability
- Win32_CurrentProbe.Caption
- Win32_CurrentProbe.ConfigManagerErrorCode
- Win32_CurrentProbe.ConfigManagerUserConfig
- Win32_CurrentProbe.CreationClassName
- Win32_CurrentProbe.CurrentReading
- Win32_CurrentProbe.Description
- Win32_CurrentProbe.DeviceID
- Win32_CurrentProbe.ErrorCleared
- Win32_CurrentProbe.ErrorDescription
- Win32_CurrentProbe.InstallDate
- Win32_CurrentProbe.IsLinear
- Win32_CurrentProbe.LastErrorCode
- Win32_CurrentProbe.LowerThresholdCritical
- Win32_CurrentProbe.LowerThresholdFatal
- Win32_CurrentProbe.LowerThresholdNonCritical
- Win32_CurrentProbe.MaxReadable
- Win32_CurrentProbe.MinReadable
- Win32_CurrentProbe.Name
- Win32_CurrentProbe.NominalReading
- Win32_CurrentProbe.NormalMax
- Win32_CurrentProbe.NormalMin
- Win32_CurrentProbe.PNPDeviceID
- Win32_CurrentProbe.PowerManagementCapabilities
- Win32_CurrentProbe.PowerManagementSupported
- Win32_CurrentProbe.Resolution
- Win32_CurrentProbe.Status
- Win32_CurrentProbe.StatusInfo
- Win32_CurrentProbe.SystemCreationClassName
- Win32_CurrentProbe.SystemName
- Win32_CurrentProbe.Tolerance
- Win32_CurrentProbe.UpperThresholdCritical
- Win32_CurrentProbe.UpperThresholdFatal
- Win32_CurrentProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be834e56eb3d958a8cd6ee653dc9a248c14ae3bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861720"
---
# <a name="win32_currentprobe-class"></a><span data-ttu-id="b6277-103">Win32 \_ currentprobe-Klasse</span><span class="sxs-lookup"><span data-stu-id="b6277-103">Win32\_CurrentProbe class</span></span>

<span data-ttu-id="b6277-104">Die **Win32 \_ currentprobe** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Eigenschaften eines aktuellen Überwachungs Sensors (Ammeter) dar.</span><span class="sxs-lookup"><span data-stu-id="b6277-104">The **Win32\_CurrentProbe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a current monitoring sensor (ammeter).</span></span>

<span data-ttu-id="b6277-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6277-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b6277-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b6277-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6277-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6277-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABA-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_CurrentProbe : CIM_CurrentSensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="b6277-108">Member</span><span class="sxs-lookup"><span data-stu-id="b6277-108">Members</span></span>

<span data-ttu-id="b6277-109">Die **Win32 \_ currentprobe** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b6277-109">The **Win32\_CurrentProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="b6277-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="b6277-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b6277-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6277-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b6277-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="b6277-112">Methods</span></span>

<span data-ttu-id="b6277-113">Die **Win32 \_ currentprobe** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b6277-113">The **Win32\_CurrentProbe** class has these methods.</span></span>



| <span data-ttu-id="b6277-114">Methode</span><span class="sxs-lookup"><span data-stu-id="b6277-114">Method</span></span>            | <span data-ttu-id="b6277-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6277-115">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6277-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="b6277-116">**Reset**</span></span>         | <span data-ttu-id="b6277-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b6277-117">Not implemented.</span></span> <span data-ttu-id="b6277-118">Informationen zur Implementierung dieser Methode finden Sie in der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ CurrentSensor**](cim-currentsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="b6277-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="b6277-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b6277-119">**SetPowerState**</span></span> | <span data-ttu-id="b6277-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b6277-120">Not implemented.</span></span> <span data-ttu-id="b6277-121">Informationen zur Implementierung dieser Methode finden Sie in der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ CurrentSensor**](cim-currentsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="b6277-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b6277-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6277-122">Properties</span></span>

<span data-ttu-id="b6277-123">Die **Win32 \_ currentprobe** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6277-123">The **Win32\_CurrentProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6277-124">**Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="b6277-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-125">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-127">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Strom, aktueller Test \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="b6277-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-128">Genauigkeit des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b6277-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="b6277-129">Der Wert wird als Plus-oder minus Hundertstel eines Prozentsatzes aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b6277-129">The value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="b6277-130">Die Genauigkeit wird zusammen mit der Auflösung und Toleranz verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b6277-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="b6277-131">Die Genauigkeit kann variieren und hängt davon ab, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-131">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b6277-132">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-133">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="b6277-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6277-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-136">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="b6277-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-137">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="b6277-137">Availability and status of the device.</span></span>

<span data-ttu-id="b6277-138">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b6277-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b6277-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6277-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b6277-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b6277-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="b6277-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-142">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="b6277-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b6277-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="b6277-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b6277-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="b6277-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b6277-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="b6277-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b6277-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="b6277-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b6277-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="b6277-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b6277-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="b6277-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b6277-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="b6277-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b6277-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="b6277-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b6277-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="b6277-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b6277-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="b6277-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-153">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="b6277-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b6277-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="b6277-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-155">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b6277-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b6277-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="b6277-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-157">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b6277-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="b6277-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b6277-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="b6277-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-160">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="b6277-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b6277-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="b6277-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-162">Angehalten.</span><span class="sxs-lookup"><span data-stu-id="b6277-162">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b6277-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="b6277-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-164">Nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="b6277-164">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b6277-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="b6277-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-166">Nicht konfiguriert</span><span class="sxs-lookup"><span data-stu-id="b6277-166">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b6277-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="b6277-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-168">Der aktuelle Sensor ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b6277-168">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b6277-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b6277-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-172">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b6277-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-173">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b6277-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b6277-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-175">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="b6277-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-176">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6277-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-178">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b6277-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-179">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b6277-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b6277-180">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b6277-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="b6277-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b6277-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="b6277-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-183">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b6277-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b6277-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="b6277-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b6277-185">(1)</span><span class="sxs-lookup"><span data-stu-id="b6277-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-186">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b6277-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b6277-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="b6277-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b6277-188">(2)</span><span class="sxs-lookup"><span data-stu-id="b6277-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b6277-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="b6277-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b6277-190">(3)</span><span class="sxs-lookup"><span data-stu-id="b6277-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-191">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b6277-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b6277-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="b6277-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b6277-193">(4)</span><span class="sxs-lookup"><span data-stu-id="b6277-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-194">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b6277-194">Device is not working properly.</span></span> <span data-ttu-id="b6277-195">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b6277-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b6277-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="b6277-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b6277-197">(5)</span><span class="sxs-lookup"><span data-stu-id="b6277-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-198">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6277-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b6277-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="b6277-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b6277-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="b6277-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-201">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="b6277-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b6277-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="b6277-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b6277-203">(7)</span><span class="sxs-lookup"><span data-stu-id="b6277-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b6277-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="b6277-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b6277-205">(8)</span><span class="sxs-lookup"><span data-stu-id="b6277-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-206">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="b6277-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b6277-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="b6277-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b6277-208">(9)</span><span class="sxs-lookup"><span data-stu-id="b6277-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-209">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b6277-209">Device is not working properly.</span></span> <span data-ttu-id="b6277-210">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="b6277-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b6277-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="b6277-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b6277-212">(10)</span><span class="sxs-lookup"><span data-stu-id="b6277-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-213">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b6277-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="b6277-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b6277-215">(11)</span><span class="sxs-lookup"><span data-stu-id="b6277-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-216">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="b6277-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b6277-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="b6277-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b6277-218">(12)</span><span class="sxs-lookup"><span data-stu-id="b6277-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-219">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="b6277-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b6277-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="b6277-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b6277-221">(13)</span><span class="sxs-lookup"><span data-stu-id="b6277-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-222">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b6277-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="b6277-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b6277-224">(14)</span><span class="sxs-lookup"><span data-stu-id="b6277-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-225">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b6277-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="b6277-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b6277-227">(15)</span><span class="sxs-lookup"><span data-stu-id="b6277-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-228">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b6277-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b6277-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="b6277-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b6277-230">(16)</span><span class="sxs-lookup"><span data-stu-id="b6277-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-231">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b6277-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="b6277-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b6277-233">(17)</span><span class="sxs-lookup"><span data-stu-id="b6277-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-234">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="b6277-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b6277-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="b6277-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b6277-236">(18)</span><span class="sxs-lookup"><span data-stu-id="b6277-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-237">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b6277-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="b6277-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b6277-239">(19)</span><span class="sxs-lookup"><span data-stu-id="b6277-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b6277-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="b6277-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b6277-241">(20)</span><span class="sxs-lookup"><span data-stu-id="b6277-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-242">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b6277-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b6277-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="b6277-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b6277-244">(21)</span><span class="sxs-lookup"><span data-stu-id="b6277-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-245">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="b6277-245">System failure.</span></span> <span data-ttu-id="b6277-246">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b6277-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b6277-247">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="b6277-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b6277-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="b6277-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b6277-249">(22)</span><span class="sxs-lookup"><span data-stu-id="b6277-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-250">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b6277-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b6277-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="b6277-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b6277-252">(23)</span><span class="sxs-lookup"><span data-stu-id="b6277-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-253">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="b6277-253">System failure.</span></span> <span data-ttu-id="b6277-254">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b6277-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b6277-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="b6277-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b6277-256">(24)</span><span class="sxs-lookup"><span data-stu-id="b6277-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-257">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="b6277-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b6277-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="b6277-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b6277-259">(25)</span><span class="sxs-lookup"><span data-stu-id="b6277-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-260">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b6277-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b6277-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="b6277-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b6277-262">(26)</span><span class="sxs-lookup"><span data-stu-id="b6277-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-263">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b6277-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b6277-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="b6277-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b6277-265">(27)</span><span class="sxs-lookup"><span data-stu-id="b6277-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-266">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b6277-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b6277-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="b6277-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b6277-268">(28)</span><span class="sxs-lookup"><span data-stu-id="b6277-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-269">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="b6277-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b6277-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="b6277-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b6277-271">(29)</span><span class="sxs-lookup"><span data-stu-id="b6277-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-272">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b6277-272">Device is disabled.</span></span> <span data-ttu-id="b6277-273">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b6277-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b6277-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="b6277-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b6277-275">(30)</span><span class="sxs-lookup"><span data-stu-id="b6277-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-276">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b6277-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="b6277-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b6277-278">31,5</span><span class="sxs-lookup"><span data-stu-id="b6277-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-279">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b6277-279">Device is not working properly.</span></span> <span data-ttu-id="b6277-280">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b6277-281">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="b6277-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-282">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b6277-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-284">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b6277-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-285">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6277-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b6277-286">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-287">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="b6277-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-290">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b6277-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b6277-291">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-291">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b6277-292">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b6277-293">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="b6277-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-295">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-295">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-297">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-297">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-298">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-298">Current value indicated by the sensor.</span></span>

<span data-ttu-id="b6277-299">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-299">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-300">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6277-300">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-303">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b6277-303">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-304">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b6277-304">Description of the object.</span></span>

<span data-ttu-id="b6277-305">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-306">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b6277-306">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-309">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b6277-309">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-310">Eindeutiger Bezeichner des aktuellen Tests.</span><span class="sxs-lookup"><span data-stu-id="b6277-310">Unique identifier of the current probe.</span></span>

<span data-ttu-id="b6277-311">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-312">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="b6277-312">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-313">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b6277-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6277-315">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-315">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b6277-316">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-317">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b6277-317">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6277-320">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="b6277-320">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="b6277-321">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b6277-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-323">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b6277-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-325">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="b6277-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-326">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b6277-326">Date and time the object was installed.</span></span> <span data-ttu-id="b6277-327">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b6277-328">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-329">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="b6277-329">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-330">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b6277-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6277-332">**True** gibt an, dass der Sensor über den dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-332">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="b6277-333">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-333">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b6277-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6277-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6277-337">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b6277-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b6277-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-339">**Lowerstammoldcritical**</span><span class="sxs-lookup"><span data-stu-id="b6277-339">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-340">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-342">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,13 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-342">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-343">Sensor Schwellenwerte geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-343">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether or not the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b6277-344">Wenn **CurrentReading** zwischen **lowerstammoldcritical** und **lowerstammoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="b6277-344">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="b6277-345">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-345">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-346">**Lower-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="b6277-346">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-347">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-347">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-349">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-350">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-350">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b6277-351">Wenn **CurrentReading** unterhalb von **lowerveroldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="b6277-351">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="b6277-352">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-352">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-353">**Lower-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="b6277-353">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-354">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-354">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-356">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-357">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-357">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b6277-358">Wenn **CurrentReading** zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="b6277-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="b6277-359">Wenn **CurrentReading** zwischen **lowertransioldnoncritical** und **lowerstammoldcritical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="b6277-359">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="b6277-360">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-360">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-361">**Maxlesbar**</span><span class="sxs-lookup"><span data-stu-id="b6277-361">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-362">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-362">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-364">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,9 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-365">Der größte Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6277-365">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="b6277-366">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-367">**Minlesbar**</span><span class="sxs-lookup"><span data-stu-id="b6277-367">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-368">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-370">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-371">Der kleinste Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6277-371">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="b6277-372">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="b6277-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-376">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b6277-376">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-377">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-377">Label by which the object is known.</span></span> <span data-ttu-id="b6277-378">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b6277-379">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-380">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="b6277-380">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-381">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-381">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-383">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-384">Normaler oder erwarteter Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="b6277-384">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="b6277-385">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-385">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-386">**Normal Max**</span><span class="sxs-lookup"><span data-stu-id="b6277-386">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-387">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-389">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-390">Normaler oder erwarteter Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="b6277-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="b6277-391">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-392">**Normal Minuten**</span><span class="sxs-lookup"><span data-stu-id="b6277-392">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-393">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-395">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-396">Leitfaden für den Benutzer, der dem normalen Minimal Bereich des numerischen Sensors entspricht.</span><span class="sxs-lookup"><span data-stu-id="b6277-396">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="b6277-397">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-398">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b6277-398">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-399">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-401">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b6277-401">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-402">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b6277-402">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b6277-403">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b6277-404">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b6277-404">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b6277-405">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="b6277-405">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-406">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b6277-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b6277-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6277-408">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b6277-408">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b6277-409">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-409">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6277-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b6277-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b6277-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="b6277-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b6277-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="b6277-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b6277-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b6277-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-414">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b6277-414">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b6277-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="b6277-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-416">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="b6277-416">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b6277-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="b6277-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-418">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6277-418">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b6277-419">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-419">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b6277-420">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b6277-420">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b6277-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="b6277-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-422">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b6277-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="b6277-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b6277-424">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="b6277-424">Timed Power-On Supported</span></span>

<span data-ttu-id="b6277-425">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-425">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b6277-426">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="b6277-426">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-427">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b6277-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6277-429">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="b6277-429">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b6277-430">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-430">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b6277-431">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-432">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="b6277-432">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-433">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6277-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-435">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,17 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Millisekunden ")</span><span class="sxs-lookup"><span data-stu-id="b6277-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-436">Die Fähigkeit des Sensors, Unterschiede in der gemessenen Eigenschaft aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="b6277-436">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="b6277-437">Dieser Wert kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-437">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b6277-438">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-438">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-439">**Status**</span><span class="sxs-lookup"><span data-stu-id="b6277-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-440">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-442">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b6277-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-443">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b6277-443">Current status of the object.</span></span> <span data-ttu-id="b6277-444">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-444">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b6277-445">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="b6277-445">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b6277-446">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="b6277-446">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b6277-447">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-447">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b6277-448">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="b6277-448">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b6277-449">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-449">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b6277-450">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="b6277-450">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b6277-451">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b6277-451">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b6277-452">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="b6277-452">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b6277-453">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="b6277-453">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6277-454">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b6277-454">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b6277-455">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b6277-455">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b6277-456">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="b6277-456">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b6277-457">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="b6277-457">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b6277-458">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="b6277-458">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b6277-459">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="b6277-459">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b6277-460">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="b6277-460">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b6277-461">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="b6277-461">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b6277-462">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="b6277-462">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b6277-463">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b6277-463">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-464">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b6277-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-466">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b6277-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-467">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b6277-467">State of the logical device.</span></span> <span data-ttu-id="b6277-468">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6277-468">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b6277-469">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b6277-470">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b6277-470">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6277-471">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b6277-471">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b6277-472">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="b6277-472">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b6277-473">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="b6277-473">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b6277-474">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="b6277-474">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b6277-475">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="b6277-475">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-476">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-478">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b6277-478">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b6277-479">Der Wert für die Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="b6277-479">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b6277-480">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-481">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="b6277-481">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-482">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6277-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-483">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-484">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b6277-484">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b6277-485">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="b6277-485">Name of the scoping system.</span></span>

<span data-ttu-id="b6277-486">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-486">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-487">**Toleranz**</span><span class="sxs-lookup"><span data-stu-id="b6277-487">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-488">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-488">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-489">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-490">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,18 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-490">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-491">Toleranz des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b6277-491">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="b6277-492">Toleranz wird zusammen mit Auflösung und Genauigkeit verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b6277-492">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="b6277-493">Die Toleranz kann abhängig davon variieren, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="b6277-493">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="b6277-494">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-494">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-495">**Upperder oldcritical**</span><span class="sxs-lookup"><span data-stu-id="b6277-495">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-496">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-496">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-497">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-498">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,14 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-499">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-499">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b6277-500">Wenn **CurrentReading** zwischen **Upper-oldcritical** und **upperanoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="b6277-500">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="b6277-501">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-501">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-502">**Upper-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="b6277-502">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-503">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-503">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-505">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,16 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-506">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-506">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b6277-507">Wenn **CurrentReading** oberhalb von **Upper-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="b6277-507">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="b6277-508">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-508">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6277-509">**Upper-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="b6277-509">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6277-510">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6277-510">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6277-511">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6277-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6277-512">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,12 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="b6277-512">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="b6277-513">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b6277-513">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="b6277-514">Wenn **CurrentReading** zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="b6277-514">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="b6277-515">Wenn **CurrentReading** zwischen **uppertransioldnoncritical** und **upperandincritical Critical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="b6277-515">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="b6277-516">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b6277-516">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6277-517">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6277-517">Remarks</span></span>

<span data-ttu-id="b6277-518">Die **Win32 \_ currentprobe** -Klasse wird von [**CIM \_ CurrentSensor**](cim-currentsensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b6277-518">The **Win32\_CurrentProbe** class is derived from [**CIM\_CurrentSensor**](cim-currentsensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6277-519">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6277-519">Requirements</span></span>



| <span data-ttu-id="b6277-520">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6277-520">Requirement</span></span> | <span data-ttu-id="b6277-521">Wert</span><span class="sxs-lookup"><span data-stu-id="b6277-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6277-522">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6277-522">Minimum supported client</span></span><br/> | <span data-ttu-id="b6277-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6277-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6277-524">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6277-524">Minimum supported server</span></span><br/> | <span data-ttu-id="b6277-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6277-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6277-526">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6277-526">Namespace</span></span><br/>                | <span data-ttu-id="b6277-527">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b6277-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6277-528">MOF</span><span class="sxs-lookup"><span data-stu-id="b6277-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6277-529"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b6277-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6277-530">DLL</span><span class="sxs-lookup"><span data-stu-id="b6277-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6277-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6277-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6277-532">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6277-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6277-533">**CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="b6277-533">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dt>

[<span data-ttu-id="b6277-534">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="b6277-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

