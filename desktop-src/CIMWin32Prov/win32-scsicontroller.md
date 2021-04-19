---
description: Die Win32 \_ SCSIController-WMI-Klasse stellt einen SCSI-Controller auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 14ed523e-d505-40fa-81d5-3a71eb9f078e
ms.tgt_platform: multiple
title: Win32_SCSIController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIController
- Win32_SCSIController.Reset
- Win32_SCSIController.SetPowerState
- Win32_SCSIController.Availability
- Win32_SCSIController.Caption
- Win32_SCSIController.ConfigManagerErrorCode
- Win32_SCSIController.ConfigManagerUserConfig
- Win32_SCSIController.ControllerTimeouts
- Win32_SCSIController.CreationClassName
- Win32_SCSIController.Description
- Win32_SCSIController.DeviceID
- Win32_SCSIController.DeviceMap
- Win32_SCSIController.DriverName
- Win32_SCSIController.ErrorCleared
- Win32_SCSIController.ErrorDescription
- Win32_SCSIController.HardwareVersion
- Win32_SCSIController.Index
- Win32_SCSIController.InstallDate
- Win32_SCSIController.LastErrorCode
- Win32_SCSIController.Manufacturer
- Win32_SCSIController.MaxDataWidth
- Win32_SCSIController.MaxNumberControlled
- Win32_SCSIController.MaxTransferRate
- Win32_SCSIController.Name
- Win32_SCSIController.PNPDeviceID
- Win32_SCSIController.PowerManagementCapabilities
- Win32_SCSIController.PowerManagementSupported
- Win32_SCSIController.ProtectionManagement
- Win32_SCSIController.ProtocolSupported
- Win32_SCSIController.Status
- Win32_SCSIController.StatusInfo
- Win32_SCSIController.SystemCreationClassName
- Win32_SCSIController.SystemName
- Win32_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f8ba77d626ada787ed18fd9855333fa813f3ab7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346865"
---
# <a name="win32_scsicontroller-class"></a><span data-ttu-id="07b3d-103">Win32 \_ SCSIController-Klasse</span><span class="sxs-lookup"><span data-stu-id="07b3d-103">Win32\_SCSIController class</span></span>

<span data-ttu-id="07b3d-104">Die **Win32 \_ SCSIController** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt einen SCSI-Controller auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-104">The **Win32\_SCSIController** [WMI class](../wmisdk/retrieving-a-class.md) represents a SCSI controller on a computer system running Windows.</span></span>

<span data-ttu-id="07b3d-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07b3d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="07b3d-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="07b3d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b3d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="07b3d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SCSIController : CIM_SCSIController
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  string   DeviceMap;
  string   DriverName;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareVersion;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="07b3d-108">Member</span><span class="sxs-lookup"><span data-stu-id="07b3d-108">Members</span></span>

<span data-ttu-id="07b3d-109">Die **Win32 \_ SCSIController** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="07b3d-109">The **Win32\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="07b3d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="07b3d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="07b3d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07b3d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07b3d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="07b3d-112">Methods</span></span>

<span data-ttu-id="07b3d-113">Die **Win32 \_ SCSIController** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-113">The **Win32\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="07b3d-114">Methode</span><span class="sxs-lookup"><span data-stu-id="07b3d-114">Method</span></span>            | <span data-ttu-id="07b3d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07b3d-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b3d-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="07b3d-116">**Reset**</span></span>         | <span data-ttu-id="07b3d-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-117">Not implemented.</span></span> <span data-ttu-id="07b3d-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="07b3d-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/>                 |
| <span data-ttu-id="07b3d-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="07b3d-119">**SetPowerState**</span></span> | <span data-ttu-id="07b3d-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-120">Not implemented.</span></span> <span data-ttu-id="07b3d-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="07b3d-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="07b3d-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="07b3d-122">Properties</span></span>

<span data-ttu-id="07b3d-123">Die **Win32 \_ SCSIController** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="07b3d-123">The **Win32\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07b3d-124">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="07b3d-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3d-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-127">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="07b3d-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-128">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-128">Availability and status of the device.</span></span>

