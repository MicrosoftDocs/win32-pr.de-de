---
description: Die CIM \_ -Lüfter-Klasse stellt die Funktionen und die Verwaltung eines Lüfter-kühl Geräts dar.
ms.assetid: eddfb694-cba1-45e2-998f-f93355520c80
ms.tgt_platform: multiple
title: CIM_Fan-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan
- CIM_Fan.ActiveCooling
- CIM_Fan.Availability
- CIM_Fan.Caption
- CIM_Fan.ConfigManagerErrorCode
- CIM_Fan.ConfigManagerUserConfig
- CIM_Fan.CreationClassName
- CIM_Fan.Description
- CIM_Fan.DesiredSpeed
- CIM_Fan.DeviceID
- CIM_Fan.ErrorCleared
- CIM_Fan.ErrorDescription
- CIM_Fan.InstallDate
- CIM_Fan.LastErrorCode
- CIM_Fan.Name
- CIM_Fan.PNPDeviceID
- CIM_Fan.PowerManagementCapabilities
- CIM_Fan.PowerManagementSupported
- CIM_Fan.Status
- CIM_Fan.StatusInfo
- CIM_Fan.SystemCreationClassName
- CIM_Fan.SystemName
- CIM_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a06e0ddebbdadf7cb4e6dd61afa3fa7c178f661
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861260"
---
# <a name="cim_fan-class"></a><span data-ttu-id="6aad3-103">CIM- \_ Fan-Klasse</span><span class="sxs-lookup"><span data-stu-id="6aad3-103">CIM\_Fan class</span></span>

<span data-ttu-id="6aad3-104">Die **CIM- \_ Lüfter** -Klasse stellt die Funktionen und die Verwaltung eines Lüfter-kühl Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="6aad3-104">The **CIM\_Fan** class represents the capabilities and management of a fan cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6aad3-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6aad3-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6aad3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6aad3-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6aad3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6aad3-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6aad3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aad3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6aad3-109">Syntax</span></span>

