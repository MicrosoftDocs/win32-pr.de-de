---
description: Die Win32 \_ portableakku-WMI-Klasse enthält die Eigenschaften, die sich auf einen tragbaren Akku beziehen, z. b. eine Notebook-Computer Batterie.
ms.assetid: ca7d061f-8fc6-4a1e-aa75-2465ce5e2735
ms.tgt_platform: multiple
title: Win32_PortableBattery-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortableBattery
- Win32_PortableBattery.Reset
- Win32_PortableBattery.SetPowerState
- Win32_PortableBattery.Availability
- Win32_PortableBattery.BatteryStatus
- Win32_PortableBattery.CapacityMultiplier
- Win32_PortableBattery.Caption
- Win32_PortableBattery.Chemistry
- Win32_PortableBattery.ConfigManagerErrorCode
- Win32_PortableBattery.ConfigManagerUserConfig
- Win32_PortableBattery.CreationClassName
- Win32_PortableBattery.Description
- Win32_PortableBattery.DesignCapacity
- Win32_PortableBattery.DesignVoltage
- Win32_PortableBattery.DeviceID
- Win32_PortableBattery.ErrorCleared
- Win32_PortableBattery.ErrorDescription
- Win32_PortableBattery.EstimatedChargeRemaining
- Win32_PortableBattery.EstimatedRunTime
- Win32_PortableBattery.ExpectedBatteryLife
- Win32_PortableBattery.ExpectedLife
- Win32_PortableBattery.FullChargeCapacity
- Win32_PortableBattery.InstallDate
- Win32_PortableBattery.LastErrorCode
- Win32_PortableBattery.Location
- Win32_PortableBattery.ManufactureDate
- Win32_PortableBattery.Manufacturer
- Win32_PortableBattery.MaxBatteryError
- Win32_PortableBattery.MaxRechargeTime
- Win32_PortableBattery.Name
- Win32_PortableBattery.PNPDeviceID
- Win32_PortableBattery.PowerManagementCapabilities
- Win32_PortableBattery.PowerManagementSupported
- Win32_PortableBattery.SmartBatteryVersion
- Win32_PortableBattery.Status
- Win32_PortableBattery.StatusInfo
- Win32_PortableBattery.SystemCreationClassName
- Win32_PortableBattery.SystemName
- Win32_PortableBattery.TimeOnBattery
- Win32_PortableBattery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9db875e7e4d1736cf45945b53f2f20fec0490a47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747912"
---
# <a name="win32_portablebattery-class"></a><span data-ttu-id="248aa-103">Win32 \_ portableakku-Klasse</span><span class="sxs-lookup"><span data-stu-id="248aa-103">Win32\_PortableBattery class</span></span>

<span data-ttu-id="248aa-104">Die **Win32 \_ portableakku** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) enthält die Eigenschaften, die sich auf einen tragbaren Akku beziehen, z. b. eine Notebook-Computer Batterie.</span><span class="sxs-lookup"><span data-stu-id="248aa-104">The **Win32\_PortableBattery** [WMI class](../wmisdk/retrieving-a-class.md) contains the properties related to a portable battery, such as a notebook computer battery.</span></span>