<span data-ttu-id="07b3d-129">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07b3d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07b3d-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3d-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="07b3d-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3d-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-133">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="07b3d-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="07b3d-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="07b3d-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="07b3d-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="07b3d-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="07b3d-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="07b3d-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="07b3d-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="07b3d-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="07b3d-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="07b3d-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="07b3d-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="07b3d-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07b3d-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="07b3d-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="07b3d-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="07b3d-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="07b3d-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="07b3d-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="07b3d-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="07b3d-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="07b3d-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="07b3d-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="07b3d-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="07b3d-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="07b3d-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="07b3d-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="07b3d-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="07b3d-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="07b3d-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="07b3d-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="07b3d-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="07b3d-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-153">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="07b3d-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="07b3d-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="07b3d-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-155">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="07b3d-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="07b3d-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="07b3d-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-157">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="07b3d-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="07b3d-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-159">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="07b3d-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07b3d-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="07b3d-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-163">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="07b3d-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-164">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-164">Short description of the object.</span></span>

<span data-ttu-id="07b3d-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-166">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="07b3d-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b3d-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-169">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07b3d-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-170">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="07b3d-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="07b3d-171">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="07b3d-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="07b3d-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="07b3d-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-174">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="07b3d-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="07b3d-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="07b3d-176">(1)</span><span class="sxs-lookup"><span data-stu-id="07b3d-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-177">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07b3d-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="07b3d-179">(2)</span><span class="sxs-lookup"><span data-stu-id="07b3d-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="07b3d-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="07b3d-181">(3)</span><span class="sxs-lookup"><span data-stu-id="07b3d-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-182">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="07b3d-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="07b3d-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="07b3d-184">(4)</span><span class="sxs-lookup"><span data-stu-id="07b3d-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-185">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="07b3d-185">Device is not working properly.</span></span> <span data-ttu-id="07b3d-186">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="07b3d-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="07b3d-188">(5)</span><span class="sxs-lookup"><span data-stu-id="07b3d-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-189">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="07b3d-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="07b3d-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="07b3d-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="07b3d-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-192">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="07b3d-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="07b3d-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="07b3d-194">(7)</span><span class="sxs-lookup"><span data-stu-id="07b3d-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="07b3d-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="07b3d-196">(8)</span><span class="sxs-lookup"><span data-stu-id="07b3d-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-197">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="07b3d-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="07b3d-199">(9)</span><span class="sxs-lookup"><span data-stu-id="07b3d-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-200">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="07b3d-200">Device is not working properly.</span></span> <span data-ttu-id="07b3d-201">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="07b3d-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="07b3d-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="07b3d-203">(10)</span><span class="sxs-lookup"><span data-stu-id="07b3d-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-204">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="07b3d-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="07b3d-206">(11)</span><span class="sxs-lookup"><span data-stu-id="07b3d-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-207">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="07b3d-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="07b3d-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="07b3d-209">(12)</span><span class="sxs-lookup"><span data-stu-id="07b3d-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-210">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="07b3d-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="07b3d-212">(13)</span><span class="sxs-lookup"><span data-stu-id="07b3d-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-213">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="07b3d-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="07b3d-215">(14)</span><span class="sxs-lookup"><span data-stu-id="07b3d-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-216">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="07b3d-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="07b3d-218">(15)</span><span class="sxs-lookup"><span data-stu-id="07b3d-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-219">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="07b3d-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="07b3d-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="07b3d-221">(16)</span><span class="sxs-lookup"><span data-stu-id="07b3d-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-222">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="07b3d-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="07b3d-224">(17)</span><span class="sxs-lookup"><span data-stu-id="07b3d-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-225">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="07b3d-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07b3d-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="07b3d-227">(18)</span><span class="sxs-lookup"><span data-stu-id="07b3d-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-228">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="07b3d-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="07b3d-230">(19)</span><span class="sxs-lookup"><span data-stu-id="07b3d-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="07b3d-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="07b3d-232">(20)</span><span class="sxs-lookup"><span data-stu-id="07b3d-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-233">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="07b3d-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="07b3d-235">(21)</span><span class="sxs-lookup"><span data-stu-id="07b3d-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-236">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="07b3d-236">System failure.</span></span> <span data-ttu-id="07b3d-237">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="07b3d-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="07b3d-238">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="07b3d-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="07b3d-240">(22)</span><span class="sxs-lookup"><span data-stu-id="07b3d-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-241">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="07b3d-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="07b3d-243">(23)</span><span class="sxs-lookup"><span data-stu-id="07b3d-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-244">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="07b3d-244">System failure.</span></span> <span data-ttu-id="07b3d-245">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="07b3d-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="07b3d-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="07b3d-247">(24)</span><span class="sxs-lookup"><span data-stu-id="07b3d-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-248">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="07b3d-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="07b3d-250">(25)</span><span class="sxs-lookup"><span data-stu-id="07b3d-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-251">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="07b3d-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="07b3d-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="07b3d-253">(26)</span><span class="sxs-lookup"><span data-stu-id="07b3d-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-254">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="07b3d-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="07b3d-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="07b3d-256">(27)</span><span class="sxs-lookup"><span data-stu-id="07b3d-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-257">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="07b3d-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="07b3d-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="07b3d-259">(28)</span><span class="sxs-lookup"><span data-stu-id="07b3d-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-260">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="07b3d-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="07b3d-262">(29)</span><span class="sxs-lookup"><span data-stu-id="07b3d-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-263">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="07b3d-263">Device is disabled.</span></span> <span data-ttu-id="07b3d-264">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="07b3d-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="07b3d-266">(30)</span><span class="sxs-lookup"><span data-stu-id="07b3d-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-267">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07b3d-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="07b3d-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="07b3d-269">31,5</span><span class="sxs-lookup"><span data-stu-id="07b3d-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-270">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="07b3d-270">Device is not working properly.</span></span> <span data-ttu-id="07b3d-271">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07b3d-272">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="07b3d-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-273">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="07b3d-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-275">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07b3d-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-276">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="07b3d-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="07b3d-277">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-278">**Controllertimeouts**</span><span class="sxs-lookup"><span data-stu-id="07b3d-278">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-279">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b3d-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-281">Anzahl der Timeouts, die nach dem **TimeOfLastReset** -Wert aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="07b3d-281">Number of time-outs that have occurred after the **TimeOfLastReset** value.</span></span>

