---
description: Stellt einen Akku dar, der mit dem Computersystem verbunden ist.
ms.assetid: b07ccb1d-008e-4bf1-8299-33706cbcbaee
ms.tgt_platform: multiple
title: Win32_Battery-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Battery
- Win32_Battery.Reset
- Win32_Battery.SetPowerState
- Win32_Battery.Availability
- Win32_Battery.BatteryRechargeTime
- Win32_Battery.BatteryStatus
- Win32_Battery.Caption
- Win32_Battery.Chemistry
- Win32_Battery.ConfigManagerErrorCode
- Win32_Battery.ConfigManagerUserConfig
- Win32_Battery.CreationClassName
- Win32_Battery.Description
- Win32_Battery.DesignCapacity
- Win32_Battery.DesignVoltage
- Win32_Battery.DeviceID
- Win32_Battery.ErrorCleared
- Win32_Battery.ErrorDescription
- Win32_Battery.EstimatedChargeRemaining
- Win32_Battery.EstimatedRunTime
- Win32_Battery.ExpectedBatteryLife
- Win32_Battery.ExpectedLife
- Win32_Battery.FullChargeCapacity
- Win32_Battery.InstallDate
- Win32_Battery.LastErrorCode
- Win32_Battery.MaxRechargeTime
- Win32_Battery.Name
- Win32_Battery.PNPDeviceID
- Win32_Battery.PowerManagementCapabilities
- Win32_Battery.PowerManagementSupported
- Win32_Battery.SmartBatteryVersion
- Win32_Battery.Status
- Win32_Battery.StatusInfo
- Win32_Battery.SystemCreationClassName
- Win32_Battery.SystemName
- Win32_Battery.TimeOnBattery
- Win32_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75477bcf670bcc0cf16c63f130f95d4c38d7b783
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041514"
---
# <a name="win32_battery-class"></a><span data-ttu-id="6b3dd-103">Win32- \_ Akku Klasse</span><span class="sxs-lookup"><span data-stu-id="6b3dd-103">Win32\_Battery class</span></span>

<span data-ttu-id="6b3dd-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) des **Win32- \_ Akkus** stellt einen Akku dar, der mit dem Computersystem verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-104">The **Win32\_Battery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a battery connected to the computer system.</span></span>

