---
description: Die CIM- \_ Temperatursensor Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.
ms.assetid: ddef21db-e33a-4e2b-ac31-df3f0acd6fc2
ms.tgt_platform: multiple
title: CIM_TemperatureSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TemperatureSensor
- CIM_TemperatureSensor.Accuracy
- CIM_TemperatureSensor.Availability
- CIM_TemperatureSensor.Caption
- CIM_TemperatureSensor.ConfigManagerErrorCode
- CIM_TemperatureSensor.ConfigManagerUserConfig
- CIM_TemperatureSensor.CreationClassName
- CIM_TemperatureSensor.CurrentReading
- CIM_TemperatureSensor.Description
- CIM_TemperatureSensor.DeviceID
- CIM_TemperatureSensor.ErrorCleared
- CIM_TemperatureSensor.ErrorDescription
- CIM_TemperatureSensor.InstallDate
- CIM_TemperatureSensor.IsLinear
- CIM_TemperatureSensor.LastErrorCode
- CIM_TemperatureSensor.LowerThresholdCritical
- CIM_TemperatureSensor.LowerThresholdFatal
- CIM_TemperatureSensor.LowerThresholdNonCritical
- CIM_TemperatureSensor.MaxReadable
- CIM_TemperatureSensor.MinReadable
- CIM_TemperatureSensor.Name
- CIM_TemperatureSensor.NominalReading
- CIM_TemperatureSensor.NormalMax
- CIM_TemperatureSensor.NormalMin
- CIM_TemperatureSensor.PNPDeviceID
- CIM_TemperatureSensor.PowerManagementCapabilities
- CIM_TemperatureSensor.PowerManagementSupported
- CIM_TemperatureSensor.Resolution
- CIM_TemperatureSensor.Status
- CIM_TemperatureSensor.StatusInfo
- CIM_TemperatureSensor.SystemCreationClassName
- CIM_TemperatureSensor.SystemName
- CIM_TemperatureSensor.Tolerance
- CIM_TemperatureSensor.UpperThresholdCritical
- CIM_TemperatureSensor.UpperThresholdFatal
- CIM_TemperatureSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f48988db3cb213c06013b7ebac61095dbc365daa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342359"
---
# <a name="cim_temperaturesensor-class"></a><span data-ttu-id="8cc0e-103">CIM \_ temperaturesensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="8cc0e-103">CIM\_TemperatureSensor class</span></span>

<span data-ttu-id="8cc0e-104">Die **CIM- \_ Temperatursensor** Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-104">The **CIM\_TemperatureSensor** class exists for backward compatibility with earlier CIM schema definitions.</span></span> <span data-ttu-id="8cc0e-105">Mit Ergänzungen der [**CIM- \_ Sensor**](cim-sensor.md) -und [**CIM- \_ numericsensor**](cim-numericsensor.md) -Klassen in Version 2,2 ist es nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-105">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="8cc0e-106">Ein Temperatursensor kann definiert werden, indem die **SensorType** -Eigenschaft, die vom **CIM- \_ Sensor** geerbt wurde, auf 2 ("Temperatur") festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-106">A temperature sensor can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 2 ("Temperature").</span></span> <span data-ttu-id="8cc0e-107">Andere Eigenschaften dieser Klasse sind als Konstante Werte hart codiert, die Definitionen in der Sensor Hierarchie entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-107">Other properties of this class are hardcoded as constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cc0e-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8cc0e-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8cc0e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8cc0e-110">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8cc0e-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc0e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc0e-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979D-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_TemperatureSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="8cc0e-113">Member</span><span class="sxs-lookup"><span data-stu-id="8cc0e-113">Members</span></span>

<span data-ttu-id="8cc0e-114">Die **CIM- \_ Temperatursensor** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8cc0e-114">The **CIM\_TemperatureSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="8cc0e-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="8cc0e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="8cc0e-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cc0e-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8cc0e-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="8cc0e-117">Methods</span></span>

<span data-ttu-id="8cc0e-118">Die **CIM \_ temperaturesensor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-118">The **CIM\_TemperatureSensor** class has these methods.</span></span>