<span data-ttu-id="07b3d-282">Diese Eigenschaft wird von [**CIM \_ SCSIController**](cim-scsicontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-282">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-283">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="07b3d-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-284">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-286">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="07b3d-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-287">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-287">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="07b3d-288">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="07b3d-289">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-290">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07b3d-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-291">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-293">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="07b3d-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-294">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-294">Description of the object.</span></span>

<span data-ttu-id="07b3d-295">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="07b3d-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-299">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Geräte-ID"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ Karte \\ \\ SCSI")</span><span class="sxs-lookup"><span data-stu-id="07b3d-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-300">Eindeutiger Bezeichner des SCSI-Controllers mit anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="07b3d-300">Unique identifier of the SCSI controller with other devices on the system.</span></span>

<span data-ttu-id="07b3d-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-302">**DeviceMap**</span><span class="sxs-lookup"><span data-stu-id="07b3d-302">**DeviceMap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-305">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SCSI \| SCSIPort")</span><span class="sxs-lookup"><span data-stu-id="07b3d-305">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-306">Die Reihenfolge, in der die Geräte mit diesem SCSI-Controller aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-306">Order in which the devices are listed with this SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-307">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="07b3d-307">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-310">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| portdriver")</span><span class="sxs-lookup"><span data-stu-id="07b3d-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|PortDriver")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-311">Treiber Dateiname des SCSI-Controllers.</span><span class="sxs-lookup"><span data-stu-id="07b3d-311">Driver file name of the SCSI controller.</span></span>

