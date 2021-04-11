---
description: Die \_ WMI-Klasse "Win32 voltageprobe" stellt die Eigenschaften eines Spannungs Sensors (Electronic Voltmeter) dar.
ms.assetid: ca27c1df-fb38-412d-b77c-d9ccf7941c66
ms.tgt_platform: multiple
title: Win32_VoltageProbe-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VoltageProbe
- Win32_VoltageProbe.Reset
- Win32_VoltageProbe.SetPowerState
- Win32_VoltageProbe.Accuracy
- Win32_VoltageProbe.Availability
- Win32_VoltageProbe.Caption
- Win32_VoltageProbe.ConfigManagerErrorCode
- Win32_VoltageProbe.ConfigManagerUserConfig
- Win32_VoltageProbe.CreationClassName
- Win32_VoltageProbe.CurrentReading
- Win32_VoltageProbe.Description
- Win32_VoltageProbe.DeviceID
- Win32_VoltageProbe.ErrorCleared
- Win32_VoltageProbe.ErrorDescription
- Win32_VoltageProbe.InstallDate
- Win32_VoltageProbe.IsLinear
- Win32_VoltageProbe.LastErrorCode
- Win32_VoltageProbe.LowerThresholdCritical
- Win32_VoltageProbe.LowerThresholdFatal
- Win32_VoltageProbe.LowerThresholdNonCritical
- Win32_VoltageProbe.MaxReadable
- Win32_VoltageProbe.MinReadable
- Win32_VoltageProbe.Name
- Win32_VoltageProbe.NominalReading
- Win32_VoltageProbe.NormalMax
- Win32_VoltageProbe.NormalMin
- Win32_VoltageProbe.PNPDeviceID
- Win32_VoltageProbe.PowerManagementCapabilities
- Win32_VoltageProbe.PowerManagementSupported
- Win32_VoltageProbe.Resolution
- Win32_VoltageProbe.Status
- Win32_VoltageProbe.StatusInfo
- Win32_VoltageProbe.SystemCreationClassName
- Win32_VoltageProbe.SystemName
- Win32_VoltageProbe.Tolerance
- Win32_VoltageProbe.UpperThresholdCritical
- Win32_VoltageProbe.UpperThresholdFatal
- Win32_VoltageProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: acb5fe56706ed55098443ad9667eb980a1fe6d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214047"
---
# <a name="win32_voltageprobe-class"></a><span data-ttu-id="ae6b4-103">Win32- \_ Klasse "voltageprobe"</span><span class="sxs-lookup"><span data-stu-id="ae6b4-103">Win32\_VoltageProbe class</span></span>

<span data-ttu-id="ae6b4-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ voltageprobe** " stellt die Eigenschaften eines Spannungs Sensors (Electronic Voltmeter) dar.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-104">The **Win32\_VoltageProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a voltage sensor (electronic voltmeter).</span></span>

<span data-ttu-id="ae6b4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ae6b4-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6b4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae6b4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB8-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_VoltageProbe : CIM_VoltageSensor
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

## <a name="members"></a><span data-ttu-id="ae6b4-108">Member</span><span class="sxs-lookup"><span data-stu-id="ae6b4-108">Members</span></span>

<span data-ttu-id="ae6b4-109">Die Win32-Klasse " **\_ voltageprobe** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ae6b4-109">The **Win32\_VoltageProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="ae6b4-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="ae6b4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ae6b4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae6b4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ae6b4-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="ae6b4-112">Methods</span></span>

<span data-ttu-id="ae6b4-113">Die Win32-Klasse " **\_ voltageprobe** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-113">The **Win32\_VoltageProbe** class has these methods.</span></span>



| <span data-ttu-id="ae6b4-114">Methode</span><span class="sxs-lookup"><span data-stu-id="ae6b4-114">Method</span></span>            | <span data-ttu-id="ae6b4-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae6b4-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6b4-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-116">**Reset**</span></span>         | <span data-ttu-id="ae6b4-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-117">Not implemented.</span></span> <span data-ttu-id="ae6b4-118">Informationen zur Implementierung dieser Methode finden Sie in der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ VoltageSensor**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="ae6b4-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/>                 |
| <span data-ttu-id="ae6b4-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-119">**SetPowerState**</span></span> | <span data-ttu-id="ae6b4-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-120">Not implemented.</span></span> <span data-ttu-id="ae6b4-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM- \_ Temperatursensor**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="ae6b4-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ae6b4-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae6b4-122">Properties</span></span>

