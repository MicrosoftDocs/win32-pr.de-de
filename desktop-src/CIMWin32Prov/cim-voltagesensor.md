---
description: Die CIM- \_ Klasse "VoltageSensor" ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden. Mit Ergänzungen der CIM \_ -Sensor-und CIM- \_ numericsensor-Klassen in Version 2,2 ist es nicht mehr erforderlich.
ms.assetid: a578c7a2-27d5-4bd8-86d7-3962d5091f14
ms.tgt_platform: multiple
title: CIM_VoltageSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VoltageSensor
- CIM_VoltageSensor.Accuracy
- CIM_VoltageSensor.Availability
- CIM_VoltageSensor.Caption
- CIM_VoltageSensor.ConfigManagerErrorCode
- CIM_VoltageSensor.ConfigManagerUserConfig
- CIM_VoltageSensor.CreationClassName
- CIM_VoltageSensor.CurrentReading
- CIM_VoltageSensor.Description
- CIM_VoltageSensor.DeviceID
- CIM_VoltageSensor.ErrorCleared
- CIM_VoltageSensor.ErrorDescription
- CIM_VoltageSensor.InstallDate
- CIM_VoltageSensor.IsLinear
- CIM_VoltageSensor.LastErrorCode
- CIM_VoltageSensor.LowerThresholdCritical
- CIM_VoltageSensor.LowerThresholdFatal
- CIM_VoltageSensor.LowerThresholdNonCritical
- CIM_VoltageSensor.MaxReadable
- CIM_VoltageSensor.MinReadable
- CIM_VoltageSensor.Name
- CIM_VoltageSensor.NominalReading
- CIM_VoltageSensor.NormalMax
- CIM_VoltageSensor.NormalMin
- CIM_VoltageSensor.PNPDeviceID
- CIM_VoltageSensor.PowerManagementCapabilities
- CIM_VoltageSensor.PowerManagementSupported
- CIM_VoltageSensor.Resolution
- CIM_VoltageSensor.Status
- CIM_VoltageSensor.StatusInfo
- CIM_VoltageSensor.SystemCreationClassName
- CIM_VoltageSensor.SystemName
- CIM_VoltageSensor.Tolerance
- CIM_VoltageSensor.UpperThresholdCritical
- CIM_VoltageSensor.UpperThresholdFatal
- CIM_VoltageSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bd0f3d79415254d0af50429c8f1776d2eb451cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344810"
---
# <a name="cim_voltagesensor-class"></a><span data-ttu-id="39720-104">CIM- \_ Klasse "VoltageSensor"</span><span class="sxs-lookup"><span data-stu-id="39720-104">CIM\_VoltageSensor class</span></span>

<span data-ttu-id="39720-105">Die CIM-Klasse " **\_ VoltageSensor** " ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="39720-105">The **CIM\_VoltageSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="39720-106">Mit Ergänzungen der [**CIM- \_ Sensor**](cim-sensor.md) -und [**CIM- \_ numericsensor**](cim-numericsensor.md) -Klassen in Version 2,2 ist es nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39720-106">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="39720-107">Ein Spannungssensor kann definiert werden, indem die **SensorType** -Eigenschaft, die vom [**CIM- \_ Sensor**](cim-sensor.md)geerbt wurde, auf 3 ("Spannung") festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="39720-107">A voltage sensor can be defined by setting the **SensorType** property, inherited from [**CIM\_Sensor**](cim-sensor.md), to 3 ("Voltage").</span></span> <span data-ttu-id="39720-108">Andere Eigenschaften dieser Klasse sind für konstante Werte hart codiert, die Definitionen in der Sensor Hierarchie entsprechen.</span><span class="sxs-lookup"><span data-stu-id="39720-108">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39720-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="39720-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39720-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39720-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39720-111">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39720-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="39720-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="39720-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39720-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="39720-113">Syntax</span></span>