<span data-ttu-id="248aa-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="248aa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="248aa-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="248aa-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="248aa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="248aa-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortableBattery : CIM_Battery
{
  uint16   Availability;
  uint16   BatteryStatus;
  uint16   CapacityMultiplier;
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
  string   Location;
  string   ManufactureDate;
  string   Manufacturer;
  uint16   MaxBatteryError;
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

## <a name="members"></a><span data-ttu-id="248aa-108">Member</span><span class="sxs-lookup"><span data-stu-id="248aa-108">Members</span></span>

<span data-ttu-id="248aa-109">Die **Win32- \_ portableakku** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="248aa-109">The **Win32\_PortableBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="248aa-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="248aa-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="248aa-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="248aa-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="248aa-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="248aa-112">Methods</span></span>

<span data-ttu-id="248aa-113">Die **Win32- \_ portableakku** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="248aa-113">The **Win32\_PortableBattery** class has these methods.</span></span>



| <span data-ttu-id="248aa-114">Methode</span><span class="sxs-lookup"><span data-stu-id="248aa-114">Method</span></span>            | <span data-ttu-id="248aa-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="248aa-115">Description</span></span>                                                                                                                                                                        |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="248aa-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="248aa-116">**Reset**</span></span>         | <span data-ttu-id="248aa-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="248aa-117">Not implemented.</span></span> <span data-ttu-id="248aa-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ Akku**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="248aa-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/>                 |
| <span data-ttu-id="248aa-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="248aa-119">**SetPowerState**</span></span> | <span data-ttu-id="248aa-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="248aa-120">Not implemented.</span></span> <span data-ttu-id="248aa-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ Akku**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="248aa-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="248aa-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="248aa-122">Properties</span></span>

<span data-ttu-id="248aa-123">Die **Win32 \_ portableakku** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="248aa-123">The **Win32\_PortableBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="248aa-124">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="248aa-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="248aa-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-127">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="248aa-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-128">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="248aa-128">Availability and status of the device.</span></span>

<span data-ttu-id="248aa-129">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="248aa-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="248aa-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="248aa-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="248aa-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="248aa-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="248aa-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-133">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="248aa-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="248aa-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="248aa-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="248aa-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="248aa-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="248aa-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="248aa-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="248aa-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="248aa-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="248aa-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="248aa-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="248aa-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="248aa-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="248aa-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="248aa-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="248aa-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="248aa-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="248aa-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="248aa-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="248aa-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="248aa-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="248aa-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="248aa-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="248aa-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="248aa-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="248aa-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="248aa-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="248aa-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="248aa-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="248aa-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="248aa-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="248aa-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="248aa-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="248aa-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-153">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="248aa-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="248aa-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="248aa-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-155">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="248aa-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="248aa-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="248aa-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-157">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="248aa-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="248aa-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="248aa-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-159">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="248aa-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="248aa-160">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="248aa-160">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="248aa-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-163">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="248aa-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-164">Die Beschreibung des Ladestatus der Batterie.</span><span class="sxs-lookup"><span data-stu-id="248aa-164">Description of the battery's charge status.</span></span> <span data-ttu-id="248aa-165">Der Wert 10 (nicht definiert) ist im CIM-Schema (Common Information Model) ungültig, da er in der Desktop Management Interface (DMI) anzeigt, dass kein Akku installiert ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-165">The value 10 (Undefined) is not valid in the Common Information Model (CIM) schema because in Desktop Management Interface (DMI) it indicates that no battery is installed.</span></span> <span data-ttu-id="248aa-166">In diesem Fall sollte dieses Objekt nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-166">In this case, this object should not be instantiated.</span></span>

<span data-ttu-id="248aa-167">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-167">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="248aa-168">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="248aa-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="248aa-169">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="248aa-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="248aa-170">**Vollständig abgerechnet** (3)</span><span class="sxs-lookup"><span data-stu-id="248aa-170">**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="248aa-171">**Niedrig** (4)</span><span class="sxs-lookup"><span data-stu-id="248aa-171">**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="248aa-172">**Kritisch** (5)</span><span class="sxs-lookup"><span data-stu-id="248aa-172">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="248aa-173">Wird **berechnet** (6)</span><span class="sxs-lookup"><span data-stu-id="248aa-173">**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="248aa-174">**Abrechnung und hoch** (7)</span><span class="sxs-lookup"><span data-stu-id="248aa-174">**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="248aa-175">**Abrechnung und niedrig** (8)</span><span class="sxs-lookup"><span data-stu-id="248aa-175">**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="248aa-176">**Abrechnung und kritisch** (9)</span><span class="sxs-lookup"><span data-stu-id="248aa-176">**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="248aa-177">Nicht **definiert** (10)</span><span class="sxs-lookup"><span data-stu-id="248aa-177">**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="248aa-178">**Teilweise abgerechnet** (11)</span><span class="sxs-lookup"><span data-stu-id="248aa-178">**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="248aa-179">**Capacitymultiplikator**</span><span class="sxs-lookup"><span data-stu-id="248aa-179">**CapacityMultiplier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-180">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="248aa-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-182">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22- \| Entwurfs Kapazitäts Multiplikator")</span><span class="sxs-lookup"><span data-stu-id="248aa-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Design Capacity Multiplier")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-183">Multiplikationsfaktor des **DesignCapacity** -Werts, um sicherzustellen, dass der milliwattstunden-Stunden Wert für SBDS-Implementierungen (Smart Akku Data Specification) keinen Überlauf erzeugt.</span><span class="sxs-lookup"><span data-stu-id="248aa-183">Multiplication factor of the **DesignCapacity** value to ensure that the milliwatt hour value does not overflow for Smart Battery Data Specification (SBDS) implementations.</span></span>

</dd> <dt>

<span data-ttu-id="248aa-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="248aa-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-187">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="248aa-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-188">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="248aa-188">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="248aa-189">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-190">**Chemi**</span><span class="sxs-lookup"><span data-stu-id="248aa-190">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-191">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="248aa-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-193">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="248aa-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-194">Chemie des Akkus.</span><span class="sxs-lookup"><span data-stu-id="248aa-194">Chemistry of the battery.</span></span>

<span data-ttu-id="248aa-195">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-195">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="248aa-196">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="248aa-196">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="248aa-197">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="248aa-197">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="248aa-198">**Führende Acid** (3)</span><span class="sxs-lookup"><span data-stu-id="248aa-198">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="248aa-199">**Nickel-Cadmium** (4)</span><span class="sxs-lookup"><span data-stu-id="248aa-199">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="248aa-200">**Nickel-Metal-Hydride** (5)</span><span class="sxs-lookup"><span data-stu-id="248aa-200">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="248aa-201">**Lithium-Ion** (6)</span><span class="sxs-lookup"><span data-stu-id="248aa-201">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="248aa-202">**Zink Luft** (7)</span><span class="sxs-lookup"><span data-stu-id="248aa-202">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="248aa-203">**Lithium-Polymer** (8)</span><span class="sxs-lookup"><span data-stu-id="248aa-203">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="248aa-204">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="248aa-204">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-205">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-207">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="248aa-207">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-208">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="248aa-208">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="248aa-209">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-209">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="248aa-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="248aa-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="248aa-211"> (0)</span><span class="sxs-lookup"><span data-stu-id="248aa-211">(0)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-212">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="248aa-212">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="248aa-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="248aa-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="248aa-214">(1)</span><span class="sxs-lookup"><span data-stu-id="248aa-214">(1)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-215">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="248aa-215">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="248aa-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="248aa-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="248aa-217">(2)</span><span class="sxs-lookup"><span data-stu-id="248aa-217">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="248aa-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="248aa-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="248aa-219">(3)</span><span class="sxs-lookup"><span data-stu-id="248aa-219">(3)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-220">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="248aa-220">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="248aa-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="248aa-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="248aa-222">(4)</span><span class="sxs-lookup"><span data-stu-id="248aa-222">(4)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-223">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="248aa-223">Device is not working properly.</span></span> <span data-ttu-id="248aa-224">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="248aa-224">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="248aa-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="248aa-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="248aa-226">(5)</span><span class="sxs-lookup"><span data-stu-id="248aa-226">(5)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-227">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="248aa-227">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="248aa-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="248aa-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="248aa-229"> (6)</span><span class="sxs-lookup"><span data-stu-id="248aa-229">(6)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-230">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="248aa-230">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="248aa-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="248aa-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="248aa-232">(7)</span><span class="sxs-lookup"><span data-stu-id="248aa-232">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="248aa-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="248aa-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="248aa-234">(8)</span><span class="sxs-lookup"><span data-stu-id="248aa-234">(8)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-235">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="248aa-235">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="248aa-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="248aa-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="248aa-237">(9)</span><span class="sxs-lookup"><span data-stu-id="248aa-237">(9)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-238">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="248aa-238">Device is not working properly.</span></span> <span data-ttu-id="248aa-239">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="248aa-239">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="248aa-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="248aa-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="248aa-241">(10)</span><span class="sxs-lookup"><span data-stu-id="248aa-241">(10)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-242">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-242">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="248aa-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="248aa-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="248aa-244">(11)</span><span class="sxs-lookup"><span data-stu-id="248aa-244">(11)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-245">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="248aa-245">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="248aa-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="248aa-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="248aa-247">(12)</span><span class="sxs-lookup"><span data-stu-id="248aa-247">(12)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-248">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="248aa-248">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="248aa-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="248aa-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="248aa-250">(13)</span><span class="sxs-lookup"><span data-stu-id="248aa-250">(13)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-251">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-251">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="248aa-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="248aa-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="248aa-253">(14)</span><span class="sxs-lookup"><span data-stu-id="248aa-253">(14)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-254">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="248aa-254">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="248aa-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="248aa-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="248aa-256">(15)</span><span class="sxs-lookup"><span data-stu-id="248aa-256">(15)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-257">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="248aa-257">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="248aa-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="248aa-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="248aa-259">(16)</span><span class="sxs-lookup"><span data-stu-id="248aa-259">(16)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-260">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-260">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="248aa-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="248aa-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="248aa-262">(17)</span><span class="sxs-lookup"><span data-stu-id="248aa-262">(17)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-263">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="248aa-263">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="248aa-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="248aa-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="248aa-265">(18)</span><span class="sxs-lookup"><span data-stu-id="248aa-265">(18)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-266">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-266">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="248aa-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="248aa-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="248aa-268">(19)</span><span class="sxs-lookup"><span data-stu-id="248aa-268">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="248aa-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="248aa-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="248aa-270">(20)</span><span class="sxs-lookup"><span data-stu-id="248aa-270">(20)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-271">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="248aa-271">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="248aa-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="248aa-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="248aa-273">(21)</span><span class="sxs-lookup"><span data-stu-id="248aa-273">(21)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-274">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="248aa-274">System failure.</span></span> <span data-ttu-id="248aa-275">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="248aa-275">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="248aa-276">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="248aa-276">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="248aa-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="248aa-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="248aa-278">(22)</span><span class="sxs-lookup"><span data-stu-id="248aa-278">(22)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-279">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="248aa-279">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="248aa-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="248aa-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="248aa-281">(23)</span><span class="sxs-lookup"><span data-stu-id="248aa-281">(23)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-282">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="248aa-282">System failure.</span></span> <span data-ttu-id="248aa-283">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="248aa-283">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="248aa-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="248aa-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="248aa-285">(24)</span><span class="sxs-lookup"><span data-stu-id="248aa-285">(24)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-286">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="248aa-286">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="248aa-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="248aa-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="248aa-288">(25)</span><span class="sxs-lookup"><span data-stu-id="248aa-288">(25)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-289">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="248aa-289">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="248aa-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="248aa-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="248aa-291">(26)</span><span class="sxs-lookup"><span data-stu-id="248aa-291">(26)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-292">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="248aa-292">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="248aa-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="248aa-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="248aa-294">(27)</span><span class="sxs-lookup"><span data-stu-id="248aa-294">(27)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-295">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="248aa-295">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="248aa-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="248aa-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="248aa-297">(28)</span><span class="sxs-lookup"><span data-stu-id="248aa-297">(28)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-298">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="248aa-298">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="248aa-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="248aa-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="248aa-300">(29)</span><span class="sxs-lookup"><span data-stu-id="248aa-300">(29)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-301">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="248aa-301">Device is disabled.</span></span> <span data-ttu-id="248aa-302">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="248aa-302">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="248aa-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="248aa-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="248aa-304">(30)</span><span class="sxs-lookup"><span data-stu-id="248aa-304">(30)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-305">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="248aa-305">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="248aa-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="248aa-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="248aa-307">31,5</span><span class="sxs-lookup"><span data-stu-id="248aa-307">(31)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-308">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="248aa-308">Device is not working properly.</span></span> <span data-ttu-id="248aa-309">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-309">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="248aa-310">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="248aa-310">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-311">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="248aa-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-313">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="248aa-313">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-314">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="248aa-314">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="248aa-315">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-316">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="248aa-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-319">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="248aa-319">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="248aa-320">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="248aa-320">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="248aa-321">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-321">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="248aa-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-323">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="248aa-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-326">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="248aa-326">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-327">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="248aa-327">Description of the object.</span></span>

<span data-ttu-id="248aa-328">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-329">**Design Capacity**</span><span class="sxs-lookup"><span data-stu-id="248aa-329">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-330">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-332">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,8 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Milliwatt Stunden ")</span><span class="sxs-lookup"><span data-stu-id="248aa-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-333">Die Entwurfs Kapazität der Akkukapazität in Milliwatt Stunden.</span><span class="sxs-lookup"><span data-stu-id="248aa-333">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="248aa-334">Wenn diese Eigenschaft nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="248aa-334">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="248aa-335">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-335">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-336">**Design Spannung**</span><span class="sxs-lookup"><span data-stu-id="248aa-336">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-337">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="248aa-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-339">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,9 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Millivolt ")</span><span class="sxs-lookup"><span data-stu-id="248aa-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-340">Die Entwurfs Spannung des Akkus in Millivolt.</span><span class="sxs-lookup"><span data-stu-id="248aa-340">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="248aa-341">Wenn dieses Attribut nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="248aa-341">If this attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="248aa-342">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-342">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="248aa-343">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="248aa-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-344">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="248aa-344">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-347">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="248aa-347">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-348">Akku Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="248aa-348">Battery identifier.</span></span>