<span data-ttu-id="6b3dd-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6b3dd-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b3dd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b3dd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Battery : CIM_Battery
{
  uint16   Availability;
  uint32   BatteryRechargeTime;
  uint16   BatteryStatus;
  string   Caption;
  uint16   Chemistry;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedBatteryLife;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxRechargeTime;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   SmartBatteryVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="6b3dd-108">Member</span><span class="sxs-lookup"><span data-stu-id="6b3dd-108">Members</span></span>

<span data-ttu-id="6b3dd-109">Die **Win32- \_ Akku** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b3dd-109">The **Win32\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="6b3dd-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b3dd-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6b3dd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b3dd-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6b3dd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b3dd-112">Methods</span></span>

<span data-ttu-id="6b3dd-113">Die **Win32- \_ Akku** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-113">The **Win32\_Battery** class has these methods.</span></span>



| <span data-ttu-id="6b3dd-114">Methode</span><span class="sxs-lookup"><span data-stu-id="6b3dd-114">Method</span></span>            | <span data-ttu-id="6b3dd-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b3dd-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b3dd-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-116">**Reset**</span></span>         | <span data-ttu-id="6b3dd-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-117">Not implemented.</span></span> <span data-ttu-id="6b3dd-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in der [**CIM- \_ Akku**](cim-battery.md) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="6b3dd-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-119">**SetPowerState**</span></span> | <span data-ttu-id="6b3dd-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-120">Not implemented.</span></span> <span data-ttu-id="6b3dd-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in der [**CIM- \_ Akku**](cim-battery.md) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6b3dd-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b3dd-122">Properties</span></span>

<span data-ttu-id="6b3dd-123">Die **Win32- \_ Akku** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-123">The **Win32\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b3dd-124">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-127">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-128">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-128">Availability and status of the device.</span></span>

<span data-ttu-id="6b3dd-129">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b3dd-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b3dd-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6b3dd-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-133">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="6b3dd-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6b3dd-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6b3dd-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b3dd-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6b3dd-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6b3dd-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6b3dd-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6b3dd-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="6b3dd-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6b3dd-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6b3dd-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6b3dd-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6b3dd-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6b3dd-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6b3dd-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6b3dd-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6b3dd-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-153">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6b3dd-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-155">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6b3dd-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-157">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6b3dd-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="6b3dd-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-159">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b3dd-160">**Akku Ladezeit**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-160">**BatteryRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-163">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| LADEGERATE"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minutes")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-163">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-164">Erforderliche Zeit zum vollständigen Berechnen der Akkukapazität.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-164">Time required to fully charge the battery.</span></span> <span data-ttu-id="6b3dd-165">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-165">This property is not supported.</span></span> <span data-ttu-id="6b3dd-166">" **Batteryakku** " hat keine Ersatz Eigenschaft und wird nun als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-166">**BatteryRechargeTime** does not have a replacement property, and is now considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-167">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-167">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-170">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-171">Der Akku Status.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-171">Status of the battery.</span></span> <span data-ttu-id="6b3dd-172">Der Wert 10 (nicht definiert) ist im CIM-Schema ungültig, da er in DMI angibt, dass kein Akku installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-172">The value 10 (Undefined) is not valid in the CIM schema because in DMI it represents that no battery is installed.</span></span> <span data-ttu-id="6b3dd-173">In diesem Fall sollte das Objekt nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-173">In this case, the object should not be instantiated.</span></span>

<span data-ttu-id="6b3dd-174">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-174">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b3dd-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-176">Der Akku wird entladen.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-176">The battery is discharging.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b3dd-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-178">Das System hat Zugriff auf die Systemsteuerung, sodass kein Akku entladen wird.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-178">The system has access to AC so no battery is being discharged.</span></span> <span data-ttu-id="6b3dd-179">Der Akku wird jedoch nicht zwangsläufig berechnet.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-179">However, the battery is not necessarily charging.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="6b3dd-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Vollständig abgerechnet** (3)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="6b3dd-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (4)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="6b3dd-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (5)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="6b3dd-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>Wird **berechnet** (6)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="6b3dd-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Abrechnung und hoch** (7)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="6b3dd-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Abrechnung und niedrig** (8)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="6b3dd-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Abrechnung und kritisch** (9)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6b3dd-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Nicht **definiert** (10)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="6b3dd-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Teilweise abgerechnet** (11)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b3dd-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-192">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-193">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="6b3dd-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-195">**Chemi**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-195">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-198">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-199">Enumeration, die die Chemie des Akkus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-199">Enumeration that describes the battery's chemistry.</span></span>

<span data-ttu-id="6b3dd-200">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-200">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b3dd-201">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-201">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b3dd-202">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-202">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="6b3dd-203">**Führende Acid** (3)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-203">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="6b3dd-204">**Nickel-Cadmium** (4)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-204">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="6b3dd-205">**Nickel-Metal-Hydride** (5)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-205">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="6b3dd-206">**Lithium-Ion** (6)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-206">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="6b3dd-207">**Zink Luft** (7)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-207">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="6b3dd-208">**Lithium-Polymer** (8)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-208">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b3dd-209">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-209">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-210">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-212">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-212">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-213">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-213">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="6b3dd-214">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-214">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6b3dd-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6b3dd-216"> (0)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-216">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-217">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-217">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6b3dd-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6b3dd-219">(1)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-219">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-220">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-220">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6b3dd-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6b3dd-222">(2)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-222">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6b3dd-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6b3dd-224">(3)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-224">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-225">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-225">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6b3dd-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6b3dd-227">(4)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-227">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-228">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-228">Device is not working properly.</span></span> <span data-ttu-id="6b3dd-229">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-229">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6b3dd-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6b3dd-231">(5)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-231">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-232">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-232">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6b3dd-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6b3dd-234"> (6)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-234">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-235">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-235">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6b3dd-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6b3dd-237">(7)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-237">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6b3dd-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6b3dd-239">(8)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-239">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-240">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-240">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6b3dd-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6b3dd-242">(9)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-242">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-243">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-243">Device is not working properly.</span></span> <span data-ttu-id="6b3dd-244">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-244">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6b3dd-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6b3dd-246">(10)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-246">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-247">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-247">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6b3dd-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6b3dd-249">(11)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-249">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-250">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-250">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6b3dd-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6b3dd-252">(12)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-252">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-253">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-253">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6b3dd-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6b3dd-255">(13)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-255">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-256">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-256">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6b3dd-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6b3dd-258">(14)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-258">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-259">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-259">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6b3dd-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6b3dd-261">(15)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-261">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-262">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-262">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6b3dd-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6b3dd-264">(16)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-264">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-265">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-265">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6b3dd-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6b3dd-267">(17)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-267">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-268">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-268">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6b3dd-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6b3dd-270">(18)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-270">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-271">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-271">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6b3dd-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6b3dd-273">(19)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-273">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6b3dd-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6b3dd-275">(20)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-275">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-276">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-276">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6b3dd-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6b3dd-278">(21)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-278">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-279">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-279">System failure.</span></span> <span data-ttu-id="6b3dd-280">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-280">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6b3dd-281">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-281">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6b3dd-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6b3dd-283">(22)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-283">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-284">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-284">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6b3dd-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6b3dd-286">(23)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-286">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-287">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-287">System failure.</span></span> <span data-ttu-id="6b3dd-288">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-288">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6b3dd-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6b3dd-290">(24)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-290">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-291">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-291">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6b3dd-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6b3dd-293">(25)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-293">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-294">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-294">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6b3dd-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6b3dd-296">(26)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-296">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-297">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-297">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6b3dd-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6b3dd-299">(27)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-299">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-300">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-300">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6b3dd-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6b3dd-302">(28)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-302">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-303">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-303">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6b3dd-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6b3dd-305">(29)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-305">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-306">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-306">Device is disabled.</span></span> <span data-ttu-id="6b3dd-307">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-307">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6b3dd-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6b3dd-309">(30)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-309">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-310">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-310">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6b3dd-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6b3dd-312">31,5</span><span class="sxs-lookup"><span data-stu-id="6b3dd-312">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-313">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-313">Device is not working properly.</span></span> <span data-ttu-id="6b3dd-314">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-314">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b3dd-315">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-315">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-316">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b3dd-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-318">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-318">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-319">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-319">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6b3dd-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-321">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-321">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-324">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-325">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-325">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6b3dd-326">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-326">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="6b3dd-327">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-328">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-328">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-331">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-331">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-332">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-332">Description of the object.</span></span>

<span data-ttu-id="6b3dd-333">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-334">**Design Capacity**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-334">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-337">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,8 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt Stunden ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-338">Die Entwurfs Kapazität der Akkukapazität in Milliwatt Stunden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-338">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6b3dd-339">Wenn die Eigenschaft nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-339">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="6b3dd-340">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-340">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-341">**Design Spannung**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-341">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-342">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-344">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,9 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-345">Die Entwurfs Spannung des Akkus in Millivolt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-345">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="6b3dd-346">Wenn das Attribut nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-346">If the attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="6b3dd-347">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-347">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="6b3dd-348">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6b3dd-348">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-352">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-352">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-353">Identifiziert den Akku.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-353">Identifies the battery.</span></span>

<span data-ttu-id="6b3dd-354">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6b3dd-355">Beispiel: "Interner Akku"</span><span class="sxs-lookup"><span data-stu-id="6b3dd-355">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-356">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-357">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b3dd-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-359">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-359">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6b3dd-360">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-362">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-364">Eine frei Form Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu eventuell durchzuführenden Korrekturmaßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-364">Free-form string that supplies more information about the error recorded in **LastErrorCode** property, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="6b3dd-365">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-366">**Estimatedchargeremainung**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-366">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-367">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-369">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-370">Schätzung des Prozentsatzes der verbleibenden Gesamtkosten.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-370">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="6b3dd-371">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-371">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-372">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-372">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-373">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-373">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-375">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,15 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Minuten ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-376">Schätzen Sie die Zeit in Minuten für die Belastung der Akku Kosten unter den aktuellen Ladebedingungen ein, wenn die Stromversorgung ausfällt, verloren geht und ausfällt oder ein Laptop von einer Stromquelle getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-376">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="6b3dd-377">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-378">**Expectedbatterylife**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-378">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-379">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-381">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| batterylife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minutes")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-381">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-382">Die Zeitspanne, die benötigt wird, um den Akku vollständig zu entladen, nachdem er vollständig abgerechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-382">Amount of time it takes to completely drain the battery after it is fully charged.</span></span> <span data-ttu-id="6b3dd-383">Diese Eigenschaft wird nicht mehr verwendet und wird als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-383">This property is no longer used and is considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-384">**Expectedlife**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-384">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-385">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-386">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-387">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-388">Erwartete Lebensdauer des Akkus (in Minuten), vorausgesetzt, dass der Akku vollständig abgerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-388">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="6b3dd-389">Die-Eigenschaft stellt die erwartete Gesamtlebensdauer des Akkus dar, nicht die aktuelle verbleibende Lebensdauer, die durch die **EstimatedRunTime** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-389">The property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="6b3dd-390">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-390">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-391">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-391">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-392">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-394">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,11 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Milliwatt Stunden ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-395">Volle Ladekapazität des Akkus in Milliwatt Stunden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-395">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="6b3dd-396">Der Vergleich des Werts mit der **DesignCapacity** -Eigenschaft bestimmt, wann der Akku ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-396">Comparison of the value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="6b3dd-397">Das Ende der Lebensdauer des Akkus ist normalerweise der Fall, wenn die **FullChargeCapacity** -Eigenschaft unter 80% der **DesignCapacity** -Eigenschaft liegt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-397">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="6b3dd-398">Wenn die Eigenschaft nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-398">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="6b3dd-399">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-399">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-400">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-400">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-401">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-403">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-404">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-404">Date and time the object was installed.</span></span> <span data-ttu-id="6b3dd-405">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-405">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6b3dd-406">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-407">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-407">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-408">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-408">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-410">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-410">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6b3dd-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-412">**Maxakku Zeit**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-412">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-413">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-413">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-415">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-416">Maximale Zeit in Minuten, um den Akku vollständig zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-416">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="6b3dd-417">Die-Eigenschaft stellt die Zeit dar, die eine vollständig abgelegte Akkukapazität wieder auflädt, nicht die derzeit verbleibende Ladezeit, die in der **Timeto fullladung** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-417">The property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="6b3dd-418">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-418">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-419">**Name**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-420">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-422">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-423">Definiert die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-423">Defines the label by which the object is known.</span></span> <span data-ttu-id="6b3dd-424">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-424">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="6b3dd-425">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-426">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-426">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-429">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-429">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-430">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-430">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6b3dd-431">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6b3dd-432">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6b3dd-432">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-433">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-433">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-434">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6b3dd-434">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-436">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-436">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6b3dd-437">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-437">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b3dd-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6b3dd-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b3dd-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b3dd-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-442">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-442">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6b3dd-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-444">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-444">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6b3dd-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-446">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6b3dd-447">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-447">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="6b3dd-448">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6b3dd-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6b3dd-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-450">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6b3dd-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6b3dd-452">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-452">Timed Power-On Supported</span></span>