<span data-ttu-id="ae6b4-123">Die Win32-Klasse " **\_ voltageprobe** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-123">The **Win32\_VoltageProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae6b4-124">**Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-125">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-127">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-128">Genauigkeit des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="ae6b4-129">Der Genauigkeits Wert wird als Plus-oder minus Hundertstel eines Prozentsatzes aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-129">The accuracy value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="ae6b4-130">Die Genauigkeit wird zusammen mit der Auflösung und Toleranz verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="ae6b4-131">Die Genauigkeit kann variieren und hängt davon ab, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-131">The accuracy may vary and depends on whether or not the device is linear in its dynamic range.</span></span>

<span data-ttu-id="ae6b4-132">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-133">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-136">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-137">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-137">Availability and status of the device.</span></span>

<span data-ttu-id="ae6b4-138">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae6b4-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae6b4-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ae6b4-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ae6b4-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ae6b4-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ae6b4-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ae6b4-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ae6b4-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ae6b4-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ae6b4-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="ae6b4-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ae6b4-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ae6b4-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ae6b4-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-152">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ae6b4-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-154">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ae6b4-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-156">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-156">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ae6b4-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ae6b4-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-159">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ae6b4-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-161">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ae6b4-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-163">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ae6b4-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-165">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ae6b4-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="ae6b4-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-167">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae6b4-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-171">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-171">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-172">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-172">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="ae6b4-173">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-174">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-175">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-177">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-177">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-178">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ae6b4-179">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ae6b4-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ae6b4-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-182">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ae6b4-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ae6b4-184">(1)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-185">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ae6b4-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ae6b4-187">(2)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ae6b4-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ae6b4-189">(3)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-190">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ae6b4-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ae6b4-192">(4)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-193">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-193">Device is not working properly.</span></span> <span data-ttu-id="ae6b4-194">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ae6b4-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ae6b4-196">(5)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-197">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ae6b4-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ae6b4-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-200">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ae6b4-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ae6b4-202">(7)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ae6b4-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ae6b4-204">(8)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-205">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ae6b4-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ae6b4-207">(9)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-208">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-208">Device is not working properly.</span></span> <span data-ttu-id="ae6b4-209">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ae6b4-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ae6b4-211">(10)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-212">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ae6b4-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ae6b4-214">(11)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-215">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ae6b4-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ae6b4-217">(12)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-218">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ae6b4-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ae6b4-220">(13)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-221">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ae6b4-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ae6b4-223">(14)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-224">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ae6b4-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ae6b4-226">(15)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-227">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ae6b4-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ae6b4-229">(16)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-230">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ae6b4-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ae6b4-232">(17)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-233">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ae6b4-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ae6b4-235">(18)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-236">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ae6b4-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ae6b4-238">(19)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ae6b4-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ae6b4-240">(20)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-241">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ae6b4-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ae6b4-243">(21)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-244">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-244">System failure.</span></span> <span data-ttu-id="ae6b4-245">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ae6b4-246">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ae6b4-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ae6b4-248">(22)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-249">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ae6b4-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ae6b4-251">(23)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-252">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-252">System failure.</span></span> <span data-ttu-id="ae6b4-253">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ae6b4-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ae6b4-255">(24)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-256">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ae6b4-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ae6b4-258">(25)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-259">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ae6b4-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ae6b4-261">(26)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-262">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ae6b4-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ae6b4-264">(27)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-265">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ae6b4-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ae6b4-267">(28)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-268">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ae6b4-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ae6b4-270">(29)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-271">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-271">Device is disabled.</span></span> <span data-ttu-id="ae6b4-272">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ae6b4-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ae6b4-274">(30)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-275">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ae6b4-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ae6b4-277">31,5</span><span class="sxs-lookup"><span data-stu-id="ae6b4-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-278">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-278">Device is not working properly.</span></span> <span data-ttu-id="ae6b4-279">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae6b4-280">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-281">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ae6b4-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-283">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-283">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-284">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ae6b4-285">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-286">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-287">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-289">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-289">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-290">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ae6b4-291">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-291">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ae6b4-292">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-293">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-293">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-294">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-294">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-296">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,5 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-297">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-297">Current value indicated by the sensor.</span></span>