<span data-ttu-id="248aa-349">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="248aa-350">Beispiel: "Interner Akku"</span><span class="sxs-lookup"><span data-stu-id="248aa-350">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="248aa-351">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="248aa-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-352">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="248aa-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="248aa-354">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="248aa-354">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="248aa-355">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="248aa-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-357">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="248aa-359">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie zu den ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="248aa-359">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="248aa-360">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-361">**Estimatedchargeremainung**</span><span class="sxs-lookup"><span data-stu-id="248aa-361">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-362">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="248aa-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-364">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="248aa-364">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-365">Schätzung des Prozentsatzes der verbleibenden Gesamtkosten.</span><span class="sxs-lookup"><span data-stu-id="248aa-365">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="248aa-366">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-366">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-367">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="248aa-367">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-368">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-370">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,15 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Minuten ")</span><span class="sxs-lookup"><span data-stu-id="248aa-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-371">Schätzen Sie die Zeit in Minuten für die Belastung der Akku Kosten unter den aktuellen Ladebedingungen ein, wenn die Stromversorgung ausfällt, verloren geht und ausfällt oder ein Laptop von einer Stromquelle getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-371">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="248aa-372">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-372">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-373">**Expectedbatterylife**</span><span class="sxs-lookup"><span data-stu-id="248aa-373">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-374">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="248aa-376">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="248aa-376">Not supported.</span></span>

