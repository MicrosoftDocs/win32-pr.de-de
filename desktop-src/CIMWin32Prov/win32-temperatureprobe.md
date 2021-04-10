---
description: Der Win32- \_ temperaturprobe-&\# 32; Die WMI-Klasse stellt die Eigenschaften eines Temperatursensors (elektronisches Thermometer) dar.
ms.assetid: 63ba1ae2-6abc-4d86-a7f6-f02536ebd8ac
ms.tgt_platform: multiple
title: Win32_TemperatureProbe-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TemperatureProbe
- Win32_TemperatureProbe.Reset
- Win32_TemperatureProbe.SetPowerState
- Win32_TemperatureProbe.Accuracy
- Win32_TemperatureProbe.Availability
- Win32_TemperatureProbe.Caption
- Win32_TemperatureProbe.ConfigManagerErrorCode
- Win32_TemperatureProbe.ConfigManagerUserConfig
- Win32_TemperatureProbe.CreationClassName
- Win32_TemperatureProbe.CurrentReading
- Win32_TemperatureProbe.Description
- Win32_TemperatureProbe.DeviceID
- Win32_TemperatureProbe.ErrorCleared
- Win32_TemperatureProbe.ErrorDescription
- Win32_TemperatureProbe.InstallDate
- Win32_TemperatureProbe.IsLinear
- Win32_TemperatureProbe.LastErrorCode
- Win32_TemperatureProbe.LowerThresholdCritical
- Win32_TemperatureProbe.LowerThresholdFatal
- Win32_TemperatureProbe.LowerThresholdNonCritical
- Win32_TemperatureProbe.MaxReadable
- Win32_TemperatureProbe.MinReadable
- Win32_TemperatureProbe.Name
- Win32_TemperatureProbe.NominalReading
- Win32_TemperatureProbe.NormalMax
- Win32_TemperatureProbe.NormalMin
- Win32_TemperatureProbe.PNPDeviceID
- Win32_TemperatureProbe.PowerManagementCapabilities
- Win32_TemperatureProbe.PowerManagementSupported
- Win32_TemperatureProbe.Resolution
- Win32_TemperatureProbe.Status
- Win32_TemperatureProbe.StatusInfo
- Win32_TemperatureProbe.SystemCreationClassName
- Win32_TemperatureProbe.SystemName
- Win32_TemperatureProbe.Tolerance
- Win32_TemperatureProbe.UpperThresholdCritical
- Win32_TemperatureProbe.UpperThresholdFatal
- Win32_TemperatureProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6de4ed6334747e8313098075bc916a1975f520c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861155"
---
# <a name="win32_temperatureprobe-class"></a><span data-ttu-id="08088-103">Win32 \_ temperatureprobe-Klasse</span><span class="sxs-lookup"><span data-stu-id="08088-103">Win32\_TemperatureProbe class</span></span>

<span data-ttu-id="08088-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32 \_ -Temperatur** Test stellt die Eigenschaften eines Temperatursensors (elektronisches Thermometer) dar.</span><span class="sxs-lookup"><span data-stu-id="08088-104">The **Win32\_TemperatureProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a temperature sensor (electronic thermometer).</span></span>

<span data-ttu-id="08088-105">Die meisten Informationen, die die WMI-Klasse " **Win32 \_ temperatureprobe** " bereitstellt, stammen aus SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="08088-105">Most of the information that the **Win32\_TemperatureProbe** WMI class provides comes from SMBIOS.</span></span> <span data-ttu-id="08088-106">Echt Zeit Messwerte für die **CurrentReading** -Eigenschaft können nicht aus SMBIOS-Tabellen extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="08088-106">Real-time readings for the **CurrentReading** property cannot be extracted from SMBIOS tables.</span></span> <span data-ttu-id="08088-107">Aus diesem Grund füllen die aktuellen Implementierungen von WMI nicht die **CurrentReading** -Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="08088-107">For this reason, current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="08088-108">Die Anwesenheit der **CurrentReading** -Eigenschaft ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="08088-108">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="08088-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08088-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="08088-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="08088-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08088-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="08088-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABB-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_TemperatureProbe : CIM_TemperatureSensor
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

## <a name="members"></a><span data-ttu-id="08088-112">Member</span><span class="sxs-lookup"><span data-stu-id="08088-112">Members</span></span>