| <span data-ttu-id="8cc0e-119">Methode</span><span class="sxs-lookup"><span data-stu-id="8cc0e-119">Method</span></span>                                                                       | <span data-ttu-id="8cc0e-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cc0e-120">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cc0e-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-121">**Reset**</span></span>](reset-method-in-class-cim-temperaturesensor.md)                 | <span data-ttu-id="8cc0e-122">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="8cc0e-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="8cc0e-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-temperaturesensor.md) | <span data-ttu-id="8cc0e-125">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="8cc0e-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8cc0e-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8cc0e-127">Properties</span></span>

<span data-ttu-id="8cc0e-128">Die **CIM \_ temperaturesensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-128">The **CIM\_TemperatureSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cc0e-129">**Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-132">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Genauigkeit"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-133">Genauigkeit des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="8cc0e-134">Der Wert wird als Plus-oder minus Hundertstel eines Prozentsatzes aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="8cc0e-135">Diese Eigenschaft und die **Auflösungs** -und **Toleranz** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="8cc0e-136">Die Genauigkeit kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="8cc0e-137">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-141">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-142">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-142">Availability and status of the device.</span></span>

<span data-ttu-id="8cc0e-143">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8cc0e-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8cc0e-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8cc0e-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-147">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="8cc0e-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8cc0e-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8cc0e-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8cc0e-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8cc0e-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8cc0e-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8cc0e-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8cc0e-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="8cc0e-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8cc0e-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8cc0e-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8cc0e-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-158">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8cc0e-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-160">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8cc0e-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-162">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8cc0e-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8cc0e-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-165">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8cc0e-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-167">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8cc0e-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-169">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8cc0e-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-171">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8cc0e-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="8cc0e-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-173">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8cc0e-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-177">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-178">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-178">Short textual description of the object.</span></span>

<span data-ttu-id="8cc0e-179">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-180">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-181">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-183">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-184">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="8cc0e-185">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8cc0e-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8cc0e-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-188">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8cc0e-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8cc0e-190">(1)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-191">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8cc0e-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8cc0e-193">(2)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8cc0e-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8cc0e-195">(3)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-196">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8cc0e-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8cc0e-198">(4)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-199">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-199">Device is not working properly.</span></span> <span data-ttu-id="8cc0e-200">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8cc0e-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8cc0e-202">(5)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-203">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8cc0e-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8cc0e-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-206">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8cc0e-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8cc0e-208">(7)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8cc0e-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8cc0e-210">(8)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-211">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8cc0e-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8cc0e-213">(9)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-214">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-214">Device is not working properly.</span></span> <span data-ttu-id="8cc0e-215">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8cc0e-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8cc0e-217">(10)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-218">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8cc0e-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8cc0e-220">(11)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-221">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8cc0e-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8cc0e-223">(12)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-224">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8cc0e-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8cc0e-226">(13)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-227">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8cc0e-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8cc0e-229">(14)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-230">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8cc0e-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8cc0e-232">(15)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-233">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8cc0e-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8cc0e-235">(16)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-236">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8cc0e-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8cc0e-238">(17)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-239">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8cc0e-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8cc0e-241">(18)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-242">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8cc0e-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8cc0e-244">(19)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8cc0e-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8cc0e-246">(20)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-247">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8cc0e-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8cc0e-249">(21)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-250">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-250">System failure.</span></span> <span data-ttu-id="8cc0e-251">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8cc0e-252">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8cc0e-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8cc0e-254">(22)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-255">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8cc0e-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8cc0e-257">(23)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-258">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-258">System failure.</span></span> <span data-ttu-id="8cc0e-259">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8cc0e-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8cc0e-261">(24)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-262">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8cc0e-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8cc0e-264">(25)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-265">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8cc0e-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8cc0e-267">(26)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-268">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8cc0e-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8cc0e-270">(27)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-271">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8cc0e-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8cc0e-273">(28)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-274">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8cc0e-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8cc0e-276">(29)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-277">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-277">Device is disabled.</span></span> <span data-ttu-id="8cc0e-278">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8cc0e-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8cc0e-280">(30)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-281">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8cc0e-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8cc0e-283">31,5</span><span class="sxs-lookup"><span data-stu-id="8cc0e-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-284">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-284">Device is not working properly.</span></span> <span data-ttu-id="8cc0e-285">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8cc0e-286">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-287">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8cc0e-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-289">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-290">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8cc0e-291">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-292">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-295">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-296">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8cc0e-297">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8cc0e-298">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-299">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-299">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-300">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-300">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-302">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-302">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-303">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-303">Current value indicated by the sensor.</span></span>

