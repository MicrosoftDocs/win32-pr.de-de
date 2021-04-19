---
description: Die CIM \_ -numericsensor-Klasse stellt einen numerischen Sensor dar, der numerische Messwerte zurückgibt und optional Schwellenwert Einstellungen unterstützt.
ms.assetid: 9be9ee28-24ee-49d1-871f-73b504c77518
ms.tgt_platform: multiple
title: CIM_NumericSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NumericSensor
- CIM_NumericSensor.Accuracy
- CIM_NumericSensor.Availability
- CIM_NumericSensor.Caption
- CIM_NumericSensor.ConfigManagerErrorCode
- CIM_NumericSensor.ConfigManagerUserConfig
- CIM_NumericSensor.CreationClassName
- CIM_NumericSensor.CurrentReading
- CIM_NumericSensor.Description
- CIM_NumericSensor.DeviceID
- CIM_NumericSensor.ErrorCleared
- CIM_NumericSensor.ErrorDescription
- CIM_NumericSensor.InstallDate
- CIM_NumericSensor.IsLinear
- CIM_NumericSensor.LastErrorCode
- CIM_NumericSensor.LowerThresholdCritical
- CIM_NumericSensor.LowerThresholdFatal
- CIM_NumericSensor.LowerThresholdNonCritical
- CIM_NumericSensor.MaxReadable
- CIM_NumericSensor.MinReadable
- CIM_NumericSensor.Name
- CIM_NumericSensor.NominalReading
- CIM_NumericSensor.NormalMax
- CIM_NumericSensor.NormalMin
- CIM_NumericSensor.PNPDeviceID
- CIM_NumericSensor.PowerManagementCapabilities
- CIM_NumericSensor.PowerManagementSupported
- CIM_NumericSensor.Resolution
- CIM_NumericSensor.Status
- CIM_NumericSensor.StatusInfo
- CIM_NumericSensor.SystemCreationClassName
- CIM_NumericSensor.SystemName
- CIM_NumericSensor.Tolerance
- CIM_NumericSensor.UpperThresholdCritical
- CIM_NumericSensor.UpperThresholdFatal
- CIM_NumericSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2888b56e39184b05484cacd587be140b94dc732e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343159"
---
# <a name="cim_numericsensor-class"></a><span data-ttu-id="eecb3-103">CIM- \_ numericsensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="eecb3-103">CIM\_NumericSensor class</span></span>

<span data-ttu-id="eecb3-104">Die **CIM- \_ numericsensor** -Klasse stellt einen numerischen Sensor dar, der numerische Messwerte zurückgibt und optional Schwellenwert Einstellungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-104">The **CIM\_NumericSensor** class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eecb3-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eecb3-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eecb3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eecb3-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="eecb3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eecb3-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eecb3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eecb3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979C-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_NumericSensor : CIM_Sensor
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

## <a name="members"></a><span data-ttu-id="eecb3-110">Member</span><span class="sxs-lookup"><span data-stu-id="eecb3-110">Members</span></span>

<span data-ttu-id="eecb3-111">Die **CIM- \_ numericsensor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eecb3-111">The **CIM\_NumericSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="eecb3-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="eecb3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="eecb3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eecb3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eecb3-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="eecb3-114">Methods</span></span>

<span data-ttu-id="eecb3-115">Die **CIM- \_ numericsensor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-115">The **CIM\_NumericSensor** class has these methods.</span></span>



| <span data-ttu-id="eecb3-116">Methode</span><span class="sxs-lookup"><span data-stu-id="eecb3-116">Method</span></span>                                                                   | <span data-ttu-id="eecb3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eecb3-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eecb3-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="eecb3-118">**Reset**</span></span>](reset-method-in-class-cim-numericsensor.md)                 | <span data-ttu-id="eecb3-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="eecb3-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="eecb3-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="eecb3-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="eecb3-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-numericsensor.md) | <span data-ttu-id="eecb3-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eecb3-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="eecb3-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eecb3-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eecb3-124">Properties</span></span>