<span data-ttu-id="6b3dd-453">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b3dd-454">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-454">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-455">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b3dd-455">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-456">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-457">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="6b3dd-457">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="6b3dd-458">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-458">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="6b3dd-459">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-460">**Smartbatteryversion**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-460">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-461">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-462">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-463">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-463">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-464">Die Versionsnummer der Daten Spezifikation, die vom Akku unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-464">Data Specification version number supported by the battery.</span></span> <span data-ttu-id="6b3dd-465">Wenn der Akku diese Funktion nicht unterstützt, sollte der Wert leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-465">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="6b3dd-466">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-466">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-467">**Status**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-467">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-468">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-470">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-470">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-471">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-471">Current status of the object.</span></span> <span data-ttu-id="6b3dd-472">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-472">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6b3dd-473">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="6b3dd-473">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6b3dd-474">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="6b3dd-474">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6b3dd-475">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-475">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6b3dd-476">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-476">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6b3dd-477">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-477">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6b3dd-478">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="6b3dd-478">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6b3dd-479">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-479">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6b3dd-480">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-480">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6b3dd-481">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-481">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b3dd-482">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-482">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6b3dd-483">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-483">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6b3dd-484">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-484">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6b3dd-485">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-485">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6b3dd-486">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-486">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6b3dd-487">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-487">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6b3dd-488">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-488">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6b3dd-489">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-489">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6b3dd-490">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-490">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b3dd-491">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-491">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-492">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-492">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-493">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-494">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-494">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-495">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-495">State of the logical device.</span></span> <span data-ttu-id="6b3dd-496">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-496">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6b3dd-497">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b3dd-498">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-498">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b3dd-499">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-499">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b3dd-500">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-500">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b3dd-501">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-501">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b3dd-502">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-502">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b3dd-503">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-503">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-504">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-504">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-505">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-506">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-506">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-507">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-507">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="6b3dd-508">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-508">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-509">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-509">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-510">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-511">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-512">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-513">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-513">Name of the scoping system.</span></span>

