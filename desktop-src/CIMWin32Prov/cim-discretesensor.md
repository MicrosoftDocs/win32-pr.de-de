---
description: Die CIM \_ diskretesensor-Klasse verfügt über einen Satz gültiger Zeichen folgen Werte, die Sie melden kann. Die Werte werden in der PossibleValues-Eigenschaft des Sensors aufgelistet. Ein diskreter Sensor verfügt immer über einen aktuellen Lesevorgang, der einem der-Enumerationswerte entspricht.
ms.assetid: 58ab5b4d-ff8b-4981-8f09-c9a255635110
ms.tgt_platform: multiple
title: CIM_DiscreteSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor
- CIM_DiscreteSensor.AcceptableValues
- CIM_DiscreteSensor.Availability
- CIM_DiscreteSensor.Caption
- CIM_DiscreteSensor.ConfigManagerErrorCode
- CIM_DiscreteSensor.ConfigManagerUserConfig
- CIM_DiscreteSensor.CreationClassName
- CIM_DiscreteSensor.CurrentReading
- CIM_DiscreteSensor.Description
- CIM_DiscreteSensor.DeviceID
- CIM_DiscreteSensor.ErrorCleared
- CIM_DiscreteSensor.ErrorDescription
- CIM_DiscreteSensor.InstallDate
- CIM_DiscreteSensor.LastErrorCode
- CIM_DiscreteSensor.Name
- CIM_DiscreteSensor.PNPDeviceID
- CIM_DiscreteSensor.PossibleValues
- CIM_DiscreteSensor.PowerManagementCapabilities
- CIM_DiscreteSensor.PowerManagementSupported
- CIM_DiscreteSensor.Status
- CIM_DiscreteSensor.StatusInfo
- CIM_DiscreteSensor.SystemCreationClassName
- CIM_DiscreteSensor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5211aa8d840384eaf140c1afbeb2fa9c0680cb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523880"
---
# <a name="cim_discretesensor-class"></a><span data-ttu-id="45afd-105">CIM \_ diskretesensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="45afd-105">CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="45afd-106">Die **CIM \_ diskretesensor** -Klasse verfügt über einen Satz gültiger Zeichen folgen Werte, die Sie melden kann.</span><span class="sxs-lookup"><span data-stu-id="45afd-106">The **CIM\_DiscreteSensor** class has a set of legal string values that it can report.</span></span> <span data-ttu-id="45afd-107">Die Werte werden in der **PossibleValues** -Eigenschaft des Sensors aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45afd-107">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="45afd-108">Ein diskreter Sensor verfügt immer über einen aktuellen Lesevorgang, der einem der-Enumerationswerte entspricht.</span><span class="sxs-lookup"><span data-stu-id="45afd-108">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