``` syntax
[UUID("{0A59C856-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Fan : CIM_CoolingDevice
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="6aad3-110">Member</span><span class="sxs-lookup"><span data-stu-id="6aad3-110">Members</span></span>

<span data-ttu-id="6aad3-111">Die **CIM- \_ Lüfter** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6aad3-111">The **CIM\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="6aad3-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6aad3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6aad3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6aad3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6aad3-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="6aad3-114">Methods</span></span>

<span data-ttu-id="6aad3-115">Die **CIM- \_ Fan** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-115">The **CIM\_Fan** class has these methods.</span></span>



| <span data-ttu-id="6aad3-116">Methode</span><span class="sxs-lookup"><span data-stu-id="6aad3-116">Method</span></span>                                                         | <span data-ttu-id="6aad3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6aad3-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6aad3-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="6aad3-118">**Reset**</span></span>](reset-method-in-class-cim-fan.md)                 | <span data-ttu-id="6aad3-119">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="6aad3-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="6aad3-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="6aad3-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6aad3-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-fan.md) | <span data-ttu-id="6aad3-122">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6aad3-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="6aad3-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="6aad3-124">**SetSpeed**</span><span class="sxs-lookup"><span data-stu-id="6aad3-124">**SetSpeed**</span></span>](setspeed-method-in-class-cim-fan.md)           | <span data-ttu-id="6aad3-125">Legt die Lüfter Geschwindigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="6aad3-125">Sets the fan speed.</span></span> <span data-ttu-id="6aad3-126">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-126">Not implemented by WMI.</span></span><br/>                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="6aad3-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6aad3-127">Properties</span></span>

<span data-ttu-id="6aad3-128">Die **CIM- \_ Lüfter** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6aad3-128">The **CIM\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6aad3-129">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="6aad3-129">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6aad3-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-132">**True** gibt an, dass das kühl Gerät aktiv (im Gegensatz zur passiven) Kühlung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-132">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="6aad3-133">Diese Eigenschaft wird von [**CIM \_ coolingdevice**](cim-coolingdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-133">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-134">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="6aad3-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6aad3-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="6aad3-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-138">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-138">Availability and status of the device.</span></span>

<span data-ttu-id="6aad3-139">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6aad3-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6aad3-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6aad3-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6aad3-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6aad3-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="6aad3-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6aad3-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="6aad3-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6aad3-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="6aad3-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6aad3-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="6aad3-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6aad3-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="6aad3-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6aad3-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="6aad3-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6aad3-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="6aad3-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6aad3-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="6aad3-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6aad3-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="6aad3-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6aad3-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="6aad3-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6aad3-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="6aad3-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-153">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6aad3-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="6aad3-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-155">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6aad3-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6aad3-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="6aad3-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-157">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6aad3-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="6aad3-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6aad3-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="6aad3-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-160">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="6aad3-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6aad3-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="6aad3-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-162">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="6aad3-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6aad3-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="6aad3-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-164">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="6aad3-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6aad3-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="6aad3-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-166">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6aad3-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="6aad3-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-168">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="6aad3-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6aad3-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6aad3-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-172">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6aad3-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-173">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-173">Short textual description of the object.</span></span>

<span data-ttu-id="6aad3-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-175">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="6aad3-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-176">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6aad3-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-178">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6aad3-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-179">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6aad3-179">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="6aad3-180">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6aad3-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6aad3-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="6aad3-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-183">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6aad3-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6aad3-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6aad3-185">(1)</span><span class="sxs-lookup"><span data-stu-id="6aad3-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-186">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6aad3-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6aad3-188">(2)</span><span class="sxs-lookup"><span data-stu-id="6aad3-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6aad3-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6aad3-190">(3)</span><span class="sxs-lookup"><span data-stu-id="6aad3-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-191">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6aad3-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6aad3-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6aad3-193">(4)</span><span class="sxs-lookup"><span data-stu-id="6aad3-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-194">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6aad3-194">Device is not working properly.</span></span> <span data-ttu-id="6aad3-195">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6aad3-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6aad3-197">(5)</span><span class="sxs-lookup"><span data-stu-id="6aad3-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-198">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6aad3-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6aad3-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6aad3-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="6aad3-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-201">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="6aad3-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6aad3-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6aad3-203">(7)</span><span class="sxs-lookup"><span data-stu-id="6aad3-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6aad3-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6aad3-205">(8)</span><span class="sxs-lookup"><span data-stu-id="6aad3-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-206">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6aad3-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6aad3-208">(9)</span><span class="sxs-lookup"><span data-stu-id="6aad3-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-209">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="6aad3-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6aad3-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6aad3-211">(10)</span><span class="sxs-lookup"><span data-stu-id="6aad3-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-212">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6aad3-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6aad3-214">(11)</span><span class="sxs-lookup"><span data-stu-id="6aad3-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-215">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="6aad3-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6aad3-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6aad3-217">(12)</span><span class="sxs-lookup"><span data-stu-id="6aad3-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-218">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6aad3-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6aad3-220">(13)</span><span class="sxs-lookup"><span data-stu-id="6aad3-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-221">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6aad3-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6aad3-223">(14)</span><span class="sxs-lookup"><span data-stu-id="6aad3-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-224">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6aad3-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6aad3-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6aad3-226">(15)</span><span class="sxs-lookup"><span data-stu-id="6aad3-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-227">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6aad3-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6aad3-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6aad3-229">(16)</span><span class="sxs-lookup"><span data-stu-id="6aad3-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-230">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6aad3-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6aad3-232">(17)</span><span class="sxs-lookup"><span data-stu-id="6aad3-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-233">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="6aad3-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6aad3-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6aad3-235">(18)</span><span class="sxs-lookup"><span data-stu-id="6aad3-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-236">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6aad3-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6aad3-238">(19)</span><span class="sxs-lookup"><span data-stu-id="6aad3-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6aad3-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6aad3-240">(20)</span><span class="sxs-lookup"><span data-stu-id="6aad3-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-241">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6aad3-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6aad3-243">(21)</span><span class="sxs-lookup"><span data-stu-id="6aad3-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-244">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="6aad3-244">System failure.</span></span> <span data-ttu-id="6aad3-245">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6aad3-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6aad3-246">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6aad3-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6aad3-248">(22)</span><span class="sxs-lookup"><span data-stu-id="6aad3-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-249">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6aad3-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6aad3-251">(23)</span><span class="sxs-lookup"><span data-stu-id="6aad3-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-252">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="6aad3-252">System failure.</span></span> <span data-ttu-id="6aad3-253">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6aad3-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6aad3-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6aad3-255">(24)</span><span class="sxs-lookup"><span data-stu-id="6aad3-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-256">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6aad3-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6aad3-258">(25)</span><span class="sxs-lookup"><span data-stu-id="6aad3-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-259">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6aad3-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6aad3-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6aad3-261">(26)</span><span class="sxs-lookup"><span data-stu-id="6aad3-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-262">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6aad3-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6aad3-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6aad3-264">(27)</span><span class="sxs-lookup"><span data-stu-id="6aad3-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-265">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6aad3-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6aad3-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6aad3-267">(28)</span><span class="sxs-lookup"><span data-stu-id="6aad3-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-268">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6aad3-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6aad3-270">(29)</span><span class="sxs-lookup"><span data-stu-id="6aad3-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-271">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6aad3-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6aad3-273">(30)</span><span class="sxs-lookup"><span data-stu-id="6aad3-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-274">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6aad3-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6aad3-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="6aad3-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6aad3-276">31,5</span><span class="sxs-lookup"><span data-stu-id="6aad3-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-277">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6aad3-278">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="6aad3-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-279">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6aad3-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-281">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6aad3-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-282">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="6aad3-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6aad3-283">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-284">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="6aad3-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-287">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6aad3-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-288">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6aad3-288">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6aad3-289">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6aad3-290">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-291">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6aad3-291">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-294">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6aad3-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-295">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-295">Textual description of the object.</span></span>

<span data-ttu-id="6aad3-296">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-296">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-297">**Desiredspeed**</span><span class="sxs-lookup"><span data-stu-id="6aad3-297">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-298">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6aad3-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-300">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Umdrehungen pro Minute")</span><span class="sxs-lookup"><span data-stu-id="6aad3-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-301">Die angeforderte Lüfter-Geschwindigkeit in Umdrehungen pro Minute, wenn ein variabler Geschwindigkeits Lüfter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6aad3-301">Requested fan speed, defined in revolutions per minute, when a variable speed fan is supported.</span></span> <span data-ttu-id="6aad3-302">Die aktuelle Geschwindigkeit wird durch einen Sensor ([**CIM- \_ Tachometer**](cim-tachometer.md)) bestimmt, der dem Lüfter mithilfe der [**CIM \_ associatedsensor**](cim-associatedsensor.md) -Beziehung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6aad3-302">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="6aad3-303">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6aad3-303">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-304">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6aad3-304">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-307">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6aad3-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-308">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="6aad3-308">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6aad3-309">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-310">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="6aad3-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-311">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6aad3-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-313">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6aad3-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6aad3-314">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6aad3-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-318">Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="6aad3-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6aad3-319">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-320">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6aad3-320">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-321">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6aad3-321">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-323">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="6aad3-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-324">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-324">Date and time the object was installed.</span></span> <span data-ttu-id="6aad3-325">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6aad3-325">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6aad3-326">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-327">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6aad3-327">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-328">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6aad3-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-330">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6aad3-330">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6aad3-331">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-332">**Name**</span><span class="sxs-lookup"><span data-stu-id="6aad3-332">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-335">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6aad3-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-336">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6aad3-336">Label by which the object is known.</span></span> <span data-ttu-id="6aad3-337">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-337">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6aad3-338">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-339">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6aad3-339">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-342">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6aad3-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-343">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-343">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="6aad3-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6aad3-345">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6aad3-345">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-346">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="6aad3-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-347">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6aad3-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-349">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-349">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6aad3-350">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-350">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6aad3-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6aad3-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6aad3-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="6aad3-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-353">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-353">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6aad3-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="6aad3-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6aad3-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6aad3-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-356">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6aad3-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6aad3-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="6aad3-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-358">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="6aad3-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6aad3-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="6aad3-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-360">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6aad3-361">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6aad3-362">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6aad3-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6aad3-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="6aad3-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-364">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6aad3-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6aad3-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="6aad3-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6aad3-366">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6aad3-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6aad3-367">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="6aad3-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-368">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6aad3-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-370">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="6aad3-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6aad3-371">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="6aad3-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6aad3-372">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6aad3-373">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="6aad3-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="6aad3-374">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-375">**Status**</span><span class="sxs-lookup"><span data-stu-id="6aad3-375">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-378">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6aad3-378">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-379">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-379">Current status of the object.</span></span> <span data-ttu-id="6aad3-380">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6aad3-381">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="6aad3-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6aad3-382">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6aad3-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6aad3-383">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="6aad3-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6aad3-384">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="6aad3-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6aad3-385">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="6aad3-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6aad3-386">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6aad3-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6aad3-387">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="6aad3-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6aad3-388">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="6aad3-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6aad3-389">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="6aad3-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6aad3-390">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="6aad3-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6aad3-391">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="6aad3-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6aad3-392">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="6aad3-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6aad3-393">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="6aad3-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6aad3-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6aad3-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-395">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6aad3-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-397">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6aad3-397">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-398">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6aad3-398">State of the logical device.</span></span> <span data-ttu-id="6aad3-399">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6aad3-399">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6aad3-400">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6aad3-401">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6aad3-401">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6aad3-402">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6aad3-402">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6aad3-403">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6aad3-403">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6aad3-404">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="6aad3-404">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6aad3-405">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="6aad3-405">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6aad3-406">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="6aad3-406">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-407">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-409">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6aad3-409">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-410">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="6aad3-410">Scoping system's creation class name.</span></span>

<span data-ttu-id="6aad3-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-412">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="6aad3-412">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-413">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6aad3-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-415">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6aad3-415">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-416">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="6aad3-416">Scoping system's name.</span></span>

<span data-ttu-id="6aad3-417">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aad3-418">**Variablespeed**</span><span class="sxs-lookup"><span data-stu-id="6aad3-418">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6aad3-419">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6aad3-419">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6aad3-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6aad3-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6aad3-421">**True** gibt an, dass der Lüfter Variablen Geschwindigkeiten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6aad3-421">If **TRUE**, the fan supports variable speeds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6aad3-422">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6aad3-422">Remarks</span></span>

<span data-ttu-id="6aad3-423">Die **CIM- \_ Fan** -Klasse wird von [**CIM \_ coolingdevice**](cim-coolingdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6aad3-423">The **CIM\_Fan** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="6aad3-424">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6aad3-424">WMI does not implement this class.</span></span> <span data-ttu-id="6aad3-425">Informationen zu Klassen, die vom **CIM- \_ Lüfter** abgeleitet sind [, finden Sie](win32-provider.md)unter</span><span class="sxs-lookup"><span data-stu-id="6aad3-425">For classes derived from **CIM\_Fan**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6aad3-426">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6aad3-426">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6aad3-427">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6aad3-427">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aad3-428">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6aad3-428">Requirements</span></span>



| <span data-ttu-id="6aad3-429">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6aad3-429">Requirement</span></span> | <span data-ttu-id="6aad3-430">Wert</span><span class="sxs-lookup"><span data-stu-id="6aad3-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6aad3-431">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6aad3-431">Minimum supported client</span></span><br/> | <span data-ttu-id="6aad3-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6aad3-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6aad3-433">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6aad3-433">Minimum supported server</span></span><br/> | <span data-ttu-id="6aad3-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6aad3-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6aad3-435">Namespace</span><span class="sxs-lookup"><span data-stu-id="6aad3-435">Namespace</span></span><br/>                | <span data-ttu-id="6aad3-436">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6aad3-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6aad3-437">MOF</span><span class="sxs-lookup"><span data-stu-id="6aad3-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6aad3-438"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6aad3-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6aad3-439">DLL</span><span class="sxs-lookup"><span data-stu-id="6aad3-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aad3-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aad3-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aad3-441">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6aad3-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aad3-442">**CIM \_ coolingdevice**</span><span class="sxs-lookup"><span data-stu-id="6aad3-442">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