<span data-ttu-id="eecb3-125">Die **CIM- \_ numericsensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eecb3-125">The **CIM\_NumericSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eecb3-126">**Genauigkeit**</span><span class="sxs-lookup"><span data-stu-id="eecb3-126">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-127">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-129">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hundertstel Prozent")</span><span class="sxs-lookup"><span data-stu-id="eecb3-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-130">Genauigkeit des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="eecb3-130">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="eecb3-131">Der Wert wird als Plus-oder minus Hundertstel eines Prozentsatzes aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-131">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="eecb3-132">Diese Eigenschaft und die **Auflösungs** -und **Toleranz** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-132">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="eecb3-133">Die Genauigkeit kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-133">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-134">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="eecb3-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eecb3-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="eecb3-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-138">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-138">Availability and status of the device.</span></span>

<span data-ttu-id="eecb3-139">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eecb3-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="eecb3-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eecb3-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="eecb3-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="eecb3-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="eecb3-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="eecb3-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="eecb3-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="eecb3-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="eecb3-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="eecb3-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="eecb3-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="eecb3-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="eecb3-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="eecb3-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="eecb3-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="eecb3-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="eecb3-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eecb3-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="eecb3-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="eecb3-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="eecb3-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="eecb3-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="eecb3-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="eecb3-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="eecb3-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-153">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="eecb3-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="eecb3-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-155">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="eecb3-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="eecb3-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-157">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="eecb3-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="eecb3-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="eecb3-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="eecb3-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-160">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="eecb3-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="eecb3-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-162">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="eecb3-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="eecb3-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="eecb3-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-164">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="eecb3-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="eecb3-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="eecb3-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-166">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="eecb3-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="eecb3-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-168">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="eecb3-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eecb3-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="eecb3-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-172">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="eecb3-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-173">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-173">Short textual description of the object.</span></span>

<span data-ttu-id="eecb3-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-175">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="eecb3-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-176">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-178">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="eecb3-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-179">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="eecb3-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="eecb3-180">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="eecb3-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="eecb3-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="eecb3-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-183">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="eecb3-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="eecb3-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="eecb3-185">(1)</span><span class="sxs-lookup"><span data-stu-id="eecb3-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-186">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eecb3-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="eecb3-188">(2)</span><span class="sxs-lookup"><span data-stu-id="eecb3-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="eecb3-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="eecb3-190">(3)</span><span class="sxs-lookup"><span data-stu-id="eecb3-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-191">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="eecb3-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="eecb3-193">(4)</span><span class="sxs-lookup"><span data-stu-id="eecb3-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-194">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="eecb3-194">Device is not working properly.</span></span> <span data-ttu-id="eecb3-195">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="eecb3-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="eecb3-197">(5)</span><span class="sxs-lookup"><span data-stu-id="eecb3-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-198">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="eecb3-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="eecb3-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="eecb3-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="eecb3-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-201">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="eecb3-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="eecb3-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="eecb3-203">(7)</span><span class="sxs-lookup"><span data-stu-id="eecb3-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="eecb3-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="eecb3-205">(8)</span><span class="sxs-lookup"><span data-stu-id="eecb3-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-206">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="eecb3-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="eecb3-208">(9)</span><span class="sxs-lookup"><span data-stu-id="eecb3-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-209">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="eecb3-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="eecb3-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="eecb3-211">(10)</span><span class="sxs-lookup"><span data-stu-id="eecb3-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-212">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="eecb3-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="eecb3-214">(11)</span><span class="sxs-lookup"><span data-stu-id="eecb3-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-215">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="eecb3-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="eecb3-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="eecb3-217">(12)</span><span class="sxs-lookup"><span data-stu-id="eecb3-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-218">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="eecb3-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="eecb3-220">(13)</span><span class="sxs-lookup"><span data-stu-id="eecb3-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-221">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="eecb3-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="eecb3-223">(14)</span><span class="sxs-lookup"><span data-stu-id="eecb3-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-224">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="eecb3-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="eecb3-226">(15)</span><span class="sxs-lookup"><span data-stu-id="eecb3-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-227">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="eecb3-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="eecb3-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="eecb3-229">(16)</span><span class="sxs-lookup"><span data-stu-id="eecb3-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-230">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="eecb3-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="eecb3-232">(17)</span><span class="sxs-lookup"><span data-stu-id="eecb3-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-233">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="eecb3-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eecb3-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="eecb3-235">(18)</span><span class="sxs-lookup"><span data-stu-id="eecb3-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-236">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="eecb3-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="eecb3-238">(19)</span><span class="sxs-lookup"><span data-stu-id="eecb3-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="eecb3-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="eecb3-240">(20)</span><span class="sxs-lookup"><span data-stu-id="eecb3-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-241">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="eecb3-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="eecb3-243">(21)</span><span class="sxs-lookup"><span data-stu-id="eecb3-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-244">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="eecb3-244">System failure.</span></span> <span data-ttu-id="eecb3-245">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="eecb3-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="eecb3-246">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="eecb3-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="eecb3-248">(22)</span><span class="sxs-lookup"><span data-stu-id="eecb3-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-249">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="eecb3-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="eecb3-251">(23)</span><span class="sxs-lookup"><span data-stu-id="eecb3-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-252">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="eecb3-252">System failure.</span></span> <span data-ttu-id="eecb3-253">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="eecb3-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="eecb3-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="eecb3-255">(24)</span><span class="sxs-lookup"><span data-stu-id="eecb3-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-256">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="eecb3-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="eecb3-258">(25)</span><span class="sxs-lookup"><span data-stu-id="eecb3-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-259">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="eecb3-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="eecb3-261">(26)</span><span class="sxs-lookup"><span data-stu-id="eecb3-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-262">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="eecb3-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="eecb3-264">(27)</span><span class="sxs-lookup"><span data-stu-id="eecb3-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-265">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="eecb3-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="eecb3-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="eecb3-267">(28)</span><span class="sxs-lookup"><span data-stu-id="eecb3-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-268">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="eecb3-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="eecb3-270">(29)</span><span class="sxs-lookup"><span data-stu-id="eecb3-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-271">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="eecb3-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="eecb3-273">(30)</span><span class="sxs-lookup"><span data-stu-id="eecb3-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-274">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eecb3-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="eecb3-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="eecb3-276">31,5</span><span class="sxs-lookup"><span data-stu-id="eecb3-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-277">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eecb3-278">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="eecb3-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-279">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eecb3-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-281">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="eecb3-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-282">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="eecb3-283">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-284">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="eecb3-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-287">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eecb3-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-288">Klasse oder Unterklasse, die beim Erstellen einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-288">Class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="eecb3-289">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="eecb3-290">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-291">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="eecb3-291">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-292">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-292">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-294">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-294">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-295">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eecb3-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-296">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-298">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="eecb3-298">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-299">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-299">Textual description of the object.</span></span>