<span data-ttu-id="08088-113">Die **Win32 \_ temperatureprobe** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="08088-113">The **Win32\_TemperatureProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="08088-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="08088-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="08088-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08088-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08088-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="08088-116">Methods</span></span>

<span data-ttu-id="08088-117">Die **Win32 \_ temperatureprobe** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="08088-117">The **Win32\_TemperatureProbe** class has these methods.</span></span>



| <span data-ttu-id="08088-118">Methode</span><span class="sxs-lookup"><span data-stu-id="08088-118">Method</span></span>            | <span data-ttu-id="08088-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08088-119">Description</span></span>                                                                                                                                                                                                                     |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08088-120">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="08088-120">**Reset**</span></span>         | <span data-ttu-id="08088-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="08088-121">Not implemented.</span></span> <span data-ttu-id="08088-122">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-temperaturesensor.md) -Methode in [**CIM \_ temperaturesensor**](cim-temperaturesensor.md) .</span><span class="sxs-lookup"><span data-stu-id="08088-122">To implement this method, see the [**Reset**](reset-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="08088-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="08088-123">**SetPowerState**</span></span> | <span data-ttu-id="08088-124">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="08088-124">Not implemented.</span></span> <span data-ttu-id="08088-125">Informationen zur Implementierung dieser Methode finden Sie in der [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) -Methode unter [**CIM \_ temperaturesensor**](cim-temperaturesensor.md) .</span><span class="sxs-lookup"><span data-stu-id="08088-125">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08088-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08088-126">Properties</span></span>

<span data-ttu-id="08088-127">Die **Win32 \_ temperatureprobe** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08088-127">The **Win32\_TemperatureProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08088-128">**Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="08088-128">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-131">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="08088-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="08088-132">Genauigkeit des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="08088-132">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="08088-133">Der Wert wird als Plus-oder minus Hundertstel eines Prozentsatzes aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="08088-133">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="08088-134">Genauigkeit, Auflösung und Toleranz werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="08088-134">Accuracy, resolution, and tolerance are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="08088-135">Die Genauigkeit kann variieren und hängt davon ab, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="08088-135">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="08088-136">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-136">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-137">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="08088-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-138">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08088-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08088-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-140">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="08088-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="08088-141">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="08088-141">Availability and status of the device.</span></span>

<span data-ttu-id="08088-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="08088-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="08088-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08088-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="08088-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="08088-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="08088-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="08088-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="08088-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="08088-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="08088-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="08088-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="08088-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="08088-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="08088-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="08088-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="08088-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="08088-151">Offline</span><span class="sxs-lookup"><span data-stu-id="08088-151">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="08088-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="08088-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="08088-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="08088-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="08088-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="08088-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="08088-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="08088-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="08088-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="08088-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="08088-157">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="08088-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="08088-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="08088-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="08088-159">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="08088-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="08088-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="08088-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="08088-161">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="08088-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="08088-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="08088-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="08088-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="08088-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="08088-164">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="08088-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="08088-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="08088-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="08088-166">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="08088-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="08088-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="08088-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="08088-168">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="08088-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="08088-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="08088-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="08088-170">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="08088-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="08088-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="08088-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="08088-172">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="08088-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08088-173">**Caption**</span><span class="sxs-lookup"><span data-stu-id="08088-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-176">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="08088-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="08088-177">Kurze Beschreibung eines Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="08088-177">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="08088-178">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-179">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="08088-179">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-180">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08088-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-182">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="08088-182">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="08088-183">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="08088-183">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="08088-184">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-184">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="08088-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="08088-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="08088-186"> (0)</span><span class="sxs-lookup"><span data-stu-id="08088-186">(0)</span></span>


</dt> <dd>

<span data-ttu-id="08088-187">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08088-187">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="08088-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="08088-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="08088-189">(1)</span><span class="sxs-lookup"><span data-stu-id="08088-189">(1)</span></span>


</dt> <dd>

<span data-ttu-id="08088-190">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="08088-190">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="08088-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="08088-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="08088-192">(2)</span><span class="sxs-lookup"><span data-stu-id="08088-192">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="08088-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="08088-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="08088-194">(3)</span><span class="sxs-lookup"><span data-stu-id="08088-194">(3)</span></span>


</dt> <dd>

<span data-ttu-id="08088-195">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="08088-195">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="08088-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="08088-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="08088-197">(4)</span><span class="sxs-lookup"><span data-stu-id="08088-197">(4)</span></span>


</dt> <dd>

<span data-ttu-id="08088-198">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08088-198">Device is not working properly.</span></span> <span data-ttu-id="08088-199">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="08088-199">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="08088-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="08088-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="08088-201">(5)</span><span class="sxs-lookup"><span data-stu-id="08088-201">(5)</span></span>


</dt> <dd>

<span data-ttu-id="08088-202">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="08088-202">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="08088-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="08088-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="08088-204"> (6)</span><span class="sxs-lookup"><span data-stu-id="08088-204">(6)</span></span>


</dt> <dd>

<span data-ttu-id="08088-205">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="08088-205">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="08088-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="08088-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="08088-207">(7)</span><span class="sxs-lookup"><span data-stu-id="08088-207">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="08088-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="08088-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="08088-209">(8)</span><span class="sxs-lookup"><span data-stu-id="08088-209">(8)</span></span>


</dt> <dd>

<span data-ttu-id="08088-210">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="08088-210">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="08088-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="08088-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="08088-212">(9)</span><span class="sxs-lookup"><span data-stu-id="08088-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="08088-213">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08088-213">Device is not working properly.</span></span> <span data-ttu-id="08088-214">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="08088-214">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="08088-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="08088-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="08088-216">(10)</span><span class="sxs-lookup"><span data-stu-id="08088-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="08088-217">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="08088-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="08088-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="08088-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="08088-219">(11)</span><span class="sxs-lookup"><span data-stu-id="08088-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="08088-220">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="08088-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="08088-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="08088-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="08088-222">(12)</span><span class="sxs-lookup"><span data-stu-id="08088-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="08088-223">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="08088-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="08088-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="08088-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="08088-225">(13)</span><span class="sxs-lookup"><span data-stu-id="08088-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="08088-226">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="08088-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="08088-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="08088-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="08088-228">(14)</span><span class="sxs-lookup"><span data-stu-id="08088-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="08088-229">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="08088-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="08088-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="08088-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="08088-231">(15)</span><span class="sxs-lookup"><span data-stu-id="08088-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="08088-232">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08088-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="08088-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="08088-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="08088-234">(16)</span><span class="sxs-lookup"><span data-stu-id="08088-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="08088-235">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08088-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="08088-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="08088-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="08088-237">(17)</span><span class="sxs-lookup"><span data-stu-id="08088-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="08088-238">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="08088-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="08088-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="08088-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="08088-240">(18)</span><span class="sxs-lookup"><span data-stu-id="08088-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="08088-241">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="08088-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="08088-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="08088-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="08088-243">(19)</span><span class="sxs-lookup"><span data-stu-id="08088-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="08088-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="08088-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="08088-245">(20)</span><span class="sxs-lookup"><span data-stu-id="08088-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="08088-246">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="08088-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="08088-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="08088-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="08088-248">(21)</span><span class="sxs-lookup"><span data-stu-id="08088-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="08088-249">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="08088-249">System failure.</span></span> <span data-ttu-id="08088-250">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="08088-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="08088-251">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="08088-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="08088-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="08088-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="08088-253">(22)</span><span class="sxs-lookup"><span data-stu-id="08088-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="08088-254">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="08088-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="08088-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="08088-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="08088-256">(23)</span><span class="sxs-lookup"><span data-stu-id="08088-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="08088-257">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="08088-257">System failure.</span></span> <span data-ttu-id="08088-258">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="08088-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="08088-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="08088-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="08088-260">(24)</span><span class="sxs-lookup"><span data-stu-id="08088-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="08088-261">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="08088-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="08088-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="08088-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="08088-263">(25)</span><span class="sxs-lookup"><span data-stu-id="08088-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="08088-264">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="08088-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="08088-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="08088-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="08088-266">(26)</span><span class="sxs-lookup"><span data-stu-id="08088-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="08088-267">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="08088-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="08088-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="08088-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="08088-269">(27)</span><span class="sxs-lookup"><span data-stu-id="08088-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="08088-270">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="08088-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="08088-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="08088-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="08088-272">(28)</span><span class="sxs-lookup"><span data-stu-id="08088-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="08088-273">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="08088-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="08088-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="08088-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="08088-275">(29)</span><span class="sxs-lookup"><span data-stu-id="08088-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="08088-276">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="08088-276">Device is disabled.</span></span> <span data-ttu-id="08088-277">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="08088-277">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="08088-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="08088-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="08088-279">(30)</span><span class="sxs-lookup"><span data-stu-id="08088-279">(30)</span></span>


</dt> <dd>

<span data-ttu-id="08088-280">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08088-280">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="08088-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="08088-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="08088-282">31,5</span><span class="sxs-lookup"><span data-stu-id="08088-282">(31)</span></span>


</dt> <dd>

<span data-ttu-id="08088-283">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="08088-283">Device is not working properly.</span></span> <span data-ttu-id="08088-284">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="08088-284">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08088-285">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="08088-285">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-286">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="08088-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08088-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-288">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="08088-288">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="08088-289">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="08088-289">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="08088-290">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-291">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="08088-291">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-294">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="08088-294">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="08088-295">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08088-295">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="08088-296">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften einer Klasse verwendet wird, können alle Instanzen der Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="08088-296">When used with the other key properties of a class, this property allows all instances of the class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="08088-297">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-298">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="08088-298">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-299">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-299">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-301">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,5 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-302">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08088-302">Current value indicated by the sensor.</span></span>

<span data-ttu-id="08088-303">Die **CurrentReading** -Eigenschaft wird von den aktuellen Implementierungen von WMI nicht aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="08088-303">Current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="08088-304">Die Anwesenheit der **CurrentReading** -Eigenschaft ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="08088-304">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="08088-305">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-306">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08088-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-309">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="08088-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="08088-310">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="08088-310">Description of the object.</span></span>

<span data-ttu-id="08088-311">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="08088-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-315">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="08088-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="08088-316">Eindeutiger Bezeichner des aktuellen Tests.</span><span class="sxs-lookup"><span data-stu-id="08088-316">Unique identifier of the current probe.</span></span>

<span data-ttu-id="08088-317">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-318">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="08088-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-319">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="08088-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08088-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08088-321">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="08088-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="08088-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="08088-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08088-326">Weitere Informationen zu dem Fehler, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen zu den Maßnahmen, die Sie ausführen können, finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="08088-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that you can take.</span></span>

<span data-ttu-id="08088-327">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="08088-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-329">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="08088-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08088-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-331">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="08088-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="08088-332">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="08088-332">Date and time the object is installed.</span></span> <span data-ttu-id="08088-333">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="08088-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="08088-334">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-335">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="08088-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-336">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="08088-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08088-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08088-338">**True** gibt an, dass der Sensor über den dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="08088-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="08088-339">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="08088-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-341">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08088-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08088-343">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="08088-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="08088-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-345">**Lowerstammoldcritical**</span><span class="sxs-lookup"><span data-stu-id="08088-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-346">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-348">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,13 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-349">Sensor Schwellenwert, um die Bereiche (minimal-und Maximalwerte) anzugeben, die die Sensor Betriebssysteme identifizieren, die normale, nicht kritische, kritische oder schwerwiegende Bedingungen sein können.</span><span class="sxs-lookup"><span data-stu-id="08088-349">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="08088-350">Wenn **CurrentReading** zwischen **lowerstammoldcritical** und **lowerstammoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="08088-350">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="08088-351">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-352">**Lower-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="08088-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-353">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-355">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,15 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-356">Sensor Schwellenwert, um die Bereiche (minimal-und Maximalwerte) anzugeben, die die Sensor Betriebssysteme identifizieren, die normale, nicht kritische, kritische oder schwerwiegende Bedingungen sein können.</span><span class="sxs-lookup"><span data-stu-id="08088-356">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="08088-357">Wenn **CurrentReading** unterhalb von **lowerveroldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="08088-357">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="08088-358">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-359">**Lower-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="08088-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-360">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-362">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,11 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-363">Sensor Schwellenwert, um die Bereiche (minimal-und Maximalwerte) anzugeben, die die Sensor Betriebssysteme identifizieren, die normale, nicht kritische, kritische oder schwerwiegende Bedingungen sein können.</span><span class="sxs-lookup"><span data-stu-id="08088-363">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="08088-364">Wenn **CurrentReading** zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="08088-364">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="08088-365">Wenn **CurrentReading** zwischen **lowertransioldnoncritical** und **lowerstammoldcritical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="08088-365">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="08088-366">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-367">**Maxlesbar**</span><span class="sxs-lookup"><span data-stu-id="08088-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-368">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-370">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,9 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-371">Der größte Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="08088-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="08088-372">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-373">**Minlesbar**</span><span class="sxs-lookup"><span data-stu-id="08088-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-374">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-376">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,10 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-377">Der kleinste Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="08088-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="08088-378">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-379">**Name**</span><span class="sxs-lookup"><span data-stu-id="08088-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-380">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-382">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="08088-382">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="08088-383">Die Bezeichnung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08088-383">Label for the object.</span></span> <span data-ttu-id="08088-384">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08088-384">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="08088-385">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="08088-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-387">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-389">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,6 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-390">Normaler oder erwarteter Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="08088-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="08088-391">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-392">**Normal Max**</span><span class="sxs-lookup"><span data-stu-id="08088-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-393">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-395">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,7 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-396">Normaler oder erwarteter Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="08088-396">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="08088-397">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-398">**Normal Minuten**</span><span class="sxs-lookup"><span data-stu-id="08088-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-399">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-401">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,8 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-402">Leitfaden für den Benutzer, der dem normalen Minimal Bereich des numerischen Sensors entspricht.</span><span class="sxs-lookup"><span data-stu-id="08088-402">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="08088-403">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="08088-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-405">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-407">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="08088-407">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="08088-408">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="08088-408">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="08088-409">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="08088-409">Example: "\*PNP030b"</span></span>

<span data-ttu-id="08088-410">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-411">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="08088-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-412">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="08088-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08088-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08088-414">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="08088-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="08088-415">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08088-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="08088-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="08088-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="08088-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="08088-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="08088-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="08088-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="08088-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="08088-420">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08088-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="08088-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="08088-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="08088-422">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="08088-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="08088-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="08088-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="08088-424">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08088-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="08088-425">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="08088-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="08088-426">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="08088-426">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="08088-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="08088-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="08088-428">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="08088-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="08088-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="08088-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="08088-430">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="08088-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08088-431">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="08088-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-432">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="08088-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08088-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08088-434">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="08088-434">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="08088-435">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="08088-435">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="08088-436">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-437">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="08088-437">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-438">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08088-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-440">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,17 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Hundertstel Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-441">Die Fähigkeit des Sensors, Unterschiede in der gemessenen Eigenschaft aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="08088-441">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="08088-442">Dieser Wert kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="08088-442">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="08088-443">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-443">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-444">**Status**</span><span class="sxs-lookup"><span data-stu-id="08088-444">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-447">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="08088-447">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="08088-448">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="08088-448">Current status of the object.</span></span> <span data-ttu-id="08088-449">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="08088-449">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="08088-450">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="08088-450">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="08088-451">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="08088-451">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="08088-452">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="08088-452">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="08088-453">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="08088-453">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="08088-454">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="08088-455">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="08088-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="08088-456">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="08088-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="08088-457">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="08088-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="08088-458">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="08088-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08088-459">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="08088-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="08088-460">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="08088-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="08088-461">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="08088-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="08088-462">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="08088-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="08088-463">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="08088-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="08088-464">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="08088-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="08088-465">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="08088-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="08088-466">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="08088-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="08088-467">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="08088-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08088-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="08088-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-469">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08088-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08088-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-471">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="08088-471">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="08088-472">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="08088-472">State of the logical device.</span></span> <span data-ttu-id="08088-473">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08088-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="08088-474">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="08088-475">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="08088-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08088-476">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="08088-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="08088-477">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="08088-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="08088-478">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="08088-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="08088-479">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="08088-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08088-480">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="08088-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-483">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="08088-483">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="08088-484">Der Wert für die Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="08088-484">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="08088-485">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-486">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="08088-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08088-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08088-488">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-489">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="08088-489">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="08088-490">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="08088-490">Name of the scoping system.</span></span>

<span data-ttu-id="08088-491">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-492">**Toleranz**</span><span class="sxs-lookup"><span data-stu-id="08088-492">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-493">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-493">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-494">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-495">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,18 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-495">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-496">Toleranz des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="08088-496">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="08088-497">Toleranz wird zusammen mit Auflösung und Genauigkeit verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="08088-497">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="08088-498">Die Toleranz kann abhängig davon variieren, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="08088-498">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="08088-499">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-500">**Upperder oldcritical**</span><span class="sxs-lookup"><span data-stu-id="08088-500">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-501">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-502">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-503">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,14 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-504">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, die die Betriebsbedingungen des Sensors identifizieren, die normale, nicht kritische, kritische oder schwerwiegende Bedingungen sein können.</span><span class="sxs-lookup"><span data-stu-id="08088-504">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="08088-505">Wenn **CurrentReading** zwischen **Upper-oldcritical** und **upperanoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="08088-505">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="08088-506">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-507">**Upper-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="08088-507">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-508">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-509">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-510">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,16 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-511">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, die die Betriebsbedingungen des Sensors identifizieren, die normale, nicht kritische, kritische oder schwerwiegende Bedingungen sein können.</span><span class="sxs-lookup"><span data-stu-id="08088-511">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="08088-512">Wenn **CurrentReading** oberhalb von **Upper-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="08088-512">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="08088-513">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-513">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="08088-514">**Upper-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="08088-514">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08088-515">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08088-515">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08088-516">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08088-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08088-517">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Temperatur Test \| 001,12 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="08088-517">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="08088-518">Die Schwellenwerte des Sensors geben die Bereiche (Mindest-und Höchstwerte) an, die die Betriebsbedingungen des Sensors identifizieren, die normale, nicht kritische, kritische oder schwerwiegende Bedingungen sein können.</span><span class="sxs-lookup"><span data-stu-id="08088-518">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="08088-519">Wenn **CurrentReading** zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="08088-519">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="08088-520">Wenn **CurrentReading** zwischen **uppertransioldnoncritical** und **upperandincritical Critical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="08088-520">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="08088-521">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="08088-521">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08088-522">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08088-522">Remarks</span></span>

<span data-ttu-id="08088-523">Die **Win32 \_ temperatureprobe** -Klasse wird von [**CIM \_ temperaturesensor**](cim-temperaturesensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="08088-523">The **Win32\_TemperatureProbe** class is derived from [**CIM\_TemperatureSensor**](cim-temperaturesensor.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08088-524">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08088-524">Examples</span></span>

<span data-ttu-id="08088-525">Im folgenden Beispiel werden Temperatur Testdaten für den lokalen Computer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08088-525">The following example returns temperature probe data for the local computer.</span></span>


```VB
strComputer = "."
Set colTempProbe = GetObject("Winmgmts:"_
    & "{impersonationLevel=impersonate}!\\"_ 
    & strComputer & "\root\cimv2")._
    InstancesOf("Win32_TemperatureProbe")
Num = 0
For Each obj In colTempProbe      
    WScript.Echo   obj.Name & VBNewLine _
        & obj.DeviceID & VBNewLine _
        & obj.Status & VBNewLine _
        & obj.Resolution & VBNewLine _
        & obj.Tolerance & VBNewLine _
        & obj.Accuracy 
    Num = Num +1
Next
If Num = 0 Then
    WScript.Echo "No temperature probe data"
End If
```



## <a name="requirements"></a><span data-ttu-id="08088-526">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08088-526">Requirements</span></span>



| <span data-ttu-id="08088-527">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08088-527">Requirement</span></span> | <span data-ttu-id="08088-528">Wert</span><span class="sxs-lookup"><span data-stu-id="08088-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08088-529">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08088-529">Minimum supported client</span></span><br/> | <span data-ttu-id="08088-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08088-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08088-531">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08088-531">Minimum supported server</span></span><br/> | <span data-ttu-id="08088-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08088-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08088-533">Namespace</span><span class="sxs-lookup"><span data-stu-id="08088-533">Namespace</span></span><br/>                | <span data-ttu-id="08088-534">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="08088-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08088-535">MOF</span><span class="sxs-lookup"><span data-stu-id="08088-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08088-536"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="08088-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08088-537">DLL</span><span class="sxs-lookup"><span data-stu-id="08088-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08088-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08088-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08088-539">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08088-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08088-540">**CIM- \_ Temperatursensor**</span><span class="sxs-lookup"><span data-stu-id="08088-540">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="08088-541">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="08088-541">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