<span data-ttu-id="8cc0e-304">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-304">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-305">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-305">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-308">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-309">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-309">Textual description of the object.</span></span>

<span data-ttu-id="8cc0e-310">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-311">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-311">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-314">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-314">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-315">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-315">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="8cc0e-316">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-317">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-317">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-318">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8cc0e-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-320">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-320">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="8cc0e-321">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-322">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-322">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-323">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-325">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-325">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="8cc0e-326">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-327">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-327">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-328">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-330">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-331">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-331">Date and time the object was installed.</span></span> <span data-ttu-id="8cc0e-332">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-332">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8cc0e-333">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-334">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-334">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-335">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8cc0e-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-337">**True** gibt an, dass der Sensor über den dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-337">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="8cc0e-338">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-338">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-340">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-342">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-342">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8cc0e-343">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-344">**Lowerstammoldcritical**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-344">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-345">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-345">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-347">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldcritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,13 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-347">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-348">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="8cc0e-349">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerstammoldcritical** und **loweranoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-349">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="8cc0e-350">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-350">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-351">**Lower-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-351">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-352">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-352">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-354">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldfatal"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-354">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-355">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-355">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="8cc0e-356">Wenn die **CurrentReading** -Eigenschaft unterhalb von **Lower-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-356">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="8cc0e-357">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-357">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-358">**Lower-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-358">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-359">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-359">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-361">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldnoncritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-361">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-362">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-362">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="8cc0e-363">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-363">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="8cc0e-364">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerder oldnoncritical** und **lowerstammoldcritical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="8cc0e-365">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-366">**Maxlesbar**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-366">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-367">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-369">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("maxlesbar"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,9 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-369">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-370">Der größte Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-370">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="8cc0e-371">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-372">**Minlesbar**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-372">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-373">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-373">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-375">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("minles"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-375">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-376">Der kleinste Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-376">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="8cc0e-377">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-377">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-378">**Name**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-378">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-381">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-381">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-382">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-382">Label by which the object is known.</span></span> <span data-ttu-id="8cc0e-383">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-383">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8cc0e-384">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-384">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-385">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-385">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-386">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-388">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-388">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-389">Erwarteter oder normaler Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-389">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="8cc0e-390">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-391">**Normal Max**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-391">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-392">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-394">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("normal Max"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-394">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-395">Normaler maximaler Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-395">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="8cc0e-396">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-397">**Normal Minuten**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-397">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-398">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-398">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-400">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-400">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-401">Normaler minimal Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-401">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="8cc0e-402">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-402">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-403">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-403">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-404">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-406">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-406">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-407">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-407">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="8cc0e-408">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8cc0e-409">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8cc0e-409">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-410">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-410">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-411">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="8cc0e-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-413">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-413">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8cc0e-414">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-414">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8cc0e-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8cc0e-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8cc0e-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8cc0e-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-419">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-419">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8cc0e-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-421">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-421">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8cc0e-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-423">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8cc0e-424">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-424">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8cc0e-425">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="8cc0e-425">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8cc0e-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-427">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-427">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8cc0e-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8cc0e-429">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-429">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8cc0e-430">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-430">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-431">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8cc0e-431">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-433">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-433">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="8cc0e-434">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-434">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="8cc0e-435">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-435">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="8cc0e-436">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-436">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="8cc0e-437">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-438">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-438">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-439">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-441">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,17 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hundertstel Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-441">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-442">Die Fähigkeit des Sensors, Unterschiede in der gemessenen Eigenschaft aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-442">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="8cc0e-443">Dieser Wert kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-443">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="8cc0e-444">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-444">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-445">**Status**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-446">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-448">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-449">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-449">Current status of the object.</span></span> <span data-ttu-id="8cc0e-450">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8cc0e-451">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8cc0e-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8cc0e-452">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8cc0e-453">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8cc0e-454">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8cc0e-455">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8cc0e-456">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8cc0e-457">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8cc0e-458">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8cc0e-459">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8cc0e-460">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8cc0e-461">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8cc0e-462">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8cc0e-463">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8cc0e-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-465">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-466">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-467">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-468">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-468">State of the logical device.</span></span> <span data-ttu-id="8cc0e-469">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8cc0e-470">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8cc0e-471">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8cc0e-472">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8cc0e-473">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8cc0e-474">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8cc0e-475">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8cc0e-476">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-477">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-478">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-479">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-480">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="8cc0e-481">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-482">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-483">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-484">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-485">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-486">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-486">Scoping system's name.</span></span>