<span data-ttu-id="45afd-109">Aufgrund der Addition der **CurrentState** -Eigenschaft und der **possiblestates** -Eigenschaft zum [**CIM- \_ Sensor**](cim-sensor.md)ist die diskrete Sensor Unterklasse nicht mehr erforderlich. Sie wird jedoch aus Gründen der Abwärtskompatibilität beibehalten.</span><span class="sxs-lookup"><span data-stu-id="45afd-109">Given the addition of the **CurrentState** and **PossibleStates** properties to [**CIM\_Sensor**](cim-sensor.md), the discrete sensor subclass is no longer necessary; however, it is retained for backward compatibility.</span></span> <span data-ttu-id="45afd-110">Informationen in den Eigenschaften **CurrentReading** und **PossibleValues** verfügen in der Regel über die gleichen Werte und Semantik wie für die Eigenschaften **CurrentState** und **possiblestates** , die vom **CIM- \_ Sensor** geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-110">Information in the **CurrentReading** and **PossibleValues** properties typically has the same values and semantics as for the **CurrentState** and **PossibleStates** properties, which are inherited from **CIM\_Sensor**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45afd-111">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="45afd-112">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="45afd-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="45afd-113">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="45afd-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="45afd-114">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45afd-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45afd-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="45afd-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{1BF00330-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DiscreteSensor : CIM_Sensor
{
  string   AcceptableValues[];
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  string   PossibleValues[];
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="45afd-116">Member</span><span class="sxs-lookup"><span data-stu-id="45afd-116">Members</span></span>

<span data-ttu-id="45afd-117">Die **CIM \_ diskretesensor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="45afd-117">The **CIM\_DiscreteSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="45afd-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="45afd-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="45afd-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45afd-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45afd-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="45afd-120">Methods</span></span>

<span data-ttu-id="45afd-121">Die **CIM \_ diskretesensor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="45afd-121">The **CIM\_DiscreteSensor** class has these methods.</span></span>



| <span data-ttu-id="45afd-122">Methode</span><span class="sxs-lookup"><span data-stu-id="45afd-122">Method</span></span>                                                                | <span data-ttu-id="45afd-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45afd-123">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45afd-124">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="45afd-124">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="45afd-125">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="45afd-125">Requests a reset of the logical device.</span></span> <span data-ttu-id="45afd-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="45afd-126">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="45afd-127">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="45afd-127">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="45afd-128">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="45afd-128">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="45afd-129">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="45afd-129">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45afd-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45afd-130">Properties</span></span>

<span data-ttu-id="45afd-131">Die **CIM \_ diskretesensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45afd-131">The **CIM\_DiscreteSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45afd-132">**Akzeptablevalues**</span><span class="sxs-lookup"><span data-stu-id="45afd-132">**AcceptableValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="45afd-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45afd-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-135">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45afd-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45afd-136">Zeichen folgen in der Eigenschaft " **PossibleValues** " werden als akzeptabel erachtet (d. h., es handelt sich nicht um Fehler).</span><span class="sxs-lookup"><span data-stu-id="45afd-136">Strings in the **PossibleValues** property are considered acceptable (that is, they are not errors).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-137">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="45afd-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-138">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45afd-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="45afd-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-141">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="45afd-141">Availability and status of the device.</span></span>

<span data-ttu-id="45afd-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45afd-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="45afd-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45afd-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="45afd-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="45afd-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="45afd-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="45afd-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="45afd-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="45afd-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="45afd-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="45afd-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="45afd-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="45afd-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="45afd-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="45afd-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="45afd-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="45afd-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="45afd-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45afd-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="45afd-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="45afd-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="45afd-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="45afd-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="45afd-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="45afd-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="45afd-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-156">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="45afd-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="45afd-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="45afd-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-158">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="45afd-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="45afd-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="45afd-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-160">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="45afd-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="45afd-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="45afd-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="45afd-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-163">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="45afd-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="45afd-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="45afd-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-165">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="45afd-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="45afd-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="45afd-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-167">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="45afd-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="45afd-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="45afd-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-169">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="45afd-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="45afd-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="45afd-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-171">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="45afd-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45afd-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45afd-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-175">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="45afd-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-176">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="45afd-176">Short textual description of the object.</span></span>

<span data-ttu-id="45afd-177">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-178">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="45afd-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-179">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45afd-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-181">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45afd-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-182">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="45afd-182">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="45afd-183">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="45afd-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="45afd-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="45afd-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="45afd-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-186">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="45afd-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="45afd-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="45afd-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="45afd-188">(1)</span><span class="sxs-lookup"><span data-stu-id="45afd-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-189">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="45afd-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45afd-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="45afd-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="45afd-191">(2)</span><span class="sxs-lookup"><span data-stu-id="45afd-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="45afd-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="45afd-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="45afd-193">(3)</span><span class="sxs-lookup"><span data-stu-id="45afd-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-194">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="45afd-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="45afd-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="45afd-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="45afd-196">(4)</span><span class="sxs-lookup"><span data-stu-id="45afd-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-197">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="45afd-197">Device is not working properly.</span></span> <span data-ttu-id="45afd-198">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="45afd-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="45afd-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="45afd-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="45afd-200">(5)</span><span class="sxs-lookup"><span data-stu-id="45afd-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-201">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="45afd-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="45afd-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="45afd-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="45afd-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="45afd-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-204">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="45afd-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="45afd-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="45afd-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="45afd-206">(7)</span><span class="sxs-lookup"><span data-stu-id="45afd-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="45afd-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="45afd-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="45afd-208">(8)</span><span class="sxs-lookup"><span data-stu-id="45afd-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-209">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="45afd-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="45afd-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="45afd-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="45afd-211">(9)</span><span class="sxs-lookup"><span data-stu-id="45afd-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-212">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="45afd-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="45afd-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="45afd-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="45afd-214">(10)</span><span class="sxs-lookup"><span data-stu-id="45afd-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-215">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="45afd-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="45afd-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="45afd-217">(11)</span><span class="sxs-lookup"><span data-stu-id="45afd-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-218">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="45afd-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="45afd-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="45afd-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="45afd-220">(12)</span><span class="sxs-lookup"><span data-stu-id="45afd-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-221">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="45afd-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="45afd-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="45afd-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="45afd-223">(13)</span><span class="sxs-lookup"><span data-stu-id="45afd-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-224">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="45afd-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="45afd-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="45afd-226">(14)</span><span class="sxs-lookup"><span data-stu-id="45afd-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-227">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="45afd-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="45afd-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="45afd-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="45afd-229">(15)</span><span class="sxs-lookup"><span data-stu-id="45afd-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-230">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="45afd-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="45afd-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="45afd-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="45afd-232">(16)</span><span class="sxs-lookup"><span data-stu-id="45afd-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-233">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="45afd-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="45afd-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="45afd-235">(17)</span><span class="sxs-lookup"><span data-stu-id="45afd-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-236">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="45afd-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45afd-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="45afd-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="45afd-238">(18)</span><span class="sxs-lookup"><span data-stu-id="45afd-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-239">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="45afd-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="45afd-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="45afd-241">(19)</span><span class="sxs-lookup"><span data-stu-id="45afd-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="45afd-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="45afd-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="45afd-243">(20)</span><span class="sxs-lookup"><span data-stu-id="45afd-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-244">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="45afd-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="45afd-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="45afd-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="45afd-246">(21)</span><span class="sxs-lookup"><span data-stu-id="45afd-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-247">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="45afd-247">System failure.</span></span> <span data-ttu-id="45afd-248">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="45afd-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="45afd-249">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="45afd-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="45afd-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="45afd-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="45afd-251">(22)</span><span class="sxs-lookup"><span data-stu-id="45afd-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-252">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="45afd-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="45afd-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="45afd-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="45afd-254">(23)</span><span class="sxs-lookup"><span data-stu-id="45afd-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-255">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="45afd-255">System failure.</span></span> <span data-ttu-id="45afd-256">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="45afd-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="45afd-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="45afd-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="45afd-258">(24)</span><span class="sxs-lookup"><span data-stu-id="45afd-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-259">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="45afd-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="45afd-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="45afd-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="45afd-261">(25)</span><span class="sxs-lookup"><span data-stu-id="45afd-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-262">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="45afd-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="45afd-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="45afd-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="45afd-264">(26)</span><span class="sxs-lookup"><span data-stu-id="45afd-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-265">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="45afd-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="45afd-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="45afd-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="45afd-267">(27)</span><span class="sxs-lookup"><span data-stu-id="45afd-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-268">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="45afd-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="45afd-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="45afd-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="45afd-270">(28)</span><span class="sxs-lookup"><span data-stu-id="45afd-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-271">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="45afd-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="45afd-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="45afd-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="45afd-273">(29)</span><span class="sxs-lookup"><span data-stu-id="45afd-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-274">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="45afd-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="45afd-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="45afd-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="45afd-276">(30)</span><span class="sxs-lookup"><span data-stu-id="45afd-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-277">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45afd-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="45afd-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="45afd-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="45afd-279">31,5</span><span class="sxs-lookup"><span data-stu-id="45afd-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-280">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45afd-281">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="45afd-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-282">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="45afd-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-284">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45afd-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-285">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="45afd-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="45afd-286">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-287">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="45afd-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-290">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45afd-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45afd-291">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45afd-291">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="45afd-292">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="45afd-293">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="45afd-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-297">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45afd-297">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45afd-298">Aktueller Wert, der vom Sensor angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="45afd-298">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="45afd-299">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45afd-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-302">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="45afd-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-303">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="45afd-303">Textual description of the object.</span></span>

<span data-ttu-id="45afd-304">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="45afd-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-308">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45afd-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45afd-309">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="45afd-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="45afd-310">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-311">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="45afd-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-312">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="45afd-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45afd-314">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="45afd-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="45afd-315">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="45afd-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45afd-319">Eine frei Form Zeichenfolge, die weitere Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="45afd-319">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="45afd-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45afd-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-322">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="45afd-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-324">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="45afd-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-325">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="45afd-325">Date and time when the object was installed.</span></span> <span data-ttu-id="45afd-326">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="45afd-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="45afd-327">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45afd-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-329">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45afd-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45afd-331">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="45afd-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="45afd-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-333">**Name**</span><span class="sxs-lookup"><span data-stu-id="45afd-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-336">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="45afd-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-337">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="45afd-337">Label by which the object is known.</span></span> <span data-ttu-id="45afd-338">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="45afd-339">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="45afd-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-341">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-343">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="45afd-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-344">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="45afd-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="45afd-345">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="45afd-346">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="45afd-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="45afd-347">**PossibleValues**</span><span class="sxs-lookup"><span data-stu-id="45afd-347">**PossibleValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-348">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="45afd-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45afd-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-350">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45afd-350">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45afd-351">Listet die Zeichen folgen Ausgaben des diskreten Sensors auf.</span><span class="sxs-lookup"><span data-stu-id="45afd-351">Enumerates the string outputs from the discrete sensor.</span></span>

</dd> <dt>

<span data-ttu-id="45afd-352">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="45afd-352">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-353">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="45afd-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45afd-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45afd-355">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="45afd-355">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="45afd-356">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-356">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45afd-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="45afd-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="45afd-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="45afd-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="45afd-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="45afd-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="45afd-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="45afd-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-361">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="45afd-361">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="45afd-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="45afd-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-363">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="45afd-363">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="45afd-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="45afd-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-365">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45afd-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="45afd-366">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-366">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="45afd-367">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="45afd-367">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="45afd-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="45afd-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-369">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="45afd-369">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="45afd-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="45afd-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="45afd-371">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="45afd-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45afd-372">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="45afd-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-373">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="45afd-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45afd-375">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="45afd-375">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="45afd-376">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="45afd-376">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="45afd-377">Diese Eigenschaft weist nicht darauf hin, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-377">This property does not indicate that power management features are currently enabled, or if enabled, what features are supported.</span></span> <span data-ttu-id="45afd-378">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="45afd-378">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="45afd-379">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-380">**Status**</span><span class="sxs-lookup"><span data-stu-id="45afd-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-383">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="45afd-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-384">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="45afd-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="45afd-385">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-385">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="45afd-386">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="45afd-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="45afd-387">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="45afd-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="45afd-388">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="45afd-388">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="45afd-389">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="45afd-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="45afd-390">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="45afd-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="45afd-391">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="45afd-392">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="45afd-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="45afd-393">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="45afd-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="45afd-394">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="45afd-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="45afd-395">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="45afd-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45afd-396">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="45afd-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="45afd-397">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="45afd-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="45afd-398">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="45afd-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="45afd-399">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="45afd-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="45afd-400">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="45afd-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="45afd-401">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="45afd-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="45afd-402">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="45afd-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="45afd-403">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="45afd-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="45afd-404">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="45afd-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45afd-405">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="45afd-405">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-406">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45afd-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-408">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="45afd-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="45afd-409">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="45afd-409">State of the logical device.</span></span> <span data-ttu-id="45afd-410">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45afd-410">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="45afd-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="45afd-412">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="45afd-412">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="45afd-413">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="45afd-413">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="45afd-414">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="45afd-414">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="45afd-415">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="45afd-415">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="45afd-416">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="45afd-416">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45afd-417">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="45afd-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-420">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45afd-420">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45afd-421">Die Eigenschaft " **kreationclassname** " des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="45afd-421">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="45afd-422">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-422">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="45afd-423">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="45afd-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45afd-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45afd-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45afd-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45afd-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45afd-426">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="45afd-426">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="45afd-427">Die **Name** -Eigenschaft des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="45afd-427">Scoping system's **Name** property.</span></span>

<span data-ttu-id="45afd-428">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="45afd-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45afd-429">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45afd-429">Remarks</span></span>

<span data-ttu-id="45afd-430">Die CIM-Klasse " **\_ diskretesensor** " wird vom [**CIM- \_ Sensor**](cim-sensor.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="45afd-430">The **CIM\_DiscreteSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="45afd-431">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="45afd-431">WMI does not implement this class.</span></span>

<span data-ttu-id="45afd-432">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="45afd-432">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="45afd-433">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="45afd-433">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="45afd-434">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45afd-434">Requirements</span></span>



| <span data-ttu-id="45afd-435">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45afd-435">Requirement</span></span> | <span data-ttu-id="45afd-436">Wert</span><span class="sxs-lookup"><span data-stu-id="45afd-436">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45afd-437">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45afd-437">Minimum supported client</span></span><br/> | <span data-ttu-id="45afd-438">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45afd-438">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45afd-439">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45afd-439">Minimum supported server</span></span><br/> | <span data-ttu-id="45afd-440">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45afd-440">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45afd-441">Namespace</span><span class="sxs-lookup"><span data-stu-id="45afd-441">Namespace</span></span><br/>                | <span data-ttu-id="45afd-442">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="45afd-442">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45afd-443">MOF</span><span class="sxs-lookup"><span data-stu-id="45afd-443">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45afd-444"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="45afd-444"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45afd-445">DLL</span><span class="sxs-lookup"><span data-stu-id="45afd-445">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45afd-446"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45afd-446"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45afd-447">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45afd-447">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45afd-448">**CIM- \_ Sensor**</span><span class="sxs-lookup"><span data-stu-id="45afd-448">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