<span data-ttu-id="ae6b4-298">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-298">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-299">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-302">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-302">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-303">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-303">Description of the object.</span></span>

<span data-ttu-id="ae6b4-304">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-308">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-308">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-309">Eindeutiger Bezeichner des Spannungstests.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-309">Unique identifier of the voltage probe.</span></span>

<span data-ttu-id="ae6b4-310">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-311">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-312">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ae6b4-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-314">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-314">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="ae6b4-315">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-319">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-319">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="ae6b4-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-322">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-324">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-324">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-325">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-325">Date and time the object is installed.</span></span> <span data-ttu-id="ae6b4-326">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ae6b4-327">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-328">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-328">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-329">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ae6b4-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-331">**True** gibt an, dass der Sensor über den dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-331">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="ae6b4-332">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-332">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-333">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-333">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-334">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-334">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-336">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-336">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ae6b4-337">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-338">**Lowerstammoldcritical**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-338">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-339">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-341">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,13 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-342">Sensor Schwellenwerte geben Sie die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-342">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ae6b4-343">Wenn **CurrentReading** zwischen **lowerstammoldcritical** und **lowerstammoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-343">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="ae6b4-344">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-344">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-345">**Lower-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-345">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-346">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-348">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,15 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-349">Sensor Schwellenwerte geben Sie die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-349">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ae6b4-350">Wenn **CurrentReading** unterhalb von **lowerveroldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-350">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="ae6b4-351">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-352">**Lower-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-352">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-353">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-355">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,11 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-356">Sensor Schwellenwerte geben Sie die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-356">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ae6b4-357">Wenn **CurrentReading** zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-357">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="ae6b4-358">Wenn **CurrentReading** zwischen **lowertransioldnoncritical** und **lowerstammoldcritical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="ae6b4-359">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-359">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-360">**Maxlesbar**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-360">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-361">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-361">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-363">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,9 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-364">Der größte Wert der gemessenen Eigenschaft, die vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-364">Largest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="ae6b4-365">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-366">**Minlesbar**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-366">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-367">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-369">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,10 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-370">Der kleinste Wert der gemessenen Eigenschaft, die vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-370">Smallest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="ae6b4-371">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-372">**Name**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-375">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-375">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-376">Bezeichnung für ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-376">Label for an object.</span></span> <span data-ttu-id="ae6b4-377">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-377">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="ae6b4-378">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-379">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-379">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-380">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-380">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-382">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,6 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-383">Normaler oder erwarteter Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-383">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="ae6b4-384">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-384">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-385">**Normal Max**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-385">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-386">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-388">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,7 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-389">Normaler oder erwarteter Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-389">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="ae6b4-390">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-391">**Normal Minuten**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-391">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-392">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-394">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,8 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-395">Leitfaden für den Benutzer, um den normalen Minimal Bereich für den numerischen Sensor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-395">Guidance for the user to indicate the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="ae6b4-396">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-397">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-397">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-398">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-400">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-400">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-401">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-401">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="ae6b4-402">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ae6b4-403">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ae6b4-403">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-404">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-404">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-405">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ae6b4-405">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-407">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-407">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ae6b4-408">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-408">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae6b4-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ae6b4-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ae6b4-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ae6b4-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-413">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-413">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ae6b4-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-415">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-415">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ae6b4-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-417">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-417">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ae6b4-418">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-418">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ae6b4-419">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ae6b4-419">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ae6b4-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-421">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-421">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ae6b4-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ae6b4-423">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae6b4-424">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-424">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-425">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ae6b4-425">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-427">**True** gibt an, dass das Gerät Energie gesteuert werden kann. Dies bedeutet, dass es in den Unterbrechungs Modus versetzt werden kann usw.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-427">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="ae6b4-428">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, aber Sie gibt an, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-428">The property does not indicate that power management features are currently enabled, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="ae6b4-429">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-429">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-430">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-430">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-431">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-433">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,17 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Zehntel Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-433">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-434">Die Fähigkeit des Sensors, Unterschiede in der gemessenen Eigenschaft aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-434">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="ae6b4-435">Dieser Wert kann variieren und hängt davon ab, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-435">This value may vary and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="ae6b4-436">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-436">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-437">**Status**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-437">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-438">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-438">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-440">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-440">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-441">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-441">Current status of the object.</span></span> <span data-ttu-id="ae6b4-442">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-442">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ae6b4-443">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="ae6b4-443">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ae6b4-444">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="ae6b4-444">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ae6b4-445">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-445">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ae6b4-446">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-446">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ae6b4-447">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ae6b4-448">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ae6b4-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ae6b4-449">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ae6b4-450">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ae6b4-451">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae6b4-452">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ae6b4-453">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ae6b4-454">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ae6b4-455">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ae6b4-456">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ae6b4-457">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ae6b4-458">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ae6b4-459">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ae6b4-460">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae6b4-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-462">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-463">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-464">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-464">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-465">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-465">State of the logical device.</span></span> <span data-ttu-id="ae6b4-466">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ae6b4-467">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae6b4-468">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae6b4-469">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ae6b4-470">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ae6b4-471">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ae6b4-472">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae6b4-473">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-476">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-476">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-477">Der Wert für die Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-477">Value for the **CreationClassName** property of the scoping computer.</span></span>