<span data-ttu-id="07b3d-312">Beispiel: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="07b3d-312">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-313">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="07b3d-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-314">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="07b3d-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-316">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-316">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="07b3d-317">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="07b3d-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-321">Eine frei Form Zeichenfolge, die weitere Informationen über den in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu eventuell durchzuführenden Korrekturmaßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-321">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="07b3d-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-323">**HardwareVersion**</span><span class="sxs-lookup"><span data-stu-id="07b3d-323">**HardwareVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-326">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Enum \\ \\ root \| hwrevision")</span><span class="sxs-lookup"><span data-stu-id="07b3d-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|HWRevision")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-327">Die Hardware Versionsnummer des SCSI-Controllers.</span><span class="sxs-lookup"><span data-stu-id="07b3d-327">Hardware version number of the SCSI controller.</span></span>

<span data-ttu-id="07b3d-328">Beispiel: "1,25"</span><span class="sxs-lookup"><span data-stu-id="07b3d-328">Example: "1.25"</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-329">**Index**</span><span class="sxs-lookup"><span data-stu-id="07b3d-329">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-330">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b3d-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-332">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SCSI \| SCSIPort")</span><span class="sxs-lookup"><span data-stu-id="07b3d-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-333">Index Nummer des SCSI-Controllers in der Systemregistrierung.</span><span class="sxs-lookup"><span data-stu-id="07b3d-333">Index number of the SCSI controller in the system registry.</span></span>

<span data-ttu-id="07b3d-334">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="07b3d-334">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07b3d-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-336">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="07b3d-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-338">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="07b3d-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-339">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-339">Date and time the object was installed.</span></span> <span data-ttu-id="07b3d-340">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="07b3d-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="07b3d-341">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="07b3d-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-343">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b3d-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-345">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="07b3d-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="07b3d-346">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-347">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="07b3d-347">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-350">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Enum \\ \\ root \| MFG")</span><span class="sxs-lookup"><span data-stu-id="07b3d-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-351">Der Name des SCSI-Controller Herstellers.</span><span class="sxs-lookup"><span data-stu-id="07b3d-351">Name of the SCSI controller manufacturer.</span></span>

<span data-ttu-id="07b3d-352">Beispiel: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="07b3d-352">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-353">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="07b3d-353">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-354">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b3d-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-356">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="07b3d-356">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-357">Maximale Daten Breite (in Bit), die vom SCSI-Controller unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-357">Maximum data width (in bits) supported by the SCSI controller.</span></span>