<span data-ttu-id="eecb3-300">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-301">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="eecb3-301">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-304">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eecb3-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-305">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-305">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="eecb3-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-307">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="eecb3-307">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-308">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eecb3-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-310">**True** gibt an, dass der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="eecb3-310">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="eecb3-311">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-312">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="eecb3-312">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-315">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-315">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="eecb3-316">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eecb3-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-318">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="eecb3-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-320">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="eecb3-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-321">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-321">Date and time the object was installed.</span></span> <span data-ttu-id="eecb3-322">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-322">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="eecb3-323">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-324">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="eecb3-324">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-325">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eecb3-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-327">**True** gibt an, dass der Sensor über den dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-327">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="eecb3-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-329">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-331">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="eecb3-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="eecb3-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-333">**Lowerstammoldcritical**</span><span class="sxs-lookup"><span data-stu-id="eecb3-333">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-334">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-334">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-336">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-336">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="eecb3-337">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerstammoldcritical** und **loweranoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="eecb3-337">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="eecb3-338">Diese Eigenschaft wird vom **CIM- \_ numericsensor** geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-338">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-339">**Lower-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="eecb3-339">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-340">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-342">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-342">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="eecb3-343">Wenn die **CurrentReading** -Eigenschaft unterhalb von **Lower-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="eecb3-343">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="eecb3-344">Diese Eigenschaft wird vom **CIM- \_ numericsensor** geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-344">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-345">**Lower-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="eecb3-345">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-346">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-348">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="eecb3-349">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-349">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="eecb3-350">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerder oldnoncritical** und **lowerstammoldcritical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="eecb3-350">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="eecb3-351">Diese Eigenschaft wird vom **CIM- \_ numericsensor** geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-351">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-352">**Maxlesbar**</span><span class="sxs-lookup"><span data-stu-id="eecb3-352">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-353">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-355">Der größte Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="eecb3-355">Largest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-356">**Minlesbar**</span><span class="sxs-lookup"><span data-stu-id="eecb3-356">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-357">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-359">Der kleinste Wert der gemessenen Eigenschaft, der vom numerischen Sensor gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="eecb3-359">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-360">**Name**</span><span class="sxs-lookup"><span data-stu-id="eecb3-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-363">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="eecb3-363">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-364">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-364">Label by which the object is known.</span></span> <span data-ttu-id="eecb3-365">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-365">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="eecb3-366">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-367">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="eecb3-367">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-368">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-370">Erwarteter oder "normaler" Wert für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="eecb3-370">Expected or "normal" value for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-371">**Normal Max**</span><span class="sxs-lookup"><span data-stu-id="eecb3-371">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-372">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-372">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-374">Normaler maximaler Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="eecb3-374">Normal maximum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-375">**Normal Minuten**</span><span class="sxs-lookup"><span data-stu-id="eecb3-375">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-376">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-376">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-378">Normaler minimal Bereich für den numerischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="eecb3-378">Normal minimum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-379">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eecb3-379">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-380">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-382">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="eecb3-382">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-383">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-383">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="eecb3-384">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="eecb3-385">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="eecb3-385">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-386">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="eecb3-386">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-387">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="eecb3-387">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-389">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-389">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="eecb3-390">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-390">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eecb3-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eecb3-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="eecb3-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="eecb3-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="eecb3-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="eecb3-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="eecb3-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="eecb3-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-395">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eecb3-395">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="eecb3-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="eecb3-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-397">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="eecb3-397">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="eecb3-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="eecb3-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-399">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="eecb3-400">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-400">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="eecb3-401">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="eecb3-401">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="eecb3-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="eecb3-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-403">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-403">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="eecb3-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="eecb3-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="eecb3-405">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eecb3-406">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="eecb3-406">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-407">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eecb3-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-409">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-409">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="eecb3-410">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="eecb3-410">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="eecb3-411">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-411">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="eecb3-412">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="eecb3-412">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="eecb3-413">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-414">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="eecb3-414">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-415">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-415">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-417">Die Fähigkeit des Sensors, Unterschiede in der gemessenen Eigenschaft aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-417">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="eecb3-418">Dieser Wert kann variieren, je nachdem, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-418">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="eecb3-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-420">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-422">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="eecb3-422">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-423">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-423">Current status of the object.</span></span>