<span data-ttu-id="ae6b4-478">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-479">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-480">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-482">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-482">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-483">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-483">Name of the scoping system.</span></span>

<span data-ttu-id="ae6b4-484">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-485">**Toleranz**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-485">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-486">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-486">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-488">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,18 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-489">Toleranz des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-489">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="ae6b4-490">Toleranz wird zusammen mit Auflösung und Genauigkeit verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-490">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="ae6b4-491">Die Toleranz kann variieren und hängt davon ab, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-491">Tolerance may vary, and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="ae6b4-492">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-492">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-493">**Upperder oldcritical**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-493">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-494">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-494">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-496">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,14 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-497">Sensor Schwellenwerte geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-497">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ae6b4-498">Wenn **CurrentReading** zwischen **Upper-oldcritical** und **upperanoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-498">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="ae6b4-499">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-500">**Upper-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-500">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-501">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-502">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-503">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,16 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-504">Sensor Schwellenwerte geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-504">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ae6b4-505">Wenn **CurrentReading** oberhalb von **Upper-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-505">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="ae6b4-506">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6b4-507">**Upper-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-507">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6b4-508">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-509">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae6b4-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6b4-510">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Spannungstest \| 001,12 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="ae6b4-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ae6b4-511">Sensor Schwellenwerte geben die Bereiche (Mindest-und Höchstwerte) an, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-511">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="ae6b4-512">Wenn **CurrentReading** zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-512">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="ae6b4-513">Wenn **CurrentReading** zwischen **uppertransioldnoncritical** und **upperandincritical Critical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-513">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="ae6b4-514">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-514">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae6b4-515">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae6b4-515">Remarks</span></span>

<span data-ttu-id="ae6b4-516">Die Win32-Klasse " **\_ voltageprobe** " ist von [**CIM \_ VoltageSensor**](cim-voltagesensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ae6b4-516">The **Win32\_VoltageProbe** class is derived from [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6b4-517">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae6b4-517">Requirements</span></span>



| <span data-ttu-id="ae6b4-518">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae6b4-518">Requirement</span></span> | <span data-ttu-id="ae6b4-519">Wert</span><span class="sxs-lookup"><span data-stu-id="ae6b4-519">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6b4-520">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-520">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6b4-521">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae6b4-521">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae6b4-522">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae6b4-522">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6b4-523">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae6b4-523">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae6b4-524">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae6b4-524">Namespace</span></span><br/>                | <span data-ttu-id="ae6b4-525">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ae6b4-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae6b4-526">MOF</span><span class="sxs-lookup"><span data-stu-id="ae6b4-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae6b4-527"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ae6b4-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae6b4-528">DLL</span><span class="sxs-lookup"><span data-stu-id="ae6b4-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae6b4-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6b4-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae6b4-530">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae6b4-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6b4-531">**CIM- \_ Temperatursensor**</span><span class="sxs-lookup"><span data-stu-id="ae6b4-531">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="ae6b4-532">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="ae6b4-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