<span data-ttu-id="248aa-377">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-378">**Expectedlife**</span><span class="sxs-lookup"><span data-stu-id="248aa-378">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-379">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-381">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="248aa-381">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-382">Erwartete Lebensdauer des Akkus (in Minuten), vorausgesetzt, dass der Akku vollständig abgerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="248aa-382">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="248aa-383">Diese Eigenschaft stellt die erwartete Gesamtlebensdauer des Akkus dar, nicht die aktuelle verbleibende Lebensdauer, die durch die **EstimatedRunTime** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="248aa-383">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="248aa-384">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-384">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-385">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="248aa-385">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-386">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-388">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,11 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Milliwatt Stunden ")</span><span class="sxs-lookup"><span data-stu-id="248aa-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-389">Volle Ladekapazität des Akkus in Milliwatt Stunden.</span><span class="sxs-lookup"><span data-stu-id="248aa-389">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="248aa-390">Der Vergleich dieses Werts mit der **DesignCapacity** -Eigenschaft bestimmt, wann der Akku ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="248aa-390">Comparison of this value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="248aa-391">Das Ende der Lebensdauer des Akkus ist normalerweise der Fall, wenn die **FullChargeCapacity** -Eigenschaft unter 80% der **DesignCapacity** -Eigenschaft liegt.</span><span class="sxs-lookup"><span data-stu-id="248aa-391">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="248aa-392">Wenn diese Eigenschaft nicht unterstützt wird, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="248aa-392">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="248aa-393">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-393">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-394">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="248aa-394">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-395">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="248aa-395">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-397">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="248aa-397">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-398">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="248aa-398">Date and time the object was installed.</span></span> <span data-ttu-id="248aa-399">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-399">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="248aa-400">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-400">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-401">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="248aa-401">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-402">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="248aa-404">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="248aa-404">Last error code reported by the logical device.</span></span>

