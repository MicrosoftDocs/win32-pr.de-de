---
description: Die CIM \_ alarmdevice-Klasse ist ein Alarmgerät, das akustische oder sichtbare Anzeichen für eine Problemsituation ausgibt.
ms.assetid: 1f64aea4-d0a4-480b-9802-e2c21e71c754
ms.tgt_platform: multiple
title: CIM_AlarmDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice
- CIM_AlarmDevice.Caption
- CIM_AlarmDevice.Description
- CIM_AlarmDevice.InstallDate
- CIM_AlarmDevice.Name
- CIM_AlarmDevice.Status
- CIM_AlarmDevice.Availability
- CIM_AlarmDevice.ConfigManagerErrorCode
- CIM_AlarmDevice.ConfigManagerUserConfig
- CIM_AlarmDevice.CreationClassName
- CIM_AlarmDevice.DeviceID
- CIM_AlarmDevice.PowerManagementCapabilities
- CIM_AlarmDevice.ErrorCleared
- CIM_AlarmDevice.ErrorDescription
- CIM_AlarmDevice.LastErrorCode
- CIM_AlarmDevice.PNPDeviceID
- CIM_AlarmDevice.PowerManagementSupported
- CIM_AlarmDevice.StatusInfo
- CIM_AlarmDevice.SystemCreationClassName
- CIM_AlarmDevice.SystemName
- CIM_AlarmDevice.AudibleAlarm
- CIM_AlarmDevice.Urgency
- CIM_AlarmDevice.VisibleAlarm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 622a6031f36140e23514b925835cebae84b35025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523896"
---
# <a name="cim_alarmdevice-class"></a><span data-ttu-id="a003e-103">CIM \_ alarmdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="a003e-103">CIM\_AlarmDevice class</span></span>

<span data-ttu-id="a003e-104">Die **CIM \_ alarmdevice** -Klasse ist ein Alarmgerät, das akustische oder sichtbare Anzeichen für eine Problemsituation ausgibt.</span><span class="sxs-lookup"><span data-stu-id="a003e-104">The **CIM\_AlarmDevice** class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