<span data-ttu-id="eecb3-424">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-424">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="eecb3-425">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="eecb3-425">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eecb3-426">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="eecb3-426">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eecb3-427">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="eecb3-427">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eecb3-428">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="eecb3-428">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eecb3-429">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="eecb3-429">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eecb3-430">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="eecb3-430">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eecb3-431">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="eecb3-431">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eecb3-432">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="eecb3-432">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eecb3-433">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="eecb3-433">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eecb3-434">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="eecb3-434">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eecb3-435">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="eecb3-435">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eecb3-436">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="eecb3-436">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eecb3-437">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="eecb3-437">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eecb3-438">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="eecb3-438">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-439">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eecb3-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-441">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="eecb3-441">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-442">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="eecb3-442">State of the logical device.</span></span> <span data-ttu-id="eecb3-443">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eecb3-443">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="eecb3-444">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eecb3-445">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="eecb3-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eecb3-446">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="eecb3-446">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="eecb3-447">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="eecb3-447">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="eecb3-448">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="eecb3-448">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="eecb3-449">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="eecb3-449">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eecb3-450">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="eecb3-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-451">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-453">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eecb3-453">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-454">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="eecb3-454">Scoping system's creation class name.</span></span>

<span data-ttu-id="eecb3-455">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-455">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-456">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="eecb3-456">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-457">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eecb3-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-459">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eecb3-459">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-460">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="eecb3-460">Scoping system's name.</span></span>