<span data-ttu-id="248aa-405">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-406">**Location**</span><span class="sxs-lookup"><span data-stu-id="248aa-406">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-407">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-409">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22 \| Location")</span><span class="sxs-lookup"><span data-stu-id="248aa-409">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-410">Physischer Speicherort der Batterie.</span><span class="sxs-lookup"><span data-stu-id="248aa-410">Physical location of the battery.</span></span> <span data-ttu-id="248aa-411">Diese Eigenschaft wird vom Computerhersteller ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="248aa-411">This property is filled by the computer manufacturer.</span></span>

<span data-ttu-id="248aa-412">Beispiel: "im Hintergrund auf der linken Seite"</span><span class="sxs-lookup"><span data-stu-id="248aa-412">Example: "In the back, on the left"</span></span>

</dd> <dt>

<span data-ttu-id="248aa-413">**Manufaktur Date**</span><span class="sxs-lookup"><span data-stu-id="248aa-413">**ManufactureDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-414">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-416">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22 \| Manufacturing Date")</span><span class="sxs-lookup"><span data-stu-id="248aa-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacture Date")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-417">Das Datum, an dem der Akku gefertigt wurde.</span><span class="sxs-lookup"><span data-stu-id="248aa-417">Date when the battery was manufactured.</span></span>