<span data-ttu-id="a003e-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a003e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a003e-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a003e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a003e-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a003e-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a003e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a003e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a003e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B66-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AlarmDevice : CIM_LogicalDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  AudibleAlarm;
  uint16   Urgency;
  boolean  VisibleAlarm;
};
```

## <a name="members"></a><span data-ttu-id="a003e-110">Member</span><span class="sxs-lookup"><span data-stu-id="a003e-110">Members</span></span>

<span data-ttu-id="a003e-111">Die **CIM \_ alarmdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a003e-111">The **CIM\_AlarmDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="a003e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="a003e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a003e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a003e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a003e-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="a003e-114">Methods</span></span>

<span data-ttu-id="a003e-115">Die **CIM \_ alarmdevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a003e-115">The **CIM\_AlarmDevice** class has these methods.</span></span>



| <span data-ttu-id="a003e-116">Methode</span><span class="sxs-lookup"><span data-stu-id="a003e-116">Method</span></span>                                                                 | <span data-ttu-id="a003e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a003e-117">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a003e-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="a003e-118">**Reset**</span></span>](reset-method-in-class-cim-alarmdevice.md)                 | <span data-ttu-id="a003e-119">Fordert die zurück Setzung eines logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="a003e-119">Requests a logical device reset.</span></span> <span data-ttu-id="a003e-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a003e-120">Not implemented by WMI.</span></span><br/>                                                                     |
| [<span data-ttu-id="a003e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a003e-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md) | <span data-ttu-id="a003e-122">Legt den gewünschten Energiezustand für ein logisches Gerät fest und gibt an, wann das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a003e-122">Sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="a003e-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a003e-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="a003e-124">**Die Sekunden**</span><span class="sxs-lookup"><span data-stu-id="a003e-124">**SetUrgency**</span></span>](seturgency-method-in-class-cim-alarmdevice.md)       | <span data-ttu-id="a003e-125">Legt den gewünschten Dringlichkeits Grad für den Alarm fest.</span><span class="sxs-lookup"><span data-stu-id="a003e-125">Sets the desired urgency level for the alarm.</span></span> <span data-ttu-id="a003e-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a003e-126">Not implemented by WMI.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="a003e-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a003e-127">Properties</span></span>

<span data-ttu-id="a003e-128">Die **CIM \_ alarmdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a003e-128">The **CIM\_AlarmDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a003e-129">**Audiblealarm**</span><span class="sxs-lookup"><span data-stu-id="a003e-129">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a003e-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-132">**True** gibt an, dass der Alarm hörbar ist.</span><span class="sxs-lookup"><span data-stu-id="a003e-132">If **TRUE**, the alarm is audible.</span></span>

</dd> <dt>

<span data-ttu-id="a003e-133">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="a003e-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a003e-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-136">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="a003e-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-137">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a003e-137">Availability and status of the device.</span></span>

<span data-ttu-id="a003e-138">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a003e-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a003e-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a003e-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a003e-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a003e-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="a003e-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a003e-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="a003e-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a003e-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="a003e-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a003e-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="a003e-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a003e-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="a003e-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a003e-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="a003e-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a003e-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="a003e-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a003e-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="a003e-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a003e-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="a003e-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a003e-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="a003e-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a003e-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="a003e-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-152">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a003e-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a003e-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="a003e-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-154">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a003e-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a003e-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="a003e-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-156">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-156">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a003e-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="a003e-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a003e-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="a003e-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-159">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="a003e-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a003e-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="a003e-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-161">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="a003e-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a003e-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="a003e-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-163">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="a003e-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a003e-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="a003e-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-165">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a003e-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a003e-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="a003e-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-167">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="a003e-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a003e-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a003e-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-171">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a003e-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-172">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a003e-172">A short textual description of the object.</span></span>

<span data-ttu-id="a003e-173">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-174">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="a003e-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-175">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a003e-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-177">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a003e-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-178">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a003e-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a003e-179">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a003e-180">**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="a003e-180">**This device is working properly.**</span></span> <span data-ttu-id="a003e-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="a003e-181">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a003e-182">**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="a003e-182">**This device is not configured correctly.**</span></span> <span data-ttu-id="a003e-183">(1)</span><span class="sxs-lookup"><span data-stu-id="a003e-183">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a003e-184">**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="a003e-184">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a003e-185">(2)</span><span class="sxs-lookup"><span data-stu-id="a003e-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a003e-186">**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="a003e-186">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a003e-187">(3)</span><span class="sxs-lookup"><span data-stu-id="a003e-187">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a003e-188">**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="a003e-188">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a003e-189">(4)</span><span class="sxs-lookup"><span data-stu-id="a003e-189">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a003e-190">**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="a003e-190">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a003e-191">(5)</span><span class="sxs-lookup"><span data-stu-id="a003e-191">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a003e-192">**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="a003e-192">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a003e-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="a003e-193">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a003e-194">**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="a003e-194">**Cannot filter.**</span></span> <span data-ttu-id="a003e-195">(7)</span><span class="sxs-lookup"><span data-stu-id="a003e-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a003e-196">**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="a003e-196">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a003e-197">(8)</span><span class="sxs-lookup"><span data-stu-id="a003e-197">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a003e-198">**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="a003e-198">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a003e-199">(9)</span><span class="sxs-lookup"><span data-stu-id="a003e-199">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a003e-200">**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="a003e-200">**This device cannot start.**</span></span> <span data-ttu-id="a003e-201">(10)</span><span class="sxs-lookup"><span data-stu-id="a003e-201">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a003e-202">**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="a003e-202">**This device failed.**</span></span> <span data-ttu-id="a003e-203">(11)</span><span class="sxs-lookup"><span data-stu-id="a003e-203">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a003e-204">**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="a003e-204">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a003e-205">(12)</span><span class="sxs-lookup"><span data-stu-id="a003e-205">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a003e-206">**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="a003e-206">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a003e-207">(13)</span><span class="sxs-lookup"><span data-stu-id="a003e-207">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a003e-208">**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="a003e-208">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a003e-209">(14)</span><span class="sxs-lookup"><span data-stu-id="a003e-209">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a003e-210">**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="a003e-210">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a003e-211">(15)</span><span class="sxs-lookup"><span data-stu-id="a003e-211">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a003e-212">**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="a003e-212">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a003e-213">(16)</span><span class="sxs-lookup"><span data-stu-id="a003e-213">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a003e-214">**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="a003e-214">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a003e-215">(17)</span><span class="sxs-lookup"><span data-stu-id="a003e-215">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a003e-216">**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="a003e-216">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a003e-217">(18)</span><span class="sxs-lookup"><span data-stu-id="a003e-217">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a003e-218">**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="a003e-218">**Failure using the VxD loader.**</span></span> <span data-ttu-id="a003e-219">(19)</span><span class="sxs-lookup"><span data-stu-id="a003e-219">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a003e-220">**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="a003e-220">**Your registry might be corrupted.**</span></span> <span data-ttu-id="a003e-221">(20)</span><span class="sxs-lookup"><span data-stu-id="a003e-221">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a003e-222">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="a003e-222">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a003e-223">(21)</span><span class="sxs-lookup"><span data-stu-id="a003e-223">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a003e-224">**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="a003e-224">**This device is disabled.**</span></span> <span data-ttu-id="a003e-225">(22)</span><span class="sxs-lookup"><span data-stu-id="a003e-225">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a003e-226">**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="a003e-226">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a003e-227">(23)</span><span class="sxs-lookup"><span data-stu-id="a003e-227">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a003e-228">**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="a003e-228">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a003e-229">(24)</span><span class="sxs-lookup"><span data-stu-id="a003e-229">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a003e-230">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="a003e-230">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a003e-231">(25)</span><span class="sxs-lookup"><span data-stu-id="a003e-231">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a003e-232">**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="a003e-232">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a003e-233">(26)</span><span class="sxs-lookup"><span data-stu-id="a003e-233">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a003e-234">**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="a003e-234">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a003e-235">(27)</span><span class="sxs-lookup"><span data-stu-id="a003e-235">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a003e-236">**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="a003e-236">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a003e-237">(28)</span><span class="sxs-lookup"><span data-stu-id="a003e-237">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a003e-238">**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="a003e-238">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a003e-239">(29)</span><span class="sxs-lookup"><span data-stu-id="a003e-239">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a003e-240">**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="a003e-240">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a003e-241">(30)</span><span class="sxs-lookup"><span data-stu-id="a003e-241">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a003e-242">**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="a003e-242">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a003e-243">31,5</span><span class="sxs-lookup"><span data-stu-id="a003e-243">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a003e-244">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="a003e-244">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-245">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a003e-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-247">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a003e-247">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-248">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="a003e-248">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a003e-249">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-249">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-250">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a003e-250">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-253">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a003e-253">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a003e-254">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a003e-254">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a003e-255">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-255">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a003e-256">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-256">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-257">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a003e-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-260">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a003e-260">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-261">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a003e-261">A textual description of the object.</span></span>

<span data-ttu-id="a003e-262">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-263">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a003e-263">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-266">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a003e-266">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a003e-267">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="a003e-267">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a003e-268">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-268">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-269">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="a003e-269">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-270">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a003e-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-272">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a003e-272">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a003e-273">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-273">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-274">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a003e-274">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-275">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-277">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="a003e-277">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a003e-278">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a003e-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-280">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a003e-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-282">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a003e-282">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-283">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a003e-283">Indicates when the object was installed.</span></span> <span data-ttu-id="a003e-284">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a003e-284">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a003e-285">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-285">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-286">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a003e-286">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-287">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a003e-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-289">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a003e-289">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a003e-290">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-291">**Name**</span><span class="sxs-lookup"><span data-stu-id="a003e-291">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-294">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a003e-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-295">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a003e-295">Label by which the object is known.</span></span> <span data-ttu-id="a003e-296">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-296">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a003e-297">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-298">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a003e-298">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-301">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a003e-301">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-302">Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="a003e-302">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a003e-303">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a003e-303">Example: "\*PNP030b"</span></span>

<span data-ttu-id="a003e-304">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-305">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="a003e-305">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-306">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="a003e-306">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a003e-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-308">Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="a003e-308">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="a003e-309">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a003e-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a003e-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-311">Die energiebezogenen Kapazitäten sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a003e-311">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a003e-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="a003e-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-313">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a003e-313">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a003e-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="a003e-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-315">Energiebezogene Kapazitäten wurden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a003e-315">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a003e-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="a003e-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-317">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a003e-317">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a003e-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="a003e-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-319">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="a003e-319">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a003e-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="a003e-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-321">Die **SetPowerState** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a003e-321">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="a003e-322">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-322">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="a003e-323">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a003e-323">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a003e-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="a003e-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-325">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").</span><span class="sxs-lookup"><span data-stu-id="a003e-325">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a003e-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="a003e-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-327">Die **SetPowerState** -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 ("Power Cycle") festgelegt ist und der *Zeit* Parameter auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a003e-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a003e-328">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="a003e-328">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-329">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a003e-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-331">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a003e-331">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a003e-332">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="a003e-332">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a003e-333">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-333">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a003e-334">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="a003e-334">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a003e-335">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-336">**Status**</span><span class="sxs-lookup"><span data-stu-id="a003e-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-339">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a003e-339">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-340">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="a003e-340">String that indicates the current status of the object.</span></span> <span data-ttu-id="a003e-341">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-341">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a003e-342">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a003e-342">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a003e-343">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="a003e-343">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a003e-344">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a003e-344">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a003e-345">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a003e-345">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a003e-346">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a003e-346">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a003e-347">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a003e-348">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a003e-348">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a003e-349">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a003e-349">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a003e-350">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a003e-350">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a003e-351">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a003e-351">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a003e-352">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a003e-352">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a003e-353">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a003e-353">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a003e-354">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a003e-354">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a003e-355">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a003e-355">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a003e-356">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a003e-356">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a003e-357">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a003e-357">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a003e-358">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a003e-358">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a003e-359">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a003e-359">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a003e-360">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a003e-360">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a003e-361">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a003e-361">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-362">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a003e-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-364">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a003e-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a003e-365">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="a003e-365">State of the logical device.</span></span> <span data-ttu-id="a003e-366">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a003e-366">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="a003e-367">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a003e-368">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a003e-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a003e-369">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a003e-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a003e-370">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="a003e-370">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a003e-371">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="a003e-371">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a003e-372">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="a003e-372">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a003e-373">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="a003e-373">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-376">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a003e-376">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a003e-377">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a003e-377">The scoping system's creation class name.</span></span>

<span data-ttu-id="a003e-378">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-379">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="a003e-379">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-380">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a003e-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a003e-382">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a003e-382">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a003e-383">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="a003e-383">The scoping system's name.</span></span>

<span data-ttu-id="a003e-384">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a003e-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a003e-385">**Dringlichkeit**</span><span class="sxs-lookup"><span data-stu-id="a003e-385">**Urgency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-386">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a003e-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-388">Ein Enumerationswert, der die relative Häufigkeit angibt, mit der der Alarm blinkt, vibriert oder akustische Töne ausgibt.</span><span class="sxs-lookup"><span data-stu-id="a003e-388">Enumerated value that indicates the relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a003e-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="a003e-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-390">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="a003e-390">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a003e-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a003e-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-392">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="a003e-392">Other.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a003e-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="a003e-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-394">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a003e-394">Not supported.</span></span>

</dd> <dt>

<span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>

<span data-ttu-id="a003e-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Information** (3)</span><span class="sxs-lookup"><span data-stu-id="a003e-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informational** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-396">Zur Information.</span><span class="sxs-lookup"><span data-stu-id="a003e-396">Informational.</span></span>

</dd> <dt>

<span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>

<span data-ttu-id="a003e-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Nicht kritisch** (4)</span><span class="sxs-lookup"><span data-stu-id="a003e-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non-Critical** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-398">Nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="a003e-398">Non-critical.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a003e-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (5)</span><span class="sxs-lookup"><span data-stu-id="a003e-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-400">Kritisch.</span><span class="sxs-lookup"><span data-stu-id="a003e-400">Critical.</span></span>

</dd> <dt>

<span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>

<span data-ttu-id="a003e-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Nicht wiederherstellbar** (6)</span><span class="sxs-lookup"><span data-stu-id="a003e-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Unrecoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a003e-402">Nicht BEHEB barer.</span><span class="sxs-lookup"><span data-stu-id="a003e-402">Unrecoverable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a003e-403">**Visiblealarm**</span><span class="sxs-lookup"><span data-stu-id="a003e-403">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a003e-404">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a003e-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a003e-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a003e-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a003e-406">**True** gibt an, dass der Alarm sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="a003e-406">If **TRUE**, the alarm is visible.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a003e-407">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a003e-407">Remarks</span></span>

<span data-ttu-id="a003e-408">Die **CIM \_ alarmdevice** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a003e-408">The **CIM\_AlarmDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a003e-409">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a003e-409">WMI does not implement this class.</span></span>

<span data-ttu-id="a003e-410">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a003e-410">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a003e-411">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a003e-411">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a003e-412">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a003e-412">Requirements</span></span>



| <span data-ttu-id="a003e-413">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a003e-413">Requirement</span></span> | <span data-ttu-id="a003e-414">Wert</span><span class="sxs-lookup"><span data-stu-id="a003e-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a003e-415">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a003e-415">Minimum supported client</span></span><br/> | <span data-ttu-id="a003e-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a003e-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a003e-417">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a003e-417">Minimum supported server</span></span><br/> | <span data-ttu-id="a003e-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a003e-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a003e-419">Namespace</span><span class="sxs-lookup"><span data-stu-id="a003e-419">Namespace</span></span><br/>                | <span data-ttu-id="a003e-420">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a003e-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a003e-421">MOF</span><span class="sxs-lookup"><span data-stu-id="a003e-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a003e-422"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a003e-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a003e-423">DLL</span><span class="sxs-lookup"><span data-stu-id="a003e-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a003e-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a003e-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a003e-425">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a003e-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a003e-426">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a003e-426">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