<span data-ttu-id="07b3d-358">Diese Eigenschaft wird von [**CIM \_ SCSIController**](cim-scsicontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-358">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-359">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="07b3d-359">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-360">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b3d-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-362">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="07b3d-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-363">Maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-363">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="07b3d-364">Wenn die Zahl unbekannt ist, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-364">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="07b3d-365">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-365">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-366">**Maxtransferrate**</span><span class="sxs-lookup"><span data-stu-id="07b3d-366">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-367">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07b3d-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-369">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="07b3d-369">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-370">Maximale Übertragungsrate (in Bits pro Sekunde), die vom SCSI-Controller unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-370">Maximum transfer rate (in bits per second) supported by the SCSI controller.</span></span>

<span data-ttu-id="07b3d-371">Diese Eigenschaft wird von [**CIM \_ SCSIController**](cim-scsicontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-371">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<span data-ttu-id="07b3d-372">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="07b3d-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="07b3d-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-376">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="07b3d-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-377">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="07b3d-377">Label by which the object is known.</span></span> <span data-ttu-id="07b3d-378">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="07b3d-379">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="07b3d-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-383">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07b3d-383">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-384">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-384">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="07b3d-385">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="07b3d-386">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="07b3d-386">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-387">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="07b3d-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-388">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="07b3d-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-390">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-390">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="07b3d-391">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-391">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07b3d-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="07b3d-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="07b3d-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3d-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="07b3d-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3d-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="07b3d-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3d-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-396">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07b3d-396">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="07b3d-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="07b3d-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-398">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="07b3d-398">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="07b3d-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="07b3d-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-400">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-400">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="07b3d-401">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-401">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="07b3d-402">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="07b3d-402">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="07b3d-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="07b3d-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-404">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="07b3d-404">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="07b3d-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="07b3d-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="07b3d-406">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-406">Timed Power-On Supported</span></span>

<span data-ttu-id="07b3d-407">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="07b3d-407">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07b3d-408">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="07b3d-408">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-409">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="07b3d-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-411">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="07b3d-411">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="07b3d-412">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="07b3d-412">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="07b3d-413">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-414">**Schutz Verwaltung**</span><span class="sxs-lookup"><span data-stu-id="07b3d-414">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-415">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3d-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-417">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speicher Controller \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="07b3d-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-418">Unterstützung des SCSI-Controllers, um Redundanz oder Schutz vor Gerätefehlern zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="07b3d-418">Support of the SCSI controller for redundancy or protection against device failures.</span></span>

<span data-ttu-id="07b3d-419">Diese Eigenschaft wird von [**CIM \_ SCSIController**](cim-scsicontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-419">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07b3d-420">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3d-420">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07b3d-421">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3d-421">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="07b3d-422">**Ungeschützt** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3d-422">**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="07b3d-423">**Geschützt** (4)</span><span class="sxs-lookup"><span data-stu-id="07b3d-423">**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="07b3d-424">**Geschützt durch SCC (SCSI-3 Controller-Befehl)** (5)</span><span class="sxs-lookup"><span data-stu-id="07b3d-424">**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="07b3d-425">**Geschützt durch SCC-2 (SCSI-3 Controller-Befehl)** (6)</span><span class="sxs-lookup"><span data-stu-id="07b3d-425">**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07b3d-426">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="07b3d-426">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-427">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3d-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-429">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="07b3d-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-430">Protokoll, das vom Controller für den Zugriff auf "gesteuerte" Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07b3d-430">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="07b3d-431">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-431">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="07b3d-432">In der folgenden Liste werden die möglichen Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-432">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07b3d-433">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3d-433">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07b3d-434">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3d-434">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="07b3d-435">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3d-435">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="07b3d-436">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="07b3d-436">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="07b3d-437">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="07b3d-437">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="07b3d-438">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="07b3d-438">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="07b3d-439">**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="07b3d-439">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="07b3d-440">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="07b3d-440">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="07b3d-441">**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="07b3d-441">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="07b3d-442">**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="07b3d-442">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="07b3d-443">**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="07b3d-443">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="07b3d-444">**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="07b3d-444">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="07b3d-445">**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="07b3d-445">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="07b3d-446">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="07b3d-446">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="07b3d-447">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="07b3d-447">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="07b3d-448">**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="07b3d-448">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="07b3d-449">**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="07b3d-449">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="07b3d-450">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="07b3d-450">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="07b3d-451">**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="07b3d-451">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="07b3d-452">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="07b3d-452">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="07b3d-453">**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="07b3d-453">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="07b3d-454">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="07b3d-454">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="07b3d-455">**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="07b3d-455">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="07b3d-456">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="07b3d-456">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="07b3d-457">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="07b3d-457">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="07b3d-458">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="07b3d-458">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="07b3d-459">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="07b3d-459">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="07b3d-460">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="07b3d-460">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="07b3d-461">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="07b3d-461">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="07b3d-462">**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="07b3d-462">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="07b3d-463">**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="07b3d-463">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="07b3d-464">**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="07b3d-464">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="07b3d-465">**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="07b3d-465">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="07b3d-466">**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="07b3d-466">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="07b3d-467">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="07b3d-467">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="07b3d-468">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="07b3d-468">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="07b3d-469">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="07b3d-469">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="07b3d-470">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="07b3d-470">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="07b3d-471">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="07b3d-471">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="07b3d-472">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="07b3d-472">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="07b3d-473">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="07b3d-473">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="07b3d-474">**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="07b3d-474">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="07b3d-475">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="07b3d-475">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="07b3d-476">**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="07b3d-476">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="07b3d-477">**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="07b3d-477">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="07b3d-478">**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="07b3d-478">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="07b3d-479">" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="07b3d-479">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07b3d-480">**Status**</span><span class="sxs-lookup"><span data-stu-id="07b3d-480">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-483">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="07b3d-483">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-484">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-484">Current status of the object.</span></span> <span data-ttu-id="07b3d-485">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-485">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="07b3d-486">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="07b3d-486">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="07b3d-487">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="07b3d-487">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="07b3d-488">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-488">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="07b3d-489">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="07b3d-489">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="07b3d-490">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-490">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="07b3d-491">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="07b3d-491">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="07b3d-492">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="07b3d-492">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="07b3d-493">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="07b3d-493">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07b3d-494">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="07b3d-494">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07b3d-495">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="07b3d-495">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="07b3d-496">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="07b3d-496">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="07b3d-497">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="07b3d-497">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="07b3d-498">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="07b3d-498">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="07b3d-499">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="07b3d-499">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="07b3d-500">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="07b3d-500">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="07b3d-501">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="07b3d-501">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="07b3d-502">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="07b3d-502">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="07b3d-503">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="07b3d-503">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07b3d-504">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="07b3d-504">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-505">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3d-505">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-506">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-507">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="07b3d-507">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-508">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="07b3d-508">State of the logical device.</span></span> <span data-ttu-id="07b3d-509">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07b3d-509">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="07b3d-510">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07b3d-511">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3d-511">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07b3d-512">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3d-512">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="07b3d-513">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3d-513">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="07b3d-514">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="07b3d-514">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="07b3d-515">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="07b3d-515">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07b3d-516">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="07b3d-516">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-517">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-518">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-518">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-519">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="07b3d-519">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-520">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="07b3d-520">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="07b3d-521">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-522">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="07b3d-522">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="07b3d-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-525">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="07b3d-525">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-526">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="07b3d-526">Name of the scoping system.</span></span>

<span data-ttu-id="07b3d-527">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b3d-528">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="07b3d-528">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3d-529">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="07b3d-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07b3d-530">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="07b3d-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3d-531">Datum und Uhrzeit des letzten zurück Setzens des Controllers.</span><span class="sxs-lookup"><span data-stu-id="07b3d-531">Date and time this controller was last reset.</span></span> <span data-ttu-id="07b3d-532">Dies könnte bedeuten, dass der Controller heruntergefahren oder erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="07b3d-532">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="07b3d-533">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="07b3d-533">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07b3d-534">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07b3d-534">Remarks</span></span>

<span data-ttu-id="07b3d-535">Die **Win32 \_ SCSIController** -Klasse wird von [**CIM \_ SCSIController**](cim-scsicontroller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="07b3d-535">The **Win32\_SCSIController** class is derived from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07b3d-536">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07b3d-536">Requirements</span></span>



| <span data-ttu-id="07b3d-537">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07b3d-537">Requirement</span></span> | <span data-ttu-id="07b3d-538">Wert</span><span class="sxs-lookup"><span data-stu-id="07b3d-538">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07b3d-539">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07b3d-539">Minimum supported client</span></span><br/> | <span data-ttu-id="07b3d-540">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07b3d-540">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07b3d-541">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07b3d-541">Minimum supported server</span></span><br/> | <span data-ttu-id="07b3d-542">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07b3d-542">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07b3d-543">Namespace</span><span class="sxs-lookup"><span data-stu-id="07b3d-543">Namespace</span></span><br/>                | <span data-ttu-id="07b3d-544">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07b3d-544">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07b3d-545">MOF</span><span class="sxs-lookup"><span data-stu-id="07b3d-545">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07b3d-546"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="07b3d-546"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07b3d-547">DLL</span><span class="sxs-lookup"><span data-stu-id="07b3d-547">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07b3d-548"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b3d-548"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b3d-549">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07b3d-549">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b3d-550">**CIM- \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="07b3d-550">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dt>

[<span data-ttu-id="07b3d-551">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="07b3d-551">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