</dd> <dt>

<span data-ttu-id="248aa-418">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="248aa-418">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-419">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-421">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22- \| Hersteller")</span><span class="sxs-lookup"><span data-stu-id="248aa-421">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-422">Hersteller des Akkus.</span><span class="sxs-lookup"><span data-stu-id="248aa-422">Manufacturer of the battery.</span></span>

</dd> <dt>

<span data-ttu-id="248aa-423">**MaxBatteryError**</span><span class="sxs-lookup"><span data-stu-id="248aa-423">**MaxBatteryError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-424">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="248aa-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-426">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 22 \| maximaler Fehler in Akku Daten"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Prozent")</span><span class="sxs-lookup"><span data-stu-id="248aa-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Maximum Error in Battery Data"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-427">Der Unterschied zwischen der höchsten geschätzten Stromversorgung in der Akkukapazität und dem aktuellen Betrag, der durch den Akku gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="248aa-427">Difference between the highest estimated amount of energy left in the battery and the current amount reported by the battery.</span></span>

</dd> <dt>

<span data-ttu-id="248aa-428">**Maxakku Zeit**</span><span class="sxs-lookup"><span data-stu-id="248aa-428">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-429">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-431">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="248aa-431">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-432">Maximale Zeit in Minuten, um den Akku vollständig zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="248aa-432">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="248aa-433">Diese Eigenschaft stellt die Zeit dar, die eine vollständig abgelegte Akkukapazität wieder auflädt, nicht die derzeit verbleibende Ladezeit, die in der **Timeto fullladung** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-433">This property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="248aa-434">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-434">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-435">**Name**</span><span class="sxs-lookup"><span data-stu-id="248aa-435">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-438">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="248aa-438">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-439">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-439">Label by which the object is known.</span></span> <span data-ttu-id="248aa-440">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-440">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="248aa-441">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="248aa-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-443">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-445">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="248aa-445">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-446">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="248aa-446">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="248aa-447">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="248aa-448">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="248aa-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="248aa-449">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="248aa-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-450">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="248aa-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="248aa-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="248aa-452">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="248aa-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="248aa-453">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="248aa-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="248aa-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="248aa-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="248aa-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="248aa-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="248aa-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="248aa-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="248aa-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-458">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="248aa-458">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="248aa-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="248aa-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-460">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="248aa-460">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="248aa-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="248aa-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-462">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="248aa-462">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="248aa-463">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-463">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="248aa-464">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="248aa-464">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="248aa-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="248aa-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-466">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-466">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="248aa-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="248aa-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="248aa-468">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="248aa-468">Timed Power-On Supported</span></span>

<span data-ttu-id="248aa-469">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="248aa-470">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="248aa-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-471">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="248aa-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="248aa-473">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="248aa-473">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="248aa-474">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-474">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="248aa-475">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-476">**Smartbatteryversion**</span><span class="sxs-lookup"><span data-stu-id="248aa-476">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-477">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-478">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-479">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="248aa-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-480">Von diesem Akku unterstützte Versionsnummer der Smart Akku-Daten Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="248aa-480">Smart Battery Data Specification version number supported by this battery.</span></span> <span data-ttu-id="248aa-481">Wenn der Akku diese Funktion nicht unterstützt, sollte der Wert leer gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-481">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="248aa-482">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-482">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-483">**Status**</span><span class="sxs-lookup"><span data-stu-id="248aa-483">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-484">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-485">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-486">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="248aa-486">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-487">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="248aa-487">Current status of the object.</span></span> <span data-ttu-id="248aa-488">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-488">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="248aa-489">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="248aa-489">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="248aa-490">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="248aa-490">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="248aa-491">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-491">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="248aa-492">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="248aa-492">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="248aa-493">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-493">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="248aa-494">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="248aa-494">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="248aa-495">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="248aa-495">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="248aa-496">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="248aa-496">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="248aa-497">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="248aa-497">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="248aa-498">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="248aa-498">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="248aa-499">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="248aa-499">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="248aa-500">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="248aa-500">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="248aa-501">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="248aa-501">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="248aa-502">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="248aa-502">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="248aa-503">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="248aa-503">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="248aa-504">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="248aa-504">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="248aa-505">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="248aa-505">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="248aa-506">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="248aa-506">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="248aa-507">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="248aa-507">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-508">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="248aa-508">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-509">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-510">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="248aa-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-511">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="248aa-511">State of the logical device.</span></span> <span data-ttu-id="248aa-512">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="248aa-512">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="248aa-513">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-513">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="248aa-514">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="248aa-514">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="248aa-515">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="248aa-515">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="248aa-516">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="248aa-516">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="248aa-517">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="248aa-517">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="248aa-518">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="248aa-518">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="248aa-519">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="248aa-519">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-520">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-521">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-522">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="248aa-522">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="248aa-523">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="248aa-523">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="248aa-524">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-525">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="248aa-525">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-526">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="248aa-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-527">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-528">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="248aa-528">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="248aa-529">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="248aa-529">Name of the scoping system.</span></span>

