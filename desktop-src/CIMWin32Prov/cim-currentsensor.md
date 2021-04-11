---
description: Die CIM \_ CurrentSensor-Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.
ms.assetid: d1835b09-4286-4586-92ec-f5f77791aea6
ms.tgt_platform: multiple
title: CIM_CurrentSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor
- CIM_CurrentSensor.Accuracy
- CIM_CurrentSensor.Availability
- CIM_CurrentSensor.Caption
- CIM_CurrentSensor.ConfigManagerErrorCode
- CIM_CurrentSensor.ConfigManagerUserConfig
- CIM_CurrentSensor.CreationClassName
- CIM_CurrentSensor.CurrentReading
- CIM_CurrentSensor.Description
- CIM_CurrentSensor.DeviceID
- CIM_CurrentSensor.ErrorCleared
- CIM_CurrentSensor.ErrorDescription
- CIM_CurrentSensor.InstallDate
- CIM_CurrentSensor.IsLinear
- CIM_CurrentSensor.LastErrorCode
- CIM_CurrentSensor.LowerThresholdCritical
- CIM_CurrentSensor.LowerThresholdFatal
- CIM_CurrentSensor.LowerThresholdNonCritical
- CIM_CurrentSensor.MaxReadable
- CIM_CurrentSensor.MinReadable
- CIM_CurrentSensor.Name
- CIM_CurrentSensor.NominalReading
- CIM_CurrentSensor.NormalMax
- CIM_CurrentSensor.NormalMin
- CIM_CurrentSensor.PNPDeviceID
- CIM_CurrentSensor.PowerManagementCapabilities
- CIM_CurrentSensor.PowerManagementSupported
- CIM_CurrentSensor.Resolution
- CIM_CurrentSensor.Status
- CIM_CurrentSensor.StatusInfo
- CIM_CurrentSensor.SystemCreationClassName
- CIM_CurrentSensor.SystemName
- CIM_CurrentSensor.Tolerance
- CIM_CurrentSensor.UpperThresholdCritical
- CIM_CurrentSensor.UpperThresholdFatal
- CIM_CurrentSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1fe2a34e2e598d5c9655abbf84324dbf9982e416
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126997"
---
# <a name="cim_currentsensor-class"></a><span data-ttu-id="f94ae-103">CIM \_ CurrentSensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="f94ae-103">CIM\_CurrentSensor class</span></span>

<span data-ttu-id="f94ae-104">Die **CIM \_ CurrentSensor** -Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-104">The **CIM\_CurrentSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span>

<span data-ttu-id="f94ae-105">Erweiterungen des [**CIM- \_ Sensors**](cim-sensor.md) und des [**CIM- \_ numericsensors**](cim-numericsensor.md) in Version 2,2 machen es nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f94ae-105">Additions to [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) in version 2.2 make it no longer necessary.</span></span> <span data-ttu-id="f94ae-106">Eine **CIM \_ CurrentSensor** -Klasse kann definiert werden, indem die **SensorType** -Eigenschaft, die vom **CIM- \_ Sensor** geerbt wurde, auf 4 ("Current") festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-106">A **CIM\_CurrentSensor** class can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 4 ("Current").</span></span> <span data-ttu-id="f94ae-107">Andere Eigenschaften dieser Klasse sind für konstante Werte hart codiert, die Definitionen in der Sensor Hierarchie entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-107">Other properties of this class are hard-coded to constant values, which correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f94ae-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f94ae-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f94ae-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f94ae-110">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f94ae-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f94ae-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f94ae-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94ae-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f94ae-112">Syntax</span></span>