<span data-ttu-id="eecb3-461">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-462">**Toleranz**</span><span class="sxs-lookup"><span data-stu-id="eecb3-462">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-463">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-463">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-464">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-465">Toleranz des Sensors für die gemessene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="eecb3-465">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="eecb3-466">Diese Eigenschaft und die **Auflösungs** -und **Genauigkeits** Eigenschaften werden verwendet, um den tatsächlichen Wert der gemessenen physischen Eigenschaft zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-466">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="eecb3-467">Die Toleranz kann abhängig davon variieren, ob das Gerät im dynamischen Bereich linear ist.</span><span class="sxs-lookup"><span data-stu-id="eecb3-467">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-468">**Upperder oldcritical**</span><span class="sxs-lookup"><span data-stu-id="eecb3-468">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-469">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-469">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-471">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-471">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="eecb3-472">Wenn die **CurrentReading** -Eigenschaft zwischen **upperder oldcritical** und **upperanoldfatal** liegt, ist der aktuelle Zustand kritisch.</span><span class="sxs-lookup"><span data-stu-id="eecb3-472">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="eecb3-473">Diese Eigenschaft wird vom **CIM- \_ numericsensor** geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-473">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-474">**Upper-oldfatal**</span><span class="sxs-lookup"><span data-stu-id="eecb3-474">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-475">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-475">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-476">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-477">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-477">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="eecb3-478">Wenn die **CurrentReading** -Eigenschaft oberhalb von **Upper-oldfatal** liegt, ist der aktuelle Status schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="eecb3-478">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="eecb3-479">Diese Eigenschaft wird vom **CIM- \_ numericsensor** geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-479">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="eecb3-480">**Upper-oldnoncritical**</span><span class="sxs-lookup"><span data-stu-id="eecb3-480">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eecb3-481">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eecb3-481">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eecb3-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eecb3-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eecb3-483">Schwellenwert, der die Bereiche (minimal-und Maximalwert) angibt, um zu bestimmen, ob der Sensor unter normalen, nicht kritischen, kritischen oder schwerwiegenden Bedingungen betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="eecb3-483">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="eecb3-484">Wenn die **CurrentReading** -Eigenschaft zwischen **lowerationsoldnoncritical** und **upperationsoldnoncritical** liegt, meldet der Sensor einen normalen Wert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-484">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="eecb3-485">Wenn die **CurrentReading** -Eigenschaft zwischen **upperder oldnoncritical** und **upperder oldcritical Critical** liegt, ist der aktuelle Zustand nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="eecb3-485">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="eecb3-486">Diese Eigenschaft wird vom **CIM- \_ numericsensor** geerbt.</span><span class="sxs-lookup"><span data-stu-id="eecb3-486">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eecb3-487">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eecb3-487">Remarks</span></span>

<span data-ttu-id="eecb3-488">Die **CIM- \_ numericsensor** -Klasse wird vom [**CIM- \_ Sensor**](cim-sensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-488">The **CIM\_NumericSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="eecb3-489">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="eecb3-489">WMI does not implement this class.</span></span> <span data-ttu-id="eecb3-490">Informationen zu Klassen, die von **CIM \_ numericsensor** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="eecb3-490">For classes derived from **CIM\_NumericSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="eecb3-491">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eecb3-491">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eecb3-492">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eecb3-492">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eecb3-493">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eecb3-493">Requirements</span></span>



| <span data-ttu-id="eecb3-494">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eecb3-494">Requirement</span></span> | <span data-ttu-id="eecb3-495">Wert</span><span class="sxs-lookup"><span data-stu-id="eecb3-495">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eecb3-496">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eecb3-496">Minimum supported client</span></span><br/> | <span data-ttu-id="eecb3-497">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eecb3-497">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eecb3-498">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eecb3-498">Minimum supported server</span></span><br/> | <span data-ttu-id="eecb3-499">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eecb3-499">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eecb3-500">Namespace</span><span class="sxs-lookup"><span data-stu-id="eecb3-500">Namespace</span></span><br/>                | <span data-ttu-id="eecb3-501">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eecb3-501">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eecb3-502">MOF</span><span class="sxs-lookup"><span data-stu-id="eecb3-502">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eecb3-503"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eecb3-503"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eecb3-504">DLL</span><span class="sxs-lookup"><span data-stu-id="eecb3-504">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eecb3-505"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eecb3-505"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eecb3-506">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eecb3-506">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eecb3-507">**CIM- \_ Sensor**</span><span class="sxs-lookup"><span data-stu-id="eecb3-507">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