<span data-ttu-id="8cc0e-487">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-488">**Toleranz**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-488">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-489">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-489">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-490">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-491">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Toleranz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,18 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-491">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-492">Toleranz des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-492">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="8cc0e-493">Diese Eigenschaft und die **Auflösungs** -und **Genauigkeits** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-493">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="8cc0e-494">Die Toleranz kann abhängig davon variieren, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-494">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="8cc0e-495">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-495">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-496">**Upperder oldcritical**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-496">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-497">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-497">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-498">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-499">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldcritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,14 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-499">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-500">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-500">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="8cc0e-501">Wenn die **CurrentReading** -Eigenschaft zwischen **upperder oldcritical** und **upperanoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-501">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="8cc0e-502">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-502">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-503">**Upper-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-503">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-504">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-504">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-505">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-506">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldfatal"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,16 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-506">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-507">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-507">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="8cc0e-508">Wenn die **CurrentReading** -Eigenschaft oberhalb von **Upper-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-508">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="8cc0e-509">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-509">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="8cc0e-510">**Upper-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-510">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cc0e-511">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-511">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-512">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8cc0e-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cc0e-513">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldnoncritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Temperatur Test \| 001,12 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Grad Celsius ")</span><span class="sxs-lookup"><span data-stu-id="8cc0e-513">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="8cc0e-514">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-514">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="8cc0e-515">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-515">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="8cc0e-516">Wenn die **CurrentReading** -Eigenschaft zwischen **upperder oldnoncritical** und **upperder oldcritical Critical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-516">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="8cc0e-517">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-517">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cc0e-518">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cc0e-518">Remarks</span></span>

<span data-ttu-id="8cc0e-519">Die **CIM- \_ Temperatursensor** Klasse wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-519">The **CIM\_TemperatureSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="8cc0e-520">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-520">WMI does not implement this class.</span></span> <span data-ttu-id="8cc0e-521">Informationen zu WMI-Klassen, die von **CIM \_ Temperatursensor** abgeleitet werden, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8cc0e-521">For WMI classes derived from **CIM\_TemperatureSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8cc0e-522">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-522">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8cc0e-523">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8cc0e-523">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc0e-524">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cc0e-524">Requirements</span></span>



| <span data-ttu-id="8cc0e-525">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cc0e-525">Requirement</span></span> | <span data-ttu-id="8cc0e-526">Wert</span><span class="sxs-lookup"><span data-stu-id="8cc0e-526">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc0e-527">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-527">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc0e-528">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cc0e-528">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8cc0e-529">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cc0e-529">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc0e-530">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cc0e-530">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8cc0e-531">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cc0e-531">Namespace</span></span><br/>                | <span data-ttu-id="8cc0e-532">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8cc0e-532">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8cc0e-533">MOF</span><span class="sxs-lookup"><span data-stu-id="8cc0e-533">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cc0e-534"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8cc0e-534"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cc0e-535">DLL</span><span class="sxs-lookup"><span data-stu-id="8cc0e-535">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cc0e-536"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cc0e-536"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cc0e-537">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cc0e-537">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc0e-538">**CIM- \_ numericsensor**</span><span class="sxs-lookup"><span data-stu-id="8cc0e-538">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