``` syntax
[UUID("{DCA1D084-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_CurrentSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="f94ae-113">Member</span><span class="sxs-lookup"><span data-stu-id="f94ae-113">Members</span></span>

<span data-ttu-id="f94ae-114">Die **CIM \_ CurrentSensor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f94ae-114">The **CIM\_CurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="f94ae-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="f94ae-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="f94ae-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f94ae-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f94ae-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="f94ae-117">Methods</span></span>

<span data-ttu-id="f94ae-118">Die **CIM \_ CurrentSensor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-118">The **CIM\_CurrentSensor** class has these methods.</span></span>



| <span data-ttu-id="f94ae-119">Methode</span><span class="sxs-lookup"><span data-stu-id="f94ae-119">Method</span></span>                                                                   | <span data-ttu-id="f94ae-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f94ae-120">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f94ae-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="f94ae-121">**Reset**</span></span>](reset-method-in-class-cim-currentsensor.md)                 | <span data-ttu-id="f94ae-122">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="f94ae-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="f94ae-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f94ae-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f94ae-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-currentsensor.md) | <span data-ttu-id="f94ae-125">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f94ae-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f94ae-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f94ae-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f94ae-127">Properties</span></span>

<span data-ttu-id="f94ae-128">Die **CIM \_ CurrentSensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f94ae-128">The **CIM\_CurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f94ae-129">**Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="f94ae-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-130">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-132">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Genauigkeit"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Strom, aktueller Test \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-133">Genauigkeit des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f94ae-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="f94ae-134">Der Wert wird als Plus-oder minus Hundertstel eines Prozentsatzes aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f94ae-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="f94ae-135">Diese Eigenschaft und die **Auflösungs** -und **Toleranz** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="f94ae-136">Die Genauigkeit kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="f94ae-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="f94ae-137">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="f94ae-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f94ae-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-141">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-142">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f94ae-142">Availability and status of the device.</span></span>

<span data-ttu-id="f94ae-143">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f94ae-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f94ae-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f94ae-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f94ae-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f94ae-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="f94ae-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f94ae-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="f94ae-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f94ae-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="f94ae-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f94ae-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="f94ae-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f94ae-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="f94ae-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f94ae-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="f94ae-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f94ae-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="f94ae-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f94ae-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="f94ae-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f94ae-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="f94ae-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f94ae-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="f94ae-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f94ae-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="f94ae-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-157">Energiespeicher ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-157">Power save   unknown.</span></span>

<span data-ttu-id="f94ae-158">Das Gerät befindet sich im Energiesparmodus, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-158">Device is in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f94ae-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="f94ae-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-160">Energiesparmodus im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="f94ae-160">Power save   low-power mode.</span></span>

<span data-ttu-id="f94ae-161">Das Gerät befindet sich im Energiesparmodus und funktioniert weiterhin, kann jedoch eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-161">Device is in a power-save mode and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f94ae-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="f94ae-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-163">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="f94ae-163">Power save   standby.</span></span>

<span data-ttu-id="f94ae-164">Das Gerät funktioniert nicht, aber es kann schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-164">Device is not functioning, but it could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f94ae-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="f94ae-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f94ae-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="f94ae-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-167">Warnung zum Speichern von Energie.</span><span class="sxs-lookup"><span data-stu-id="f94ae-167">Power save   warning.</span></span>

<span data-ttu-id="f94ae-168">Das Gerät befindet sich in einem Warn Status und in einem Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="f94ae-168">Device is in a warning state and a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f94ae-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="f94ae-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f94ae-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="f94ae-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f94ae-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="f94ae-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f94ae-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="f94ae-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-173">Der aktuelle Sensor ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f94ae-173">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f94ae-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f94ae-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-177">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f94ae-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-178">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f94ae-178">Short textual description of the object.</span></span>

<span data-ttu-id="f94ae-179">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-180">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="f94ae-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-181">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-183">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f94ae-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-184">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f94ae-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f94ae-185">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f94ae-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f94ae-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="f94ae-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-188">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f94ae-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f94ae-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f94ae-190">(1)</span><span class="sxs-lookup"><span data-stu-id="f94ae-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-191">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f94ae-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f94ae-193">(2)</span><span class="sxs-lookup"><span data-stu-id="f94ae-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f94ae-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f94ae-195">(3)</span><span class="sxs-lookup"><span data-stu-id="f94ae-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-196">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f94ae-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f94ae-198">(4)</span><span class="sxs-lookup"><span data-stu-id="f94ae-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-199">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f94ae-199">Device is not working properly.</span></span> <span data-ttu-id="f94ae-200">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f94ae-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f94ae-202">(5)</span><span class="sxs-lookup"><span data-stu-id="f94ae-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-203">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f94ae-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f94ae-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f94ae-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="f94ae-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-206">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="f94ae-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f94ae-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f94ae-208">(7)</span><span class="sxs-lookup"><span data-stu-id="f94ae-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f94ae-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f94ae-210">(8)</span><span class="sxs-lookup"><span data-stu-id="f94ae-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-211">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f94ae-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f94ae-213">(9)</span><span class="sxs-lookup"><span data-stu-id="f94ae-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-214">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="f94ae-214">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f94ae-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f94ae-216">(10)</span><span class="sxs-lookup"><span data-stu-id="f94ae-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-217">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f94ae-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f94ae-219">(11)</span><span class="sxs-lookup"><span data-stu-id="f94ae-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-220">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="f94ae-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f94ae-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f94ae-222">(12)</span><span class="sxs-lookup"><span data-stu-id="f94ae-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-223">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f94ae-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f94ae-225">(13)</span><span class="sxs-lookup"><span data-stu-id="f94ae-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-226">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f94ae-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f94ae-228">(14)</span><span class="sxs-lookup"><span data-stu-id="f94ae-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-229">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f94ae-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f94ae-231">(15)</span><span class="sxs-lookup"><span data-stu-id="f94ae-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-232">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="f94ae-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f94ae-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f94ae-234">(16)</span><span class="sxs-lookup"><span data-stu-id="f94ae-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-235">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f94ae-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f94ae-237">(17)</span><span class="sxs-lookup"><span data-stu-id="f94ae-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-238">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="f94ae-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f94ae-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f94ae-240">(18)</span><span class="sxs-lookup"><span data-stu-id="f94ae-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-241">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f94ae-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f94ae-243">(19)</span><span class="sxs-lookup"><span data-stu-id="f94ae-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f94ae-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f94ae-245">(20)</span><span class="sxs-lookup"><span data-stu-id="f94ae-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-246">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f94ae-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f94ae-248">(21)</span><span class="sxs-lookup"><span data-stu-id="f94ae-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-249">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="f94ae-249">System failure.</span></span> <span data-ttu-id="f94ae-250">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f94ae-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f94ae-251">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f94ae-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f94ae-253">(22)</span><span class="sxs-lookup"><span data-stu-id="f94ae-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-254">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f94ae-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f94ae-256">(23)</span><span class="sxs-lookup"><span data-stu-id="f94ae-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-257">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="f94ae-257">System failure.</span></span> <span data-ttu-id="f94ae-258">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f94ae-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f94ae-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f94ae-260">(24)</span><span class="sxs-lookup"><span data-stu-id="f94ae-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-261">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f94ae-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f94ae-263">(25)</span><span class="sxs-lookup"><span data-stu-id="f94ae-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-264">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="f94ae-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f94ae-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f94ae-266">(26)</span><span class="sxs-lookup"><span data-stu-id="f94ae-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-267">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="f94ae-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f94ae-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f94ae-269">(27)</span><span class="sxs-lookup"><span data-stu-id="f94ae-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-270">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f94ae-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f94ae-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f94ae-272">(28)</span><span class="sxs-lookup"><span data-stu-id="f94ae-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-273">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f94ae-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f94ae-275">(29)</span><span class="sxs-lookup"><span data-stu-id="f94ae-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-276">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-276">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f94ae-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f94ae-278">(30)</span><span class="sxs-lookup"><span data-stu-id="f94ae-278">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-279">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-279">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f94ae-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="f94ae-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f94ae-281">31,5</span><span class="sxs-lookup"><span data-stu-id="f94ae-281">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-282">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-282">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f94ae-283">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="f94ae-283">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-284">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f94ae-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-286">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f94ae-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-287">Gibt an, ob das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="f94ae-287">Indicates whether the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f94ae-288">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-289">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f94ae-289">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-290">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-292">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f94ae-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-293">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-293">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f94ae-294">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-294">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f94ae-295">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-296">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="f94ae-296">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-297">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-297">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-299">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,5 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-299">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-300">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-300">Current value indicated by the sensor.</span></span>

<span data-ttu-id="f94ae-301">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-301">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-302">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f94ae-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-305">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f94ae-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-306">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f94ae-306">Textual description of the object.</span></span>

<span data-ttu-id="f94ae-307">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f94ae-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-311">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f94ae-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-312">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f94ae-313">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-314">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="f94ae-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-315">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f94ae-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-317">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f94ae-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f94ae-318">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f94ae-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-322">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f94ae-323">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f94ae-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-325">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f94ae-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-327">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-328">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f94ae-328">Date and time when the object was installed.</span></span> <span data-ttu-id="f94ae-329">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f94ae-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f94ae-330">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-331">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="f94ae-331">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-332">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f94ae-332">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-334">**True** gibt an, dass der Sensor über den dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="f94ae-334">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="f94ae-335">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-335">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-336">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f94ae-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-337">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-339">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f94ae-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f94ae-340">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-341">**Lowerstammoldcritical**</span><span class="sxs-lookup"><span data-stu-id="f94ae-341">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-342">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-342">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-344">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldcritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,13 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-344">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-345">Schwellenwert, der angibt, ob der Sensor unter kritischen Bedingungen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-345">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="f94ae-346">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerstammoldcritical** und **loweranoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="f94ae-346">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="f94ae-347">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-347">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-348">**Lower-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="f94ae-348">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-349">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-349">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-351">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldfatal"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-351">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-352">Schwellenwert, der angibt, ob der Sensor unter schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-352">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="f94ae-353">Wenn die **CurrentReading** -Eigenschaft unterhalb von **Lower-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="f94ae-353">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="f94ae-354">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-354">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-355">**Lower-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="f94ae-355">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-356">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-356">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-358">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("lowerationsoldnoncritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-358">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-359">Schwellenwert, der angibt, ob der Sensor unter normalen oder nicht kritischen Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-359">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="f94ae-360">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-360">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="f94ae-361">Wenn die **CurrentReading** -Eigenschaft jedoch zwischen **Lower-oldnoncritical** und **lowerstammoldcritical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="f94ae-361">If the **CurrentReading** property, however, is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="f94ae-362">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-362">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-363">**Maxlesbar**</span><span class="sxs-lookup"><span data-stu-id="f94ae-363">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-364">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-364">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-366">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("maxlesbar"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,9 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-366">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-367">Der größte Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f94ae-367">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="f94ae-368">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-368">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-369">**Minlesbar**</span><span class="sxs-lookup"><span data-stu-id="f94ae-369">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-370">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-370">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-372">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("minles"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,10 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-372">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-373">Der kleinste Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f94ae-373">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="f94ae-374">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-374">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-375">**Name**</span><span class="sxs-lookup"><span data-stu-id="f94ae-375">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-378">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f94ae-378">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-379">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f94ae-379">Label by which the object is known.</span></span> <span data-ttu-id="f94ae-380">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-380">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f94ae-381">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-381">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-382">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="f94ae-382">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-383">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-383">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-385">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-385">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-386">Erwarteter Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="f94ae-386">Expected value for the numeric sensor.</span></span>

<span data-ttu-id="f94ae-387">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-387">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-388">**Normal Max**</span><span class="sxs-lookup"><span data-stu-id="f94ae-388">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-389">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-389">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-391">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("normal Max"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-391">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-392">Normaler maximaler Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="f94ae-392">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="f94ae-393">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-393">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-394">**Normal Minuten**</span><span class="sxs-lookup"><span data-stu-id="f94ae-394">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-395">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-395">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-397">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-397">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-398">Normaler minimal Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="f94ae-398">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="f94ae-399">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-399">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-400">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f94ae-400">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-403">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f94ae-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-404">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f94ae-404">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f94ae-405">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f94ae-405">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f94ae-406">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-407">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f94ae-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-408">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f94ae-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-410">Bestimmte energiebezogene Funktionen des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f94ae-410">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="f94ae-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f94ae-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f94ae-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f94ae-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="f94ae-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f94ae-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="f94ae-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f94ae-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f94ae-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-416">Energie Verwaltungs Features sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f94ae-416">Power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f94ae-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="f94ae-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-418">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="f94ae-418">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f94ae-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="f94ae-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-420">Die [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-420">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f94ae-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="f94ae-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-422">Die [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="f94ae-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f94ae-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="f94ae-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f94ae-424">Die [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f94ae-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f94ae-425">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="f94ae-425">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-426">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f94ae-426">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-427">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-428">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-428">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f94ae-429">Diese Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-429">This property does not indicate that power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f94ae-430">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="f94ae-430">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f94ae-431">Wenn der Wert **false** ist, sollte der ganzzahlige Wert 1 für die Zeichenfolge "nicht unterstützt" der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="f94ae-431">If **FALSE**, the integer value 1, for the string "Not Supported", should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f94ae-432">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-433">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="f94ae-433">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-434">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-436">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,17 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Zehntel der Millisekunden ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-436">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-437">Die Fähigkeit des Sensors, Unterschiede in der gemessenen Eigenschaft aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-437">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="f94ae-438">Diese Eigenschaft und die **Genauigkeits** -und **Toleranz** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-438">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="f94ae-439">Dieser Wert kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="f94ae-439">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="f94ae-440">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-440">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-441">**Status**</span><span class="sxs-lookup"><span data-stu-id="f94ae-441">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-444">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f94ae-444">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-445">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-445">String that indicates the current status of the object.</span></span> <span data-ttu-id="f94ae-446">Der Betriebs-und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-446">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="f94ae-447">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f94ae-447">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f94ae-448">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="f94ae-448">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f94ae-449">Der Status "nicht betriebsbereit" kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f94ae-449">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f94ae-450">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-450">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f94ae-451">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f94ae-451">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f94ae-452">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f94ae-453">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="f94ae-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f94ae-454">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f94ae-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f94ae-455">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f94ae-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f94ae-456">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f94ae-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f94ae-457">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f94ae-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f94ae-458">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f94ae-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f94ae-459">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f94ae-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f94ae-460">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f94ae-461">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f94ae-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f94ae-462">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f94ae-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f94ae-463">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f94ae-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f94ae-464">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f94ae-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f94ae-465">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f94ae-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f94ae-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f94ae-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-467">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f94ae-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-468">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-469">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-470">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f94ae-470">State of the logical device.</span></span> <span data-ttu-id="f94ae-471">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f94ae-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f94ae-472">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f94ae-473">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f94ae-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f94ae-474">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f94ae-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f94ae-475">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="f94ae-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f94ae-476">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="f94ae-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f94ae-477">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="f94ae-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f94ae-478">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f94ae-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-479">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-480">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-481">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f94ae-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-482">Die Eigenschaft " **kreationclassname** " des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f94ae-482">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="f94ae-483">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-484">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f94ae-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-485">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f94ae-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-487">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f94ae-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-488">Die **Name** -Eigenschaft des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f94ae-488">Scoping system's **Name** property.</span></span>

<span data-ttu-id="f94ae-489">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-490">**Toleranz**</span><span class="sxs-lookup"><span data-stu-id="f94ae-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-491">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-492">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-493">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Toleranz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,18 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-494">Toleranz des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f94ae-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="f94ae-495">Diese Eigenschaft und die **Auflösungs** -und **Genauigkeits** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="f94ae-496">Die Toleranz kann abhängig davon variieren, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="f94ae-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-497">**Upperder oldcritical**</span><span class="sxs-lookup"><span data-stu-id="f94ae-497">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-498">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-498">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-500">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldcritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,14 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-500">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-501">Schwellenwert, der angibt, ob der Sensor unter kritischen Bedingungen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-501">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="f94ae-502">Wenn die **CurrentReading** -Eigenschaft zwischen **upperder oldcritical** und **upperanoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="f94ae-502">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="f94ae-503">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-503">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-504">**Upper-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="f94ae-504">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-505">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-505">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-506">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-507">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldfatal"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,16 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-507">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-508">Schwellenwert, der angibt, ob der Sensor unter schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-508">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="f94ae-509">Wenn die **CurrentReading** -Eigenschaft oberhalb von **Upper-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="f94ae-509">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="f94ae-510">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-510">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94ae-511">**Upper-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="f94ae-511">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f94ae-512">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f94ae-512">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f94ae-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f94ae-514">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("upperationsoldnoncritical"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Electric Current Probe \| 001,12 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="f94ae-514">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="f94ae-515">Schwellenwert, der angibt, ob der Sensor unter normalen oder nicht kritischen Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f94ae-515">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="f94ae-516">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-516">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="f94ae-517">Wenn die **CurrentReading** -Eigenschaft jedoch zwischen **upperder oldnoncritical** und **upperder oldcritical Critical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="f94ae-517">If the **CurrentReading** property, however, is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="f94ae-518">Diese Eigenschaft wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f94ae-518">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f94ae-519">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f94ae-519">Remarks</span></span>

<span data-ttu-id="f94ae-520">Die **CIM \_ CurrentSensor** -Klasse wird vom [**CIM- \_ numericsensor**](cim-numericsensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f94ae-520">The **CIM\_CurrentSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="f94ae-521">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f94ae-521">WMI does not implement this class.</span></span> <span data-ttu-id="f94ae-522">Weitere Informationen zu WMI-Klassen, die von **CIM \_ CurrentSensor** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f94ae-522">For more information about WMI classes derived from **CIM\_CurrentSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f94ae-523">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f94ae-523">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f94ae-524">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f94ae-524">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f94ae-525">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f94ae-525">Requirements</span></span>



| <span data-ttu-id="f94ae-526">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f94ae-526">Requirement</span></span> | <span data-ttu-id="f94ae-527">Wert</span><span class="sxs-lookup"><span data-stu-id="f94ae-527">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f94ae-528">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f94ae-528">Minimum supported client</span></span><br/> | <span data-ttu-id="f94ae-529">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f94ae-529">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f94ae-530">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f94ae-530">Minimum supported server</span></span><br/> | <span data-ttu-id="f94ae-531">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f94ae-531">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f94ae-532">Namespace</span><span class="sxs-lookup"><span data-stu-id="f94ae-532">Namespace</span></span><br/>                | <span data-ttu-id="f94ae-533">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f94ae-533">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f94ae-534">MOF</span><span class="sxs-lookup"><span data-stu-id="f94ae-534">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f94ae-535"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f94ae-535"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f94ae-536">DLL</span><span class="sxs-lookup"><span data-stu-id="f94ae-536">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f94ae-537"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f94ae-537"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94ae-538">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f94ae-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94ae-539">**CIM- \_ numericsensor**</span><span class="sxs-lookup"><span data-stu-id="f94ae-539">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