<span data-ttu-id="248aa-530">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-530">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-531">**Timeonakku**</span><span class="sxs-lookup"><span data-stu-id="248aa-531">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-532">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-532">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-533">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-533">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-534">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Sekunden")</span><span class="sxs-lookup"><span data-stu-id="248aa-534">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-535">Verstrichene Zeit in Sekunden seit der letzten Umstellung des Computer Systems auf die Akkuleistung oder die Zeit seit dem letzten Neustart des Systems oder der UPS, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="248aa-535">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="248aa-536">Wenn der Akku Online ist, wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="248aa-536">If the battery is online, 0 (zero) is returned.</span></span>

<span data-ttu-id="248aa-537">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-537">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="248aa-538">**Timeto fullladung**</span><span class="sxs-lookup"><span data-stu-id="248aa-538">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="248aa-539">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="248aa-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="248aa-540">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="248aa-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="248aa-541">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Portable Akku \| 002,16 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Minuten ")</span><span class="sxs-lookup"><span data-stu-id="248aa-541">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="248aa-542">Verbleibende Zeit in Minuten, um den Akku vollständig mit der aktuellen Gebühr und Nutzung zu belasten.</span><span class="sxs-lookup"><span data-stu-id="248aa-542">Remaining time in minutes to charge the battery fully at the current charge rate and usage.</span></span>

<span data-ttu-id="248aa-543">Diese Eigenschaft wird von [**CIM- \_ Akku**](cim-battery.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="248aa-543">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="248aa-544">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="248aa-544">Remarks</span></span>

<span data-ttu-id="248aa-545">Die **Win32- \_ portableakku** -Klasse wird von [**CIM- \_ Akku**](cim-battery.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="248aa-545">The **Win32\_PortableBattery** class is derived from [**CIM\_Battery**](cim-battery.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="248aa-546">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="248aa-546">Requirements</span></span>



| <span data-ttu-id="248aa-547">Anforderung</span><span class="sxs-lookup"><span data-stu-id="248aa-547">Requirement</span></span> | <span data-ttu-id="248aa-548">Wert</span><span class="sxs-lookup"><span data-stu-id="248aa-548">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="248aa-549">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="248aa-549">Minimum supported client</span></span><br/> | <span data-ttu-id="248aa-550">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="248aa-550">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="248aa-551">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="248aa-551">Minimum supported server</span></span><br/> | <span data-ttu-id="248aa-552">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="248aa-552">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="248aa-553">Namespace</span><span class="sxs-lookup"><span data-stu-id="248aa-553">Namespace</span></span><br/>                | <span data-ttu-id="248aa-554">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="248aa-554">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="248aa-555">MOF</span><span class="sxs-lookup"><span data-stu-id="248aa-555">MOF</span></span><br/>                      | <dl> <span data-ttu-id="248aa-556"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="248aa-556"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="248aa-557">DLL</span><span class="sxs-lookup"><span data-stu-id="248aa-557">DLL</span></span><br/>                      | <dl> <span data-ttu-id="248aa-558"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="248aa-558"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="248aa-559">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="248aa-559">See also</span></span>

<dl> <dt>

[<span data-ttu-id="248aa-560">**CIM- \_ Akku**</span><span class="sxs-lookup"><span data-stu-id="248aa-560">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="248aa-561">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="248aa-561">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