<span data-ttu-id="6b3dd-514">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-515">**Timeonakku**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-515">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-516">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-516">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-517">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-518">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-518">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-519">Verstrichene Zeit in Sekunden seit der letzten Umstellung des Computer Systems auf die Akkuleistung oder die Zeit seit dem letzten Neustart des Systems oder der UPS, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-519">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="6b3dd-520">Wenn der Akku "on line" ist, wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-520">If the battery is "on line", 0 (zero) is returned.</span></span>

<span data-ttu-id="6b3dd-521">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-521">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b3dd-522">**Timeto fullladung**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-522">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3dd-523">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b3dd-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b3dd-525">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Portable Akku \| 002,16 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Minuten ")</span><span class="sxs-lookup"><span data-stu-id="6b3dd-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="6b3dd-526">Verbleibende Zeit zum vollständigen Berechnen der Akkukapazität in Minuten zum aktuellen Abrechnungs Kurs und zur aktuellen Nutzung.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-526">Remaining time to charge the battery fully in minutes at the current charging rate and usage.</span></span>

<span data-ttu-id="6b3dd-527">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-527">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b3dd-528">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b3dd-528">Remarks</span></span>

<span data-ttu-id="6b3dd-529">Die **Win32- \_ Akku** Klasse wird von der CIM- [**\_ Batterie**](cim-battery.md) abgeleitet, die von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-529">The **Win32\_Battery** class is derived from [**CIM\_Battery**](cim-battery.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6b3dd-530">Windows Server 2008 enthält die (APC) UPS-Treiber im Betriebssystem, sodass Sie die UPS als Akku Versorgung behandeln können.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-530">Windows Server 2008 contains the (APC) UPS drivers in the OS, which allows you to treat the UPS as a battery supply.</span></span> <span data-ttu-id="6b3dd-531">Dies ermöglicht es Ihnen, den Status "UPS" mithilfe eines Skripts zu überwachen und bei Bedarf Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-531">This allows you to monitor the UPS status using a script and take actions when necessary.</span></span>