``` syntax
[UUID("{A998F9B4-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VoltageSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="39720-114">Member</span><span class="sxs-lookup"><span data-stu-id="39720-114">Members</span></span>

<span data-ttu-id="39720-115">Die CIM-Klasse " **\_ VoltageSensor** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="39720-115">The **CIM\_VoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="39720-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="39720-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="39720-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39720-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39720-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="39720-118">Methods</span></span>

<span data-ttu-id="39720-119">Die CIM-Klasse " **\_ VoltageSensor** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="39720-119">The **CIM\_VoltageSensor** class has these methods.</span></span>



| <span data-ttu-id="39720-120">Methode</span><span class="sxs-lookup"><span data-stu-id="39720-120">Method</span></span>                                                                   | <span data-ttu-id="39720-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39720-121">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39720-122">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="39720-122">**Reset**</span></span>](reset-method-in-class-cim-voltagesensor.md)                 | <span data-ttu-id="39720-123">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="39720-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="39720-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="39720-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="39720-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="39720-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-voltagesensor.md) | <span data-ttu-id="39720-126">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39720-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="39720-127">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="39720-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="39720-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39720-128">Properties</span></span>

<span data-ttu-id="39720-129">Die CIM-Klasse " **\_ VoltageSensor** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39720-129">The **CIM\_VoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39720-130">**Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="39720-130">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-133">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Genauigkeit"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="39720-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="39720-134">Genauigkeit des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="39720-134">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="39720-135">Der Wert wird als Plus-oder minus Hundertstel eines Prozentsatzes aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39720-135">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="39720-136">Diese Eigenschaft und die **Auflösungs** -und **Toleranz** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="39720-136">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="39720-137">Die Genauigkeit kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="39720-137">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="39720-138">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-138">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-139">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="39720-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39720-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39720-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-142">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="39720-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="39720-143">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="39720-143">Availability and status of the device.</span></span>

<span data-ttu-id="39720-144">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39720-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="39720-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39720-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="39720-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="39720-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="39720-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="39720-148">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="39720-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="39720-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="39720-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="39720-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="39720-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="39720-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="39720-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="39720-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="39720-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="39720-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="39720-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="39720-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="39720-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="39720-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="39720-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="39720-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="39720-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="39720-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="39720-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="39720-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="39720-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="39720-159">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="39720-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="39720-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="39720-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="39720-161">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39720-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="39720-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="39720-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="39720-163">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="39720-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="39720-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="39720-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="39720-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="39720-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="39720-166">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="39720-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="39720-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="39720-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="39720-168">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="39720-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="39720-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="39720-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="39720-170">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="39720-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="39720-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="39720-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="39720-172">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="39720-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="39720-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="39720-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="39720-174">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="39720-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39720-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="39720-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-178">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="39720-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="39720-179">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="39720-179">Short textual description of the object.</span></span>

<span data-ttu-id="39720-180">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-181">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="39720-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39720-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-184">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="39720-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39720-185">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="39720-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="39720-186">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="39720-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="39720-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="39720-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="39720-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="39720-189">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="39720-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="39720-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="39720-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="39720-191">(1)</span><span class="sxs-lookup"><span data-stu-id="39720-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="39720-192">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="39720-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39720-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="39720-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="39720-194">(2)</span><span class="sxs-lookup"><span data-stu-id="39720-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="39720-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="39720-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="39720-196">(3)</span><span class="sxs-lookup"><span data-stu-id="39720-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="39720-197">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="39720-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="39720-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="39720-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="39720-199">(4)</span><span class="sxs-lookup"><span data-stu-id="39720-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="39720-200">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="39720-200">Device is not working properly.</span></span> <span data-ttu-id="39720-201">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="39720-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="39720-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="39720-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="39720-203">(5)</span><span class="sxs-lookup"><span data-stu-id="39720-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="39720-204">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="39720-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="39720-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="39720-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="39720-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="39720-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="39720-207">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="39720-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="39720-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="39720-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="39720-209">(7)</span><span class="sxs-lookup"><span data-stu-id="39720-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="39720-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="39720-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="39720-211">(8)</span><span class="sxs-lookup"><span data-stu-id="39720-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="39720-212">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="39720-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="39720-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="39720-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="39720-214">(9)</span><span class="sxs-lookup"><span data-stu-id="39720-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="39720-215">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="39720-215">Device is not working properly.</span></span> <span data-ttu-id="39720-216">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="39720-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="39720-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="39720-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="39720-218">(10)</span><span class="sxs-lookup"><span data-stu-id="39720-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="39720-219">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="39720-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="39720-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="39720-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="39720-221">(11)</span><span class="sxs-lookup"><span data-stu-id="39720-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="39720-222">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="39720-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="39720-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="39720-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="39720-224">(12)</span><span class="sxs-lookup"><span data-stu-id="39720-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="39720-225">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="39720-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="39720-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="39720-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="39720-227">(13)</span><span class="sxs-lookup"><span data-stu-id="39720-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="39720-228">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="39720-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="39720-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="39720-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="39720-230">(14)</span><span class="sxs-lookup"><span data-stu-id="39720-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="39720-231">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="39720-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="39720-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="39720-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="39720-233">(15)</span><span class="sxs-lookup"><span data-stu-id="39720-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="39720-234">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="39720-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="39720-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="39720-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="39720-236">(16)</span><span class="sxs-lookup"><span data-stu-id="39720-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="39720-237">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39720-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="39720-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="39720-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="39720-239">(17)</span><span class="sxs-lookup"><span data-stu-id="39720-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="39720-240">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="39720-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39720-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="39720-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="39720-242">(18)</span><span class="sxs-lookup"><span data-stu-id="39720-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="39720-243">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="39720-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="39720-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="39720-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="39720-245">(19)</span><span class="sxs-lookup"><span data-stu-id="39720-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="39720-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="39720-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="39720-247">(20)</span><span class="sxs-lookup"><span data-stu-id="39720-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="39720-248">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="39720-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="39720-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="39720-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="39720-250">(21)</span><span class="sxs-lookup"><span data-stu-id="39720-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="39720-251">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="39720-251">System failure.</span></span> <span data-ttu-id="39720-252">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="39720-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="39720-253">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="39720-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="39720-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="39720-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="39720-255">(22)</span><span class="sxs-lookup"><span data-stu-id="39720-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="39720-256">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="39720-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="39720-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="39720-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="39720-258">(23)</span><span class="sxs-lookup"><span data-stu-id="39720-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="39720-259">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="39720-259">System failure.</span></span> <span data-ttu-id="39720-260">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="39720-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="39720-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="39720-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="39720-262">(24)</span><span class="sxs-lookup"><span data-stu-id="39720-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="39720-263">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="39720-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="39720-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="39720-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="39720-265">(25)</span><span class="sxs-lookup"><span data-stu-id="39720-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="39720-266">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="39720-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="39720-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="39720-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="39720-268">(26)</span><span class="sxs-lookup"><span data-stu-id="39720-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="39720-269">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="39720-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="39720-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="39720-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="39720-271">(27)</span><span class="sxs-lookup"><span data-stu-id="39720-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="39720-272">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="39720-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="39720-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="39720-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="39720-274">(28)</span><span class="sxs-lookup"><span data-stu-id="39720-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="39720-275">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="39720-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="39720-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="39720-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="39720-277">(29)</span><span class="sxs-lookup"><span data-stu-id="39720-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="39720-278">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="39720-278">Device is disabled.</span></span> <span data-ttu-id="39720-279">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="39720-279">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="39720-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="39720-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="39720-281">(30)</span><span class="sxs-lookup"><span data-stu-id="39720-281">(30)</span></span>


</dt> <dd>

<span data-ttu-id="39720-282">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39720-282">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="39720-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="39720-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="39720-284">31,5</span><span class="sxs-lookup"><span data-stu-id="39720-284">(31)</span></span>


</dt> <dd>

<span data-ttu-id="39720-285">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="39720-285">Device is not working properly.</span></span> <span data-ttu-id="39720-286">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="39720-286">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39720-287">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="39720-287">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-288">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="39720-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39720-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-290">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="39720-290">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39720-291">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="39720-291">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="39720-292">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-293">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="39720-293">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-296">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39720-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39720-297">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39720-297">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="39720-298">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="39720-298">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="39720-299">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-300">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="39720-300">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-301">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-301">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-303">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-303">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-304">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="39720-304">Current value indicated by the sensor.</span></span>

<span data-ttu-id="39720-305">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-306">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39720-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-309">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="39720-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="39720-310">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="39720-310">Textual description of the object.</span></span>

<span data-ttu-id="39720-311">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="39720-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-315">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39720-315">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39720-316">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="39720-316">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="39720-317">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-318">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="39720-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-319">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="39720-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39720-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39720-321">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="39720-321">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="39720-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="39720-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39720-326">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="39720-326">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="39720-327">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="39720-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-329">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="39720-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39720-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-331">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="39720-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="39720-332">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="39720-332">Date and time the object was installed.</span></span> <span data-ttu-id="39720-333">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="39720-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="39720-334">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-335">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="39720-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-336">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="39720-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39720-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39720-338">**True** gibt an, dass der Sensor über den dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="39720-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="39720-339">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="39720-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-341">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39720-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39720-343">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="39720-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="39720-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-345">**Lowerstammoldcritical**</span><span class="sxs-lookup"><span data-stu-id="39720-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-346">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-348">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldcritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,13 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-348">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-349">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="39720-349">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="39720-350">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerstammoldcritical** und **loweranoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="39720-350">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="39720-351">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-352">**Lower-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="39720-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-353">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-355">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldfatal"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-355">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-356">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="39720-356">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="39720-357">Wenn die **CurrentReading** -Eigenschaft unterhalb von **Lower-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="39720-357">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="39720-358">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-359">**Lower-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="39720-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-360">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-362">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldnoncritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-362">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-363">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="39720-363">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="39720-364">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="39720-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="39720-365">Wenn die **CurrentReading** -Eigenschaft zwischen **lowertransioldnoncritical** und **lowerstammoldcritical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="39720-365">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="39720-366">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-367">**Maxlesbar**</span><span class="sxs-lookup"><span data-stu-id="39720-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-368">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-370">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("maxlesbar"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,9 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-371">Der größte Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="39720-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="39720-372">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-373">**Minlesbar**</span><span class="sxs-lookup"><span data-stu-id="39720-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-374">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-376">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("minles"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-376">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-377">Der kleinste Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="39720-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="39720-378">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-379">**Name**</span><span class="sxs-lookup"><span data-stu-id="39720-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-380">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-382">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="39720-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="39720-383">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="39720-383">Label by which the object is known.</span></span> <span data-ttu-id="39720-384">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="39720-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="39720-385">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="39720-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-387">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-389">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-390">Erwarteter oder normaler Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="39720-390">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="39720-391">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-392">**Normal Max**</span><span class="sxs-lookup"><span data-stu-id="39720-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-393">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-395">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("normal Max"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-395">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-396">Normaler maximaler Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="39720-396">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="39720-397">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-398">**Normal Minuten**</span><span class="sxs-lookup"><span data-stu-id="39720-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-399">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-401">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-401">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-402">Normaler minimal Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="39720-402">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="39720-403">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="39720-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-405">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-407">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="39720-407">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="39720-408">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="39720-408">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="39720-409">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="39720-410">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="39720-410">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="39720-411">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="39720-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-412">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="39720-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39720-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39720-414">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="39720-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="39720-415">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-415">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39720-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="39720-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="39720-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="39720-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="39720-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="39720-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="39720-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="39720-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="39720-420">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39720-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="39720-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="39720-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="39720-422">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="39720-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="39720-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="39720-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="39720-424">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39720-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="39720-425">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="39720-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="39720-426">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="39720-426">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="39720-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="39720-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="39720-428">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39720-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="39720-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="39720-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="39720-430">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39720-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="39720-431">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="39720-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-432">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="39720-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39720-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39720-434">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="39720-434">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="39720-435">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="39720-435">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="39720-436">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="39720-436">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="39720-437">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="39720-437">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="39720-438">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-439">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="39720-439">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-440">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39720-440">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-442">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,17 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-443">Die Fähigkeit des Sensors, Unterschiede in der gemessenen Eigenschaft aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="39720-443">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="39720-444">Diese Eigenschaft und die **Genauigkeits** -und **Toleranz** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="39720-444">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="39720-445">Dieser Wert kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="39720-445">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="39720-446">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-446">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-447">**Status**</span><span class="sxs-lookup"><span data-stu-id="39720-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-450">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="39720-450">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="39720-451">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="39720-451">Current status of the object.</span></span>

<span data-ttu-id="39720-452">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="39720-453">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="39720-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="39720-454">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="39720-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="39720-455">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="39720-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="39720-456">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="39720-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39720-457">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="39720-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="39720-458">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="39720-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="39720-459">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="39720-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="39720-460">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="39720-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="39720-461">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="39720-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="39720-462">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="39720-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="39720-463">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="39720-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="39720-464">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="39720-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="39720-465">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="39720-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39720-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="39720-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-467">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39720-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39720-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-469">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="39720-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="39720-470">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="39720-470">State of the logical device.</span></span> <span data-ttu-id="39720-471">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39720-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="39720-472">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="39720-473">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="39720-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39720-474">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="39720-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="39720-475">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="39720-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="39720-476">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="39720-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="39720-477">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="39720-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39720-478">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="39720-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-479">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-480">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-481">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39720-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39720-482">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="39720-482">Scoping system's creation class name.</span></span>

<span data-ttu-id="39720-483">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-484">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="39720-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-485">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39720-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39720-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-487">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39720-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39720-488">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="39720-488">Scoping system's name.</span></span>

<span data-ttu-id="39720-489">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-490">**Toleranz**</span><span class="sxs-lookup"><span data-stu-id="39720-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-491">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-492">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-493">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Toleranz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,18 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-494">Toleranz des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="39720-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="39720-495">Diese Eigenschaft und die **Auflösungs** -und **Genauigkeits** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="39720-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="39720-496">Die Toleranz kann abhängig davon variieren, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="39720-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="39720-497">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-497">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-498">**Upperder oldcritical**</span><span class="sxs-lookup"><span data-stu-id="39720-498">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-499">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-499">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-501">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldcritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,14 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-501">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-502">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="39720-502">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="39720-503">Wenn die **CurrentReading** -Eigenschaft zwischen **upperder oldcritical** und **upperanoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="39720-503">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="39720-504">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-504">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-505">**Upper-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="39720-505">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-506">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-506">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-508">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldfatal"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,16 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-508">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-509">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="39720-509">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="39720-510">Wenn die **CurrentReading** -Eigenschaft oberhalb von **Upper-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="39720-510">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="39720-511">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-511">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="39720-512">**Upper-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="39720-512">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39720-513">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39720-513">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39720-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39720-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39720-515">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldnoncritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Spannungstest \| 001,12 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="39720-515">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="39720-516">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="39720-516">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="39720-517">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="39720-517">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="39720-518">Wenn die **CurrentReading** -Eigenschaft zwischen **uppertransioldnoncritical** und **upperder oldcritical Critical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="39720-518">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="39720-519">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="39720-519">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39720-520">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39720-520">Remarks</span></span>

<span data-ttu-id="39720-521">Die CIM-Klasse " **\_ VoltageSensor** " wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="39720-521">The **CIM\_VoltageSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="39720-522">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="39720-522">WMI does not implement this class.</span></span> <span data-ttu-id="39720-523">Informationen zu WMI-Klassen, die von **CIM \_ VoltageSensor** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="39720-523">For WMI classes derived from **CIM\_VoltageSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="39720-524">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="39720-524">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39720-525">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="39720-525">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39720-526">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39720-526">Requirements</span></span>



| <span data-ttu-id="39720-527">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39720-527">Requirement</span></span> | <span data-ttu-id="39720-528">Wert</span><span class="sxs-lookup"><span data-stu-id="39720-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39720-529">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39720-529">Minimum supported client</span></span><br/> | <span data-ttu-id="39720-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39720-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39720-531">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39720-531">Minimum supported server</span></span><br/> | <span data-ttu-id="39720-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39720-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39720-533">Namespace</span><span class="sxs-lookup"><span data-stu-id="39720-533">Namespace</span></span><br/>                | <span data-ttu-id="39720-534">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="39720-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39720-535">MOF</span><span class="sxs-lookup"><span data-stu-id="39720-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39720-536"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="39720-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39720-537">DLL</span><span class="sxs-lookup"><span data-stu-id="39720-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39720-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39720-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39720-539">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39720-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39720-540">**CIM- \_ numericsensor**</span><span class="sxs-lookup"><span data-stu-id="39720-540">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