## <a name="examples"></a><span data-ttu-id="6b3dd-532">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b3dd-532">Examples</span></span>

<span data-ttu-id="6b3dd-533">Mit dem [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell-Codebeispiel wird **Win32- \_ Akku** abgefragt, um zu bestimmen, ob das drahtlos Gerät gewechselt werden soll, um Energie zu sparen.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-533">The [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell code sample queries **Win32\_Battery** to determine whether or not to toggle the wireless in order to save power.</span></span>

<span data-ttu-id="6b3dd-534">Das Beispiel [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) perl listet Informationen zu den unterbrechungsfreien Stromquellen an, die an einen Computer angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="6b3dd-534">The [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) Perl sample Lists information about the uninterruptible power sources attached to a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b3dd-535">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b3dd-535">Requirements</span></span>



| <span data-ttu-id="6b3dd-536">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b3dd-536">Requirement</span></span> | <span data-ttu-id="6b3dd-537">Wert</span><span class="sxs-lookup"><span data-stu-id="6b3dd-537">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b3dd-538">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-538">Minimum supported client</span></span><br/> | <span data-ttu-id="6b3dd-539">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b3dd-539">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b3dd-540">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-540">Minimum supported server</span></span><br/> | <span data-ttu-id="6b3dd-541">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b3dd-541">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b3dd-542">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b3dd-542">Namespace</span></span><br/>                | <span data-ttu-id="6b3dd-543">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b3dd-543">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b3dd-544">MOF</span><span class="sxs-lookup"><span data-stu-id="6b3dd-544">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b3dd-545"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6b3dd-545"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b3dd-546">DLL</span><span class="sxs-lookup"><span data-stu-id="6b3dd-546">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b3dd-547"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b3dd-547"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b3dd-548">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b3dd-548">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3dd-549">**CIM- \_ Akku**</span><span class="sxs-lookup"><span data-stu-id="6b3dd-549">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="6b3dd-550">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="6b3dd-550">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

